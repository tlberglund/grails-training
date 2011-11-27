# A. Basic Lists
1. Write a Groovy script that declares a statically initialized list containing data of your choosing. Print out the list.
2. Experiment with accessing members of the using square bracket indexing.
3. Create sub-lists by using ranges for indexes. Make sure some of the indexes are negative.

# B. List API
1. Create a list of random numbers with the following code:
  
  def random = []
  100.times { random << Math.random() }

2. Iterate over your list using the each() method, printing out each member.
3. Convert your list to percentages using the collect() method. Output should resemble this: 14.16%.
  HINT: sprintf("%02.02f%%", number)

4. Find the average of all the random numbers without writing a loop
5. In one line of code, find the count of all the list items greater than some customizable threshold
6. Group all of the numbers by the digit in the tenths place
7. Sort the numbers in ascending order, then descending order

# C. Basic Maps
1. Write a Groovy script that declares a statically initialized map containing data of your choosing. Print it out.
2. Fetch keys from the map using three different syntaxes.
3. Alter keys in the map using three different syntaxes.
4. Create a sorted map using the sort() method. Remember, the closure you pass in will take two parameters.
5. Use the find() method to search your map for something. The semantics of your find will depend on your test data.
6. Replace the find() call with findAll(). Experiment with altering the search closure.
