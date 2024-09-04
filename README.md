# python_lambda_function
python_lambda_function 

Using a Python `lambda` function with `map` allows you to apply a function to each item in an iterable (like a list). Here's how you can use a lambda function with `map` on a list of words.

### Example 1: Convert Words to Uppercase
Suppose you have a list of words, and you want to convert each word to uppercase using a lambda function and `map`.

```python
words = ["apple", "banana", "cherry"]

# Use map with a lambda function to convert each word to uppercase
uppercase_words = list(map(lambda word: word.upper(), words))

print(uppercase_words)  # Output: ['APPLE', 'BANANA', 'CHERRY']
```

### Example 2: Find the Length of Each Word
You can also use `map` with a lambda function to calculate the length of each word in the list.

```python
words = ["apple", "banana", "cherry"]

# Use map with a lambda function to find the length of each word
word_lengths = list(map(lambda word: len(word), words))

print(word_lengths)  # Output: [5, 6, 6]
```

### Example 3: Add a Prefix to Each Word
Let's say you want to add a prefix to each word in the list.

```python
words = ["apple", "banana", "cherry"]

# Use map with a lambda function to add a prefix "fruit-" to each word
prefixed_words = list(map(lambda word: "fruit-" + word, words))

print(prefixed_words)  # Output: ['fruit-apple', 'fruit-banana', 'fruit-cherry']
```

### Example 4: Filter Words Based on Length (Using `map` and `filter`)
You can also combine `map` with `filter` to filter and transform words. For example, to keep only words with more than 5 letters and convert them to uppercase:

```python
words = ["apple", "banana", "cherry", "fig"]

# Use filter to keep words with more than 5 letters
filtered_words = filter(lambda word: len(word) > 5, words)

# Use map with a lambda function to convert the filtered words to uppercase
uppercase_filtered_words = list(map(lambda word: word.upper(), filtered_words))

print(uppercase_filtered_words)  # Output: ['BANANA', 'CHERRY']
```

### Summary:
- `map(lambda word: ..., words)` applies the lambda function to each item in the `words` list.
- You can perform various operations like transforming, filtering, and combining data using lambda functions with `map`.


Using Recursion as an Alternative

You can mimic the behavior of a while loop in a recursive lambda function:

```python

repeat = lambda x: x if x >= 100 else repeat(x * 2)
result = repeat(1)
print(result)  # Output will be 128
```

In the above recursive lambda, the function repeat keeps calling itself, doubling the value until the condition (x >= 100) is met.
Limitation

Be careful with recursion in Python, as it can lead to a stack overflow if the recursion depth is too large. Python has a recursion limit (usually 1000 calls deep), which you can adjust but it’s generally better to use a loop for such tasks.
