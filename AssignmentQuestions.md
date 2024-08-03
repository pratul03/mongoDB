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
    {
        "emp_id":"EMP001",
        "name":"John",
        "job_profile":"Software Engineer",
        "age":30,
        "marriage_status":"Married"
    },
    {
        "emp_id":"EMP002",
        "name":"Emma",
        "job_profile":"Product Manager",
        "age":28,
        "marriage_status":"Single"
    }
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

```
use customer
```

```
 db.createCollection("Customers")
```

```
db.Customers.insertOne( {"name": "Michael","age": 35,"spend": 1500.75})
```

Q3. Retrieve and display all documents from the "Customers" collection.

```
db.Customers.find()
```

Q4. Update the address of a specific customer.

```
 db.Customers.updateOne(
    { name : "Sarah"},
    {$set : {
        address : {
            city : "Baruipur",
            district: "South 24 Parganas",
            pincode: 743374
            }
        }
    }
)
```

Q5. Query for customers who have made purchases over a certain amount. ( find customers who has purchased over 2000 and below 2000 rupees)

```
db.Customers.find({ spend : {$gt : 2000}})
```

```
db.Customers.find({ spend : {$lt : 2000}})
```

```
db.Customers.find({ spend : {$gte : 2000}})
```

```
db.Customers.find({ spend : {$lte : 2000}})
```

```
db.Customers.find({ spend : {$gte : 2000 ,$lte : 3000}})
```

```
db.Customers.find({ spend : {$in : [2000 , 2500]}})
```

Q6. Remove a customer from the "Customers" collection.

```
db.Customers.deleteOne({ name : "Michael" })
```

Q7. Create a new database named "SchoolDB".

```
use SchoolDB
```

Q8. Insert documents into the "Students" collection with fields like name, age, and grade.

```
db.Students.insertMany([
    {
        name: "Alice",
        age: 20,
        grade: 9
    },
    {
        name: "Bob",
        age: 21,
        grade: 8
    }
]);
```

Q9. Query for students older than a specific age or belonging to a particular grade.

```
db.Students.find({ age : {$gt : 23}})
```

```
db.Students.find({ grade : {$in : [1, 2, 3]}})
```

Q10. Update the grade of a specific student in the "Students" collection.

```
db.Students.updateOne({ name : "Bob" } , { $set : { grade : 2}})
```

Q11. Insert documents into the "Teachers" collection representing teachers with fields like name, subject, and
experience.
Q12. Query for teachers specializing in a specific subject or with more than a certain amount of experience.
Q13. Update the experience of a specific teacher in the "Teachers" collection.
