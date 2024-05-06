# Python notes

1. Ints and Floats
  - Division with ints returns a float, such as 20 divided by 4 giving us 5.0. Python automatically returns a float to accommodate non-whole numbers. Adding a float to an int or multiplying or using exponents with both also returns a float.
  - Suppose we have 256.0 and want to convert it back to an int. We can use the int class, not function, to do this. Although it looks like a function, int is a built-in class in Python, along with other types like strings, floats, and lists. When we convert from one type to another, such as float to int, we call it casting.
  - Casting is straightforward, but it can be tricky when dealing with values like 8.9, which casts to 8, not 9.
  - Python doesn't round when casting floats to ints, it merely removes the decimal part.
  - To round a float to the nearest int, we can use the round function. We can also specify how many decimal places to round to, such as rounding 4.67 to 5.
  - One pitfall of floats is that they are approximations, which can result in rounding errors. For instance, 1.2 minus 1.0 equals 0.19999999999999996 instead of 0.2.
  - Floats are stored as binary ones and zeros in memory, and due to limited memory, Python makes approximations, leading to these rounding errors.
  - Using the round function can mitigate this issue.

2. Alternative Number Types
   - If you pass a number as a string, the int class will convert it to an integer.
   - For example, "100" becomes the integer 100.
   -  But what's really neat is that if you pass a second argument as a number, it will convert the first argument from that base to base 10. For instance, "100" in base 2 is equal to 4 in base 10.
   -  To use the decimal module, you need to import the decimal class and the getcontext function at the top of your code. The getcontext function returns a context object that holds global settings for using the decimal class.

3. Booleans
   - Python easily casts integers to booleans - 1 is true and 0 is false
   - What about strings? Boolean true is true, of course, and anything other than an empty string is also true. So even the string "false" is true. The only false string is an empty one, but be careful not to accidentally have a space in there.
   - We can also cast data structures to booleans. An empty list or dictionary is false, but anything inside is true. When Python returns a non-value from a function, it is cast to false.

4. Strings
   - Python has numerous tools to analyze and construct strings, and one of the most useful is slicing. Slicing refers to taking a portion of a string and returning it.
   - For example, if we have the string "My name is Iron-Man," we can get the first character by using name[0], since programmers start counting from zero.
   - We can also get the second character with name[1]. If we want to get the first seven characters of the string, we can use the syntax name[0:7], which gets the characters between zero and index seven, but not including the space after "name."
   - If we want to get all the characters from index 11 to the end of the string, we can use the syntax name[11:], leaving the end of the string unspecified.
   - Python has a few ways to create strings, including string concatenation and f-strings. F-strings allow us to insert variables or expressions inside curly braces in a string. We can also do rounding and number formatting with f-strings. The format function is similar to f-strings and was used in versions of Python prior to 3.6.
   - Python has a handy feature for creating multi-line strings by using triple quotes. If we need to include literal triple quotes in the string, we can escape them with a backslash.

5. Bytes
   - When Python loads that data, it knows what type it is - string, int, class, etc. But sometimes all you want is raw data, like a random sequence of ones and zeros. That's where the bytes object comes in.
   - It's just a sequence of data and Python doesn't need to know anything else about it. The bytes object is commonly used for streaming files or transmitting texts without knowing the encoding.
   - Bytes objects are immutable, like tuples, but you can use a byte array if you need to modify the data. You can treat a byte array like a string and modify specific byte values using slice notation. You can use the int library to convert hexadecimal values, like a shrugging emoji, back to bytes. And that's how to find, detect, use, and modify bytes in Python.
