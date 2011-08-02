# A. Reading a File
1. Write a Groovy script to read the included file, people.csv
  HINT: new File('people.csv').eachLine { line -> // do something }
2. Write a method to parse a line of CSV content into a list of fields
  HINT: String.split(',')
  CRAZY HINT: (line =~ /\"([^\"]+?)\",?|([^,]+),?|,/).collect { it[0] }
3. Parse `people.csv` into a list (lines) of lists (fields)
4. Enhance this parser to look for the first row of the file (the field names)
EXTRA CREDIT: Enhance the file reader to create a list (lines) of maps (field names and values)
REALLY EXTRA CREDIT: Sort the line map by the order of the fields in the file
SUPEREROGATORY CREDIT: use metaprogramming to add parse methods to the String and File classes, so they can directly parse CSV files and lines in a single method call

# B. Writing a file
1. Split the list in the previous exercise into one list of records for men and one for women
2. Write each list to a CSV file of its own
  HINT: File.withPrintWriter { ... }

# C. Converting to XML
1. Iterate over the list you created in exercise A and emit an XML file from it. Convert the CSV file field names into XML elements in whatever way makes sense to you.
  HINT: Use a heredoc string to create the XML for each line of the file
  HINT: If you don't have a map of field names to values, just rely on field order
