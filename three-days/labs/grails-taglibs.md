# A. Creating Custom Tags
1. Create a taglib class with `grails create-tag-lib org.grails.Security`
2. Create a tag called `welcome`.  This tag should say "Welcome, ${user.name}" if the user is logged in, and provide a link to the login page if the user is not logged in. (HINT: you can determine if the user is logged in by checking the `session` for the `user` object.)
3. Use the <g:welcome /> tag in the `layouts/main.gsp` layout.
4. Create a tag called `logout`. This should render a link to the logout page if the user is logged in, and render nothing if the user is logged in. Use this tag in the main layout also. HINT: to render a link, call the `link()` method, which behaves exactly like `<g:link />`.
5. EXTRA CREDIT: change the namespace of the taglib to `m33`.
6. EXTRA CREDIT: instead of rendering the "Welcome, " text inside the tag implementation, pass that text into the tag as an attribute. Remember, taglib closures can accept two parameters: one is a map of attributes, the other is tag body text.
