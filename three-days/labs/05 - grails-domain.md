# A. Creating Domain Classes
1. Use the `grails create-domain-class` command to create classes called `org.grails.Issue` and `org.grails.Product`
2. Inspect the code created in grails-app/domain
3. Add some properties to each class. Feel free to be creative.
4. Use the `grails create-controller` command to create bare controllers for Issue and Product
5. Add the `def scaffold=true` line to each controller. Remove the default index action.
6. Run the app with `grails run-app`. Experiment with the scaffolded UI for each domain object.

# B. Bootstrapping test data
1. Open `grails-app/conf/Bootstrap.groovy` and locate the `init` closure.
2. Create a few instances of the Product and Issue classes.
  HINT: new Product(name: 'subversion').save()
3. Start up the application again to verify that your test data exists.

# C. Domain Validation
1. Add some validation rules to your classes. You have defined your own domain metadata up till now, so apply some of these validation rules to the fields you've defined (add new fields to validate if necessary):
  * A string is non-blank
  * A string may be null
  * A number is between an upper and lower bound
  * A string is formatted as a URL
  * A string is formatted as an email
  * A string comes from a list of pre-defined options (might be good for validating the product name)
  * EXTRA CREDIT: If the issue severity is greater than 7, issue name and email may be null; otherwise, they cannot be null.
2. Note the order in which the fields are rendered in the scaffolded "new" view.
3. Rearrange the order of the validation calls in the constraints block.
4. Note the order in which the fields are now rendered in the scaffolded "new" view.


