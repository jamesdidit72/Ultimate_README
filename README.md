# A README to rule them all
- Contains important information regarding the two-week period where Python was taught
## Operators
| Operand | Description | Example |
|:---------: |:----------------------------: |:--------: |
| > | True if left operand is greater than the right| x > y |
| < | True if left operand is less than the right| x < y |
| == | True if both operands are equal | x == y |
| != | True if both operands are equal | x != y |
| >= | True if left operand is greater than or equal to the right| x >= y |
| <= | True if left operand is less than or equal to the right| x <= y |
## Collection types
- lists | syntax = [ ] | can be edited/ mutable | type = list
- dictionaries | syntax = {"keys":"values"} | type = dict
- tuples | syntax = ( ) | can't be edited once created/ immutable | type = tuple
- sets | syntax = { } | same as a list, but UNORDERED | type = set
## Indexes
- shopping_list = ['juice', 'strawberries', 'yogurt', 'chicken', 'raspberries', 'butter']  # a list contains 6 indexes
- 'juice' = index 0,'strawberries' = index 1,'yogurt' = index 2,'chicken' = index 3,'raspberries' = index 4,'butter' = index 5
- print(shopping_list[3])  # prints the 4th index of list
- print(shopping_list[-1])  # prints the 6th index of list because it is the end of the list
- print(shopping_list[3:6])  # prints the 4th, 5th and 6th index from the list
## Week 1
- dictionaries
  ```python
        contact_list = {
            "a": {
                "james": "76987256"
            },
            "b": {
                "kane": "3498597234"
            },
            "c": {
                "aidan": "29875405"
            }
        }
    
        print(contact_list["b"].keys())
        print(contact_list["b"]["kane"])

  ```
- control flow
    ```python
    user_age = 0
    
    if user_age <= 12:
        print("U, PG, and 12 films")
    elif user_age <= 15:
        print("U, PG, 12 and 15 films")
    else:
        print("you can see every film")
    
    time = 0
    
    if time > 5 and time < 12:
       print("good morning")
    elif time > 12 and time < 18:
        print("Good afternoon")
    else:
        print("Good evening")
    ```
- while loop | loops are used to ITERATE through data
    ```python
    game_active = True
    while game_active:
        game_random_number = random.randint(1, 10)
        user_guess = int(input("Enter a guess:  "))
        if user_guess == game_random_number:
            print(game_random_number, ".You guessed correctly")
            game_active = False
        else:
            print(game_random_number, ".Unlucky, try again")
    print("well done!")
    ```
- for loop | loops are used to ITERATE through data
    ```python
    # DICTIONARY
    student_1 = {
        'name': 'James',
        'key': 'value',
        'stream': 'Cyber Security',  # string
        'completed_lessons': 3,  # int
        'completed_lesson_names': ["variables", "operators", "data_collections"]  # list
    
    }
    for data in student_1:
        print(data)  # only prints the keys
    for data in student_1.values():
        print(data)  # only prints the values
    
    for data in student_1.values():
        if data == "Cyber Security":
            break
        print(data)
    ```
## Week 2
- OOP (Object-Oriented Programming)
  - Four major pillars of OOP
    - Abstraction
        - Hiding unnecessary data, such as when importing modules or looking up the PC specs, it doesn't tell us how it's done, just the answer
    - Inheritance
        - Inherit data from another class, such as how a database extracts data from different databases 
    - Encapsulation
        - When you need to restrict access, such as a bank account. _age = 22 means the variable is private
    - Polymorphism
        - Once code has been inherited from another class, you can change, add new etc without effecting the parent class that the data code was taken from
  - keyword for implementing these modules is 'import'
### Functions
- `def` is used to initialise the function
    - example: `def eat():`
- called via `eat()`
### Classes
- Allows for functions to be used on other files through:
  - `import` or `from file_name import class_name`
- File work
  - `try`, `except` and `finally` blocks of code
  - works similar to `if` and `else:` code
    ```python
    def greeting():  #| throws indention error, missing 'pass'
        name = 'DevSecOps'
        year = 2021
        print(name + year)  #| throws TypeError, cannot put a string and int together
        
        file = open('order.txt')  #| throws FileNotFoundError, file doesnt exist
        
        try:
            file = open('order.txt')
        except FileNotFoundError:
             print('File not found')
        try:
            file = open('order.txt')
        except FileNotFoundError as errmsg:
            # creating aliases
            print('File not found' + str(errmsg))  #|Displays a print with the error message

    ```
### API (Application Programming Interface)
  - An API, or Application Programming Interface, is a server that you can use to retrieve and send data to using code. APIs are most commonly used to retrieve data, and that will be the focus of this beginner tutorial. When we want to receive data from an API, we need to make a request.
    - API call is what UberEats uses (FOod on its way, food delivered etc)
### TDD (Test Driven Development)
  #### use pip to install the packages
    - TDD
    - Starts with RED (everything failing)
    - then GREEN to write the code to pass the test
    - BLUE is refactoring - then start again
    - `unittest` and `pytest`
        - at least two .py files, test.py and functional.py
        - test.py is for the test functions
        - functional.py is for the actual code
        - test functions must start with 'test'
        - assertEqual is a function from pytest(like .upper())
        - must set the object to the class from the functional.py file
        - the values in the test functions are (parameter1, parameter2, answer)
            - example: (10, 50), 60) = 10 + 50 = 60
        - can include hidden parameters
            - example for percentage: (10, 50), 20) = (10 / 50) * 100 = 20