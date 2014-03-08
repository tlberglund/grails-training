# A. Creating a Login Page
1. Without using scaffolding, create a view called `views/security/login.gsp`. The page should contain a form for username and password input, plus a submit button. (You should copy markup from scaffolded pages.)
2. Without using scaffolding, create a controller called `SecurityController`. It should have actions called `login`, `processLogin`, and `logout`. `processLogin` should respond to POST only.
3. The `login` action should simply present the login form.
4. The `processLogin` action should take input from the login form, look up a User object by username and password, and place the user object in the session if the user exists.
5. If no user is found, redirect to the login page and display an appropriate flash message. (HINT: you will need to copy markup from the scaffolding to display a flash message.)
6. The `logout` action should remove the user from the session (either by calling `session.removeAttribute()` or setting `user` to null), then redirect to the application home page.

# B. Securing Other Controllers
1. Create a security filter set with `grails create-filters org.grails.Security`
2. In the before filter, return true iff the controllerName is `security` or if the user is found in the session.
3. Otherwise, redirect to the login page.
4. EXTRA CREDIT: display a flash message when failing authentication.

# C. EXTRA CREDIT: Password Hashing With a Codec
1. Create a class in `grails-app/utils` called `org.grails.SHACodec`. A Grails codec looks like this:
    class SHACodec {
      static encode = { input ->
        // process input, return encoded output
      }
    }
2. Strings in Grails are now enhanced with an .encodeAsSHA() method. Use this to hash passwords in `SecurityController`. Note that you'll have to hash the password content in the database if you have not already. (HINT: grails console would be an easy way to do this.)
