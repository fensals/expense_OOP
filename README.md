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

To clone this repository:

git clone https://github.com/fensals/expense_OOP.git

```
from expense_manager import Expense, ExpenseDatabase

db = ExpenseDatabase()
expense1 = Expense("Lunch", 15.75)
db.add_expense(expense1)
print(db.to_dict())

```




