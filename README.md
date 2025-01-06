#Task 1: Create a "CodingGita Students" database.

##Step 1 : create database named "codinggita". 

    ```use codinggita```

##Step 2 : create collections named "students".

    ```db.createCollection("students");```

##Step 3 : create collections named "courses".

    ```db.createCollection("courses");```

##Step 4 : Insert sample data into student collection. 

    ```db.students.insertMany([
        {
	        "name":"Krish Shyara",
	        "rollnumber":103,
	        "department":"Computer science",
	        "year":"3",
	        "coursesEnrolled": ["CS101", "CS102"]
        }
        ]);```

##Step 5 : Insert sample data into courses collection. 

    ```db.courses.insertMany([
        {
            "courseCode": "CS101", 
            "courseName": "Frontend Development", 
            "credits": 4, 
            "instructor": "Prof. Mehta" 
        }
        ]);```