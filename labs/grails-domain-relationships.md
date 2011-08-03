# A. Adding relationships
1. A product has many issues. Reflect this in the domain model.
2. An issue belongs to a single product. Reflect this in the domain model.
3. Issue severity shouldn't be a free-form entry. Create a domain class called Severity and give Issue a many-to-one relationship with it. Be sure to populate Severity in the Bootstrap code.
  NOTE: Many Issues can have a single Severity, the many-to-one relationship does not involve a collection of any kind.
4. Create a domain class for Comments. A comment belongs to an issue, and an issue has many comments.
5. EXTRA CREDIT: think about the constraints of the Severity class. Should two records be able to exist with the same severity level? Address this in the code.
6. EXTRA CREDIT: make sure comments are ordered by time.
  HINT: you can't let hasMany provide the comments property for you
  HINT: try imposing a default ordering on the Comment domain object

# B. Adding a user model
1. Create a User domain class. You can give it whatever fields you want, as long as it has name, username, email, and password.
2. Issues and comments should know what user created them. Establish this relationship.
3. Initialize some user data using the Grails Console.

EXTRA CREDIT: you should never store a password as plain text. One approach to this is to create a passwordHash field that stores a hash of the password, then provide a setPassword method that implements the hash. See the documentation for the GORM transients list. Also see the java.security.MessageDigest class for a way to compute a hash.

