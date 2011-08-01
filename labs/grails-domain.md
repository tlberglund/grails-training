# A. Creating Domain Classes
1. Use the `grails create-domain-class` command to create classes called `org.grails.Speaker` and `org.grails.Conference`
2. Inspect the code created in grails-app/domain
3. Add some properties to each class. Feel free to be creative.
4. Use the `grails create-controller` command to create bare controllers for Speaker and Conference
5. Add the `def scaffold=true` line to each controller. Remove the default index action.
6. Run the app with `grails run-app`. Experiment with the scaffolded UI for each domain object

# B. Switching to an on-disk database
1. Modify the connection parameters in `grails-app/conf/DataConfig.groovy` for the `development` environment to point to an on-disk database. Be sure to get url, driverClassName, username, and password all correct.
2. Change `dbCreate` to `update` in `DataConfig.groovy`
3. Be sure your on-disk database is set up to respond to the URL, username, and password you have specified.
4. Be sure the JDBC driver for your on-disk database is in the Grails build. Look at `grails-app/conf/BuildConfig.groovy` for this.
  HINT: Uncomment the `mavenCentral()` and runtime dependency lines.
5. Re-run the app and look in the database for the auto-generated tables.
6. Create some Speakers and Conferences and check the database for the new records.

