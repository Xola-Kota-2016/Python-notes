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
