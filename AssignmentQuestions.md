Q1. Creating and Dropping Database & Collection
Task-1:
• Create a new MongoDB database named "PWSKILLS".

    ```
    use PWSKILLS
    ```

Task-2:
• Create a collection named "Employees" within the "PWSKILLS" database.

```
db.createCollection("Employees")
```

Task-3:
Insert several documents representing employees into the "Employees" collection.

```
db.Employees.insertMany([
    {"emp_id":"EMP001",
    "name":"John",
    "job_profile":"Software Engineer",
    "age":30,
    "marriage_status":"Married"},
    {"emp_id":"EMP002",
    "name":"Emma",
    "job_profile":"Product Manager",
    "age":28,
    "marriage_status":"Single"}
    ]);
```

Task-4:
• Retrieve and display all documents from the "Employees" collection.

```
db.Employees.find()
```

Task-5:
Drop the "Employees" collection.

```
db.collection.drop()
```

Task-6:
Drop the "PWSKILLS" database.

```
db.dropDatabase()
```

Q2. Insert a new document representing a customer into the "Customers" collection.
Q3. Retrieve and display all documents from the "Customers" collection.
Q4. Update the address of a specific customer.
Q5. Query for customers who have made purchases over a certain amount.
Q6. Remove a customer from the "Customers" collection.
Q7. Create a new database named "SchoolDB".
Q8. Insert documents into the "Students" collection with fields like name, age, and grade.
Q9. Query for students older than a specific age or belonging to a particular grade.
Q10. Update the grade of a specific student in the "Students" collection.
Q11. Insert documents into the "Teachers" collection representing teachers with fields like name, subject, and
experience.
Q12. Query for teachers specializing in a specific subject or with more than a certain amount of experience.
Q13. Update the experience of a specific teacher in the "Teachers" collection.
