# Object Oriented Programming

The goal of this project is to show my understanding of object-oriented programming (OOP) concepts in Python.
It demonstrates my understanding of object-oriented programming (OOP) concepts in Python, including defining class attributes, methods, and handling time-related functionalities.


I created 2 classes.

1. Expense which represents an individual financial expense.

  The class attributesare:
  - id: A unique identifier generated as a UUID string.
  - title: A string representing the title of the expense.
  - amount: A float representing the amount of the expense.
  - created_at: A timestamp indicating when the expense was created (UTC).
  - updated_at: A timestamp indicating the last time the expense was updated (UTC).
  
  The Methods are:
  - __init__: Initializes the attributes.
  - update: Allows updating the title and/or amount, updating the updated_at timestamp.
  - to_dict: Returns a dictionary representation of the expense.

2. ExpenseDatabase which Manages a collection of expenses.

   This class has only 1 attribute:
     - expenses: A list storing Expense instances.

  The methods are:
    - __init__: Initializes the list.
    - add_expense: Adds an expense.
    - remove_expense: Removes an expense.
    - get_expense_by_id: Retrieves an expense by ID.
    - get_expense_by_title: Retrieves expenses by title.
    - to_dict: Returns a list of dictionaries representing expenses.

## To Clone this repository

git clone https://github.com/fensals/expense_OOP.git


## To run the code...

### Import the classes
```
from expense_expense_db import Expense, ExpenseDatabase
```
### Create instances of the expense class
```
expense1 = Expense("Lunch", 15.75)

expense2 = Expense("Loan", 200)

expense3 = Expense("Subscription", 22)
```

### We can call out any Expense attribute from the above instances. Eg. Title of expense1
```
expense1.title
```
```
'Lunch'
```
### Create an instance of the expense database

```
db = ExpenseDatabase()

```
### add expenses to the database using the add_expense method
```
db.add_expense(expense1, expense2)
```
### Use the to_dict() method to output the contents of the expense db
```
db.to_dict()
```
```
[{'id': 'd19e5a11-900a-4730-a5da-12efaa373325',
  'title': 'Lunch',
  'amount': 15.75,
  'created_at': '2025-02-18T15:29:37.563447',
  'updated_at': '2025-02-18T15:29:37.563447'},
 {'id': '3072f3e5-bee0-40b7-a586-1bf3f8edc2b4',
  'title': 'Loan',
  'amount': 200,
  'created_at': '2025-02-18T15:29:37.563447',
  'updated_at': '2025-02-18T15:29:37.563447'}]
```



