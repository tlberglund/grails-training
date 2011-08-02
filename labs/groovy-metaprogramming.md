# A. Introspection of existing classes
1. List all of the methods supported by the String class
2. List all of the properties of the Class class
3. Find a method in the String class whose name is codePointAt
4. Determine the class of the object returned by that find() call.
5. List the properties and methods of that class.
  
# B. Adding a method to String
1. Add a reverse() method to String that returns the characters of the string in reverse.
  HINT: delegate

# C. Using methodMissing
1. Create a class with methods called foo() and bar(), each of which prints out a distinct message.
2. Implement a methodMissing method that prints the name and arguments of the invoked method.
3. If the method name ends with Monkey, permanently add a method to the metaClass that prints the name of the method followed by a few exclamation points.
  HINT: name.endsWith("Monkey")
4. EXTRA CREDIT: put some debug code in methodMissing and in your dynamically created methods to indicate when they are called. Call the unleashMonkey() method several times. Observe the debug output.
