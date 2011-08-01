# A. Basic Closures
1. Write a Groovy script containing a closure assigned to a variable. Have the closure print a message to stdout.
2. Call the closure from inside the script.
3. Create another closure that accepts a parameter. Fill in your own functionality inside the closure.
4. Call this closure several times, passing in different values.
5. Write a method which takes a String and a Closure as parameters. Have the method pass the string to the closure
6. Invoke that method in at least three different ways.

# B. Closure Delegation
1. Inside a Groovy script, create a class called ClosureDelegate that has three properties and two methods. Those methods can do anything, but at the very least they must add objects to a list internal to the class.
2. Outside of that class, create a closure that calls the methods defined inside the class.
3. Call the closure. You should be exceptions for the missing methods.
4. Create an instance of ClosureDelegate, then set the closure's delegate to that object.
5. Run the script again. It should work now.
6. Create methods in the script (outside of any class) with the same name as the methods in ClosureDelegate. Make sure these methods print a different message than the methods in ClosureDelegate.
7. Experiment with setting the resolveStrategy property on your closure to Closure.DELEGATE\_FIRST and Closure.DELEGATE\_ONLY and see what happens.
