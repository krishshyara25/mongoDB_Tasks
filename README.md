# Task 1: Create a "CodingGita Students" database.

### Step 1 : create database named "codinggita". 

```
use codinggita
```

### Step 2 : create collections named "students".

```
db.createCollection("students");
```

### Step 3 : create collections named "courses".

```
db.createCollection("courses");
```

### Step 4 : Insert sample data into student collection. 
```    
    db.students.insertMany([
        {
	        "name":"Krish Shyara",
	        "rollnumber":103,
	        "department":"Computer science",
	        "year":"3",
	        "coursesEnrolled": ["CS101", "CS102"]
        }
        ]);
```

### Step 5 : Insert sample data into courses collection. 

```
    db.courses.insertMany([
        {
            "courseCode": "CS101", 
            "courseName": "Frontend Development", 
            "credits": 4, 
            "instructor": "Prof. Mehta" 
        }
        ]);
```



# Task 2: Perform CRUD operations

### Step 1 : Add a few more students and courses to the database.

``` 
    db.students.insertMany([
    { 
        "name": "Dhruvesh",
        "rollNumber": 101,
        "department": "Computer Science",
        "year": 2,
        "coursesEnrolled": ["CS101", "CS102"]
    },
    { 
        "name": "Priy",
        "rollNumber": 101,
        "department": "Computer Science",
        "year": 2,
        "coursesEnrolled": ["CS101", "CS102"]
    },
    ]);
```
 
 ### Step 2 : Query data based on Department (e.g., "Computer Science").

 ```
 db.students.findOne({department : "Computer Science"});
 ```

  ### Step 3 : Query data based on Year (e.g., "2").

  ```
  db.students.find({year:2});
  ```
  ### Step 4 : Query data based on Courses enrolled (e.g., "CS101").

  ```
  db.students.find({"coursesEnrolled" : "CS101"});
  ```

### Step 5 : Update the courses for a specific student (e.g., adding a new course).
```
db.students.updateOne(
  { name: "Mahir" },
  { $set: { coursesEnrolled: "EE101" } }
);
```

### Step 6 : Update the courses for a specific student (e.g., adding a new course).

```
db.students.deleteOne(
  {name : "Mahir"}
);
```