# Practice Midterm: Python Fundamentals

This practice exam contains 20 exercises designed to test your understanding of Python fundamentals. Each exercise requires combining multiple concepts from sessions 1-11.

**Topics covered:**
- Variables and types
- Operators
- Lists and tuples
- Dictionaries and sets
- Strings
- Conditionals
- Loops
- Comprehensions
- Functions

**Instructions:**
- Read each problem carefully
- Write clean, readable code
- Test your solutions with the provided examples
- Each exercise builds on multiple concepts

---

## Exercise 1: Student Grade Calculator

Write a function `calculate_grade(scores)` that takes a list of numeric scores and returns a dictionary with:
- `"average"`: the average score (rounded to 2 decimals)
- `"letter"`: the letter grade (A: 90+, B: 80-89, C: 70-79, D: 60-69, F: below 60)
- `"passed"`: True if average >= 60, False otherwise

```python
# Example:
scores = [85, 90, 78, 92, 88]
result = calculate_grade(scores)
# result should be: {"average": 86.6, "letter": "B", "passed": True}
```

```python
# Your code here
```

---

## Exercise 2: Word Frequency Counter

Write a function `word_frequency(text)` that takes a string and returns a dictionary where keys are unique words (lowercase, no punctuation) and values are their frequencies. Ignore words with fewer than 3 characters.

```python
# Example:
text = "The quick brown fox jumps over the lazy dog. The dog was not amused."
result = word_frequency(text)
# result should include: {"the": 3, "quick": 1, "brown": 1, "fox": 1, "dog": 2, ...}
```

```python
# Your code here
```

---

## Exercise 3: Shopping Cart

Create a function `process_cart(items)` that takes a list of tuples `(product_name, price, quantity)` and returns a dictionary with:
- `"items"`: list of strings formatted as "2x Apple @ $1.50 = $3.00"
- `"subtotal"`: sum of all items
- `"tax"`: 8% of subtotal (rounded to 2 decimals)
- `"total"`: subtotal + tax (rounded to 2 decimals)

```python
# Example:
items = [("Apple", 1.50, 2), ("Bread", 3.00, 1), ("Milk", 2.50, 3)]
result = process_cart(items)
# result["items"] should be: ["2x Apple @ $1.50 = $3.00", "1x Bread @ $3.00 = $3.00", "3x Milk @ $2.50 = $7.50"]
# result["subtotal"] should be: 13.50
# result["tax"] should be: 1.08
# result["total"] should be: 14.58
```

```python
# Your code here
```

---

## Exercise 4: Password Validator

Write a function `validate_password(password)` that returns a tuple `(is_valid, messages)` where:
- `is_valid` is True if the password meets ALL requirements, False otherwise
- `messages` is a list of strings describing which requirements failed

Requirements:
- At least 8 characters long
- Contains at least one uppercase letter
- Contains at least one lowercase letter
- Contains at least one digit
- Contains at least one special character (!@#$%^&*)

```python
# Example:
result = validate_password("Hello123")
# result should be: (False, ["Missing special character (!@#$%^&*)"])

result = validate_password("Hello@123")
# result should be: (True, [])
```

```python
# Your code here
```

---

## Exercise 5: Contact Book Filter

Given a list of contact dictionaries, write a function `filter_contacts(contacts, **criteria)` that returns only contacts matching ALL provided criteria. Support filtering by any key in the contact dictionary.

```python
# Example:
contacts = [
    {"name": "Alice", "city": "NYC", "age": 30},
    {"name": "Bob", "city": "LA", "age": 25},
    {"name": "Charlie", "city": "NYC", "age": 35},
    {"name": "Diana", "city": "NYC", "age": 25}
]

result = filter_contacts(contacts, city="NYC")
# Returns: [{"name": "Alice", ...}, {"name": "Charlie", ...}, {"name": "Diana", ...}]

result = filter_contacts(contacts, city="NYC", age=25)
# Returns: [{"name": "Diana", "city": "NYC", "age": 25}]
```

```python
# Your code here
```

---

## Exercise 6: Matrix Operations

Write a function `matrix_stats(matrix)` that takes a 2D list (list of lists) of numbers and returns a dictionary with:
- `"rows"`: number of rows
- `"cols"`: number of columns
- `"sum"`: sum of all elements
- `"max"`: maximum value
- `"min"`: minimum value
- `"row_sums"`: list of sums for each row
- `"col_sums"`: list of sums for each column

```python
# Example:
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]
result = matrix_stats(matrix)
# result should include: {"rows": 3, "cols": 3, "sum": 45, "max": 9, "min": 1,
#                         "row_sums": [6, 15, 24], "col_sums": [12, 15, 18]}
```

```python
# Your code here
```

---

## Exercise 7: Email Parser

Write a function `parse_emails(emails)` that takes a list of email addresses and returns a dictionary with:
- `"valid"`: list of valid emails
- `"invalid"`: list of invalid emails
- `"domains"`: dictionary mapping domain names to count of emails

An email is valid if it contains exactly one `@`, has text before and after `@`, and the domain contains at least one `.`

```python
# Example:
emails = ["alice@gmail.com", "bob@company.org", "invalid", "mary@gmail.com", "bad@nodot", "test@sub.domain.com"]
result = parse_emails(emails)
# result["valid"] should be: ["alice@gmail.com", "bob@company.org", "mary@gmail.com", "test@sub.domain.com"]
# result["invalid"] should be: ["invalid", "bad@nodot"]
# result["domains"] should be: {"gmail.com": 2, "company.org": 1, "sub.domain.com": 1}
```

```python
# Your code here
```

---

## Exercise 8: Number Classifier

Write a function `classify_numbers(numbers)` that takes a list of integers and returns a dictionary with:
- `"even"`: list of even numbers
- `"odd"`: list of odd numbers
- `"positive"`: list of positive numbers
- `"negative"`: list of negative numbers
- `"primes"`: list of prime numbers (use a helper function to check primality)

```python
# Example:
numbers = [2, 3, -4, 5, 6, -7, 8, 9, 10, 11, -12, 13]
result = classify_numbers(numbers)
# result["even"] should be: [2, -4, 6, 8, 10, -12]
# result["primes"] should be: [2, 3, 5, 11, 13]
```

```python
# Your code here
```

---

## Exercise 9: Text Statistics

Write a function `text_stats(text)` that analyzes a text and returns a dictionary with:
- `"char_count"`: total characters (excluding spaces)
- `"word_count"`: total words
- `"sentence_count"`: total sentences (count `.`, `!`, `?`)
- `"avg_word_length"`: average word length (rounded to 2 decimals)
- `"longest_word"`: the longest word
- `"most_common_letter"`: the most frequent letter (lowercase, excluding spaces and punctuation)

```python
# Example:
text = "Hello World! How are you doing today? I am fine."
result = text_stats(text)
# result should include: {"char_count": 40, "word_count": 9, "sentence_count": 3, ...}
```

```python
# Your code here
```

---

## Exercise 10: Inventory Manager

Write a function `manage_inventory(inventory, operations)` where:
- `inventory` is a dictionary mapping product names to quantities
- `operations` is a list of tuples: `("add", product, quantity)` or `("remove", product, quantity)`

The function should return a tuple `(updated_inventory, log)` where:
- `updated_inventory` is the modified inventory
- `log` is a list of strings describing each operation and its result

Do not allow negative quantities (log an error instead).

```python
# Example:
inventory = {"apple": 10, "banana": 5}
operations = [
    ("add", "apple", 5),
    ("remove", "banana", 3),
    ("add", "orange", 8),
    ("remove", "apple", 20)
]
result, log = manage_inventory(inventory, operations)
# result should be: {"apple": 15, "banana": 2, "orange": 8}
# log should include: [..., "Error: Cannot remove 20 apple (only 15 available)"]
```

```python
# Your code here
```

---

## Exercise 11: Date Validator

Write a function `validate_date(date_string)` that takes a date string in format "DD/MM/YYYY" and returns a tuple `(is_valid, message)`:
- Check if the format is correct (exactly 2/2/4 digits with slashes)
- Check if day, month, year are valid numbers
- Check if the date is valid (correct days per month, handle leap years)

```python
# Example:
validate_date("29/02/2024")  # (True, "Valid date")
validate_date("29/02/2023")  # (False, "Invalid day for month")
validate_date("31/04/2023")  # (False, "Invalid day for month")
validate_date("15-06-2023")  # (False, "Invalid format")
```

```python
# Your code here
```

---

## Exercise 12: Score Ranking System

Write a function `rank_players(players)` that takes a list of tuples `(name, score)` and returns a list of dictionaries with ranking information:
- `"rank"`: position (1, 2, 3, ...) - players with same score share a rank
- `"name"`: player name
- `"score"`: player score
- `"medal"`: "gold" for rank 1, "silver" for rank 2, "bronze" for rank 3, None otherwise

```python
# Example:
players = [("Alice", 100), ("Bob", 85), ("Charlie", 100), ("Diana", 90), ("Eve", 85)]
result = rank_players(players)
# result should be:
# [{"rank": 1, "name": "Alice", "score": 100, "medal": "gold"},
#  {"rank": 1, "name": "Charlie", "score": 100, "medal": "gold"},
#  {"rank": 3, "name": "Diana", "score": 90, "medal": "bronze"},
#  {"rank": 4, "name": "Bob", "score": 85, "medal": None},
#  {"rank": 4, "name": "Eve", "score": 85, "medal": None}]
```

```python
# Your code here
```

---

## Exercise 13: Nested Data Extractor

Write a function `extract_values(data, key)` that searches a nested structure (dict/list combinations) and returns a list of all values associated with the given key, at any depth level.

```python
# Example:
data = {
    "name": "Company",
    "departments": [
        {"name": "Engineering", "employees": [{"name": "Alice"}, {"name": "Bob"}]},
        {"name": "Marketing", "employees": [{"name": "Charlie"}]}
    ],
    "ceo": {"name": "Diana"}
}

result = extract_values(data, "name")
# result should be: ["Company", "Engineering", "Alice", "Bob", "Marketing", "Charlie", "Diana"]
```

```python
# Your code here
```

---

## Exercise 14: Caesar Cipher

Write two functions:
1. `encrypt(text, shift)` - encrypts text by shifting each letter by `shift` positions
2. `decrypt(text, shift)` - decrypts text by reversing the shift

Only shift letters (a-z, A-Z). Preserve case and leave other characters unchanged. Handle shifts > 26 and negative shifts.

```python
# Example:
encrypt("Hello, World!", 3)   # "Khoor, Zruog!"
decrypt("Khoor, Zruog!", 3)   # "Hello, World!"
encrypt("xyz", 3)              # "abc" (wraps around)
```

```python
# Your code here
```

---

## Exercise 15: Transaction Analyzer

Write a function `analyze_transactions(transactions)` that takes a list of dictionaries with keys `"type"` ("credit" or "debit"), `"amount"`, and `"category"`, and returns:
- `"total_credits"`: sum of all credits
- `"total_debits"`: sum of all debits
- `"balance"`: credits - debits
- `"by_category"`: dict mapping category to net amount (credits positive, debits negative)
- `"largest_transaction"`: the transaction dict with highest absolute amount

```python
# Example:
transactions = [
    {"type": "credit", "amount": 1000, "category": "salary"},
    {"type": "debit", "amount": 50, "category": "food"},
    {"type": "debit", "amount": 200, "category": "utilities"},
    {"type": "credit", "amount": 100, "category": "refund"},
    {"type": "debit", "amount": 75, "category": "food"}
]
result = analyze_transactions(transactions)
# result["balance"] should be: 775
# result["by_category"] should be: {"salary": 1000, "food": -125, "utilities": -200, "refund": 100}
```

```python
# Your code here
```

---

## Exercise 16: Pattern Generator

Write a function `generate_pattern(n, pattern_type)` that generates string patterns:
- `"triangle"`: right-angled triangle of stars
- `"square"`: hollow square of stars
- `"diamond"`: diamond shape of stars

Return the pattern as a single string with newlines.

```python
# Example:
print(generate_pattern(4, "triangle"))
# *
# **
# ***
# ****

print(generate_pattern(4, "square"))
# ****
# *  *
# *  *
# ****

print(generate_pattern(5, "diamond"))
#   *
#  ***
# *****
#  ***
#   *
```

```python
# Your code here
```

---

## Exercise 17: Duplicate Finder

Write a function `find_duplicates(data)` that takes a list and returns a dictionary with:
- `"duplicates"`: list of items that appear more than once
- `"counts"`: dict mapping each duplicate to its count
- `"unique"`: list of items that appear exactly once
- `"positions"`: dict mapping each duplicate to list of its indices

```python
# Example:
data = ["a", "b", "a", "c", "b", "a", "d"]
result = find_duplicates(data)
# result["duplicates"] should be: ["a", "b"]
# result["counts"] should be: {"a": 3, "b": 2}
# result["unique"] should be: ["c", "d"]
# result["positions"] should be: {"a": [0, 2, 5], "b": [1, 4]}
```

```python
# Your code here
```

---

## Exercise 18: Temperature Converter

Write a function `convert_temperatures(temps, from_unit, to_unit)` that converts a list of temperatures between Celsius (C), Fahrenheit (F), and Kelvin (K).

Formulas:
- C to F: (C * 9/5) + 32
- F to C: (F - 32) * 5/9
- C to K: C + 273.15
- K to C: K - 273.15

Return a list of converted temperatures rounded to 2 decimals. If units are the same, return the original list.

```python
# Example:
convert_temperatures([0, 100, 37], "C", "F")    # [32.0, 212.0, 98.6]
convert_temperatures([32, 212], "F", "C")       # [0.0, 100.0]
convert_temperatures([0, 100], "C", "K")        # [273.15, 373.15]
```

```python
# Your code here
```

---

## Exercise 19: Anagram Grouper

Write a function `group_anagrams(words)` that takes a list of words and returns a list of lists, where each inner list contains words that are anagrams of each other. Words should be grouped case-insensitively, but preserve original casing in output.

```python
# Example:
words = ["eat", "tea", "tan", "ate", "nat", "bat", "TAE", "Listen", "Silent"]
result = group_anagrams(words)
# result should be (order may vary):
# [["eat", "tea", "ate", "TAE"], ["tan", "nat"], ["bat"], ["Listen", "Silent"]]
```

```python
# Your code here
```

---

## Exercise 20: Mini Database

Create a class-like structure using a dictionary and functions to simulate a simple database. Implement these functions:

1. `create_table(db, table_name, columns)` - creates a new table with specified columns
2. `insert(db, table_name, record)` - inserts a record (dict) into the table
3. `select(db, table_name, condition=None)` - returns records matching condition (a function), or all if None
4. `update(db, table_name, condition, updates)` - updates records matching condition with new values
5. `delete(db, table_name, condition)` - deletes records matching condition

All functions should modify/return the db dictionary appropriately.

```python
# Example:
db = {}
create_table(db, "users", ["id", "name", "age"])
insert(db, "users", {"id": 1, "name": "Alice", "age": 30})
insert(db, "users", {"id": 2, "name": "Bob", "age": 25})
insert(db, "users", {"id": 3, "name": "Charlie", "age": 35})

# Select all users
select(db, "users")  # Returns all 3 records

# Select users older than 28
select(db, "users", lambda r: r["age"] > 28)  # Returns Alice and Charlie

# Update Bob's age
update(db, "users", lambda r: r["name"] == "Bob", {"age": 26})

# Delete users younger than 30
delete(db, "users", lambda r: r["age"] < 30)
```

```python
# Your code here
```

---

## Good Luck!

Remember to:
- Test your functions with the provided examples
- Handle edge cases (empty inputs, invalid data)
- Write clean, readable code
- Use appropriate data structures for each problem
