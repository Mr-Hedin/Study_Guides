### Python 2 Study Guide

#### **Section 1: Lists**

- **Creating Lists**: Lists are collections of items in a specific order. To create a list in Python, use square brackets. Example:

  ```python
  books = ['Book1', 'Book2', 'Book3', 'Book4', 'Book5']
  ```

  Practice creating lists with your favorite items to get comfortable with the syntax. Make a list of your favorite books or movies, then print the list.

- **Indexing**: You can access items in a list using their index. Indexing starts from 0, so the third item is at index 2. Example:

  ```python
  colors = ['red', 'blue', 'green', 'yellow', 'purple']
  print(colors[2])  # prints 'green'
  ```

  Practice accessing different items in a list by changing the index number. For example, colors[0] prints the color 'red'.

- **List Changes**: Lists are mutable, meaning you can change them after they are created. Use `.append()` to add an item and `.remove()` to remove an item. Example:

  ```python
  colors.append('orange')
  colors.remove('yellow')
  print(colors)  # prints ['red', 'blue', 'green', 'purple', 'orange']
  ```

  Practice adding and removing items from a list to understand how they work. Use colors.append and add your favorite color. Then practice with colors.remove() and remove a color from the list.

#### **Section 2: While Loops & List Traversals**

- **Basic While Loop**: A `while` loop keeps running as long as a condition is true. Example:

  ```python
  count = 1
  while count <= 5:
      print(count)
      count += 1
  ```

  Practice using `while` loops to understand how they repeat a block of code. Change the value of count to see how long the loop lasts each time.

- **While Loop with a List**: You can use `while` loops to iterate through a list. Example:

  ```python
  numbers = [2, 4, 6, 8, 10]
  i = 0
  while i < len(numbers):
      print(numbers[i])
      i += 1
  ```

  Practice traversing lists with `while` loops to get familiar with iteration. Create a list of your friends' names, then print each one using a while loop and numbers[i].

#### **Section 3: For Loops**

- **Basic For Loop**: A `for` loop is used to iterate over a sequence, such as a string or a list. Example:

  ```python
  for letter in "PYTHON":
      print(letter)
  ```

  Practice writing `for` loops to iterate over strings and lists. Strings are technically lists, you can print each letter like an item in a list.

- **Looping Through a List**: You can use a `for` loop to go through each item in a list. Example:

  ```python
  fruits = ['apple', 'banana', 'cherry', 'date']
  for fruit in fruits:
      print(fruit)
  ```

  Practice using `for` loops to iterate over different lists. Use your lists from above and practice printing or modifying each item in the list.

- **Adding Numbers**: You can use a `for` loop to calculate the sum of numbers in a list. Example:

  ```python
  numbers = [1, 3, 5, 7, 9]
  total = 0
  for num in numbers:
      total += num
  print(total)  # prints 25
  ```

  Practice summing different lists of numbers to reinforce this concept. This is the first of many algorithms that can be implemented with a for loop. Practice subtracting, multiplying, or dividing instead!

#### **Section 4: Review of Python 1 Concepts**

- **Variables and Types**: Variables store data, and their type determines what kind of data they hold. Example:

  ```python
  age = 14
  if age > 10:
      print("Age is greater than 10")
  ```

  Practice creating variables and writing conditions to check their values. Remember, the fours main data types are Integer (whole numbers), Float (decimal numbers), String (words, or anything "in quotes"), Boolean (True/False)

- **If-Else Statements**: Use `if`, `elif`, and `else` to control the flow of your program based on conditions. Example:

  ```python
  temperature = 75
  if temperature > 70:
      print("Warm day")
  else:
      print("Cool day")
  ```

  Practice writing `if-else` statements to handle different scenarios. Create a variable called volume, then write an if statement to check if the volume is above 11 or below 11.

- **Functions**: Functions allow you to reuse blocks of code. Example:

  ```python
  def greet(name):
      print(f"Hello, {name}!")

  greet("Alice")
  ```

  Practice creating and using functions to understand how they work. Functions are like recipes, once you've got the recipe you can reuse it as many times as you'd like. Write a function that says "Nice job creating this function" and your name!

#### **Bonus Challenge**

- **Finding the Maximum Value**: Write a function to find the largest number in a list. Example:
  ```python
  def find_max(numbers):
      max_num = numbers[0]
      for num in numbers:
          if num > max_num:
              max_num = num
      return max_num
  print(find_max([3, 5, 7, 2, 8]))  # prints 8
  ```

---

Use this guide to review each section and practice the examples provided. Understanding these concepts will help you do well on the exam. Remember, practice is key to becoming comfortable with Python programming!


