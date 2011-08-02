# A. Switching to an on-disk database
0. Make sure you have a local database like MySQL installed. Create a database and an account for purposes of this workshop.
1. Modify the connection parameters in `grails-app/conf/DataConfig.groovy` for the `development` environment to point to an on-disk database. Be sure to get url, driverClassName, username, and password all correct.
2. Change `dbCreate` to `update` in `DataConfig.groovy`. Be able to explain what all three values mean, and what it means to omit `dbCreate` from the configuration entirely.
3. Be sure your on-disk database is set up to respond to the URL, username, and password you have specified.
4. Be sure the JDBC driver for your on-disk database is in the Grails build. Look at `grails-app/conf/BuildConfig.groovy` for this.
  HINT: Uncomment the `mavenCentral()` and runtime dependency lines.
5. Re-run the app and look in the database for the auto-generated tables.
6. Create some Products and Issues and check the database for the new records.
