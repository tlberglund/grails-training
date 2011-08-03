# A. Exploring Validation Errors
1. Using the `grails console`, create an instance of an `Issue` or a `Product` which will fail validation.
2. Call the `.validate()` method on that instance and inspect the return value.
3. If it is false, look at the `.errors.allErrors` collection. 
4. Iterate over this collection.
5. Determine the run-time type of the objects it returns.
6. Introspect those objects to see what they are telling you about the failure.

# B. Using GORM Dynamic Finders
1. Create a new action in `IssueController` called `filtered_issues`.
2. The action should process two request parameters: `severity` and `userId`. NOTE: your `Issue` schema needs to support both of these fields.
3. Perform a dynamic finder query on the `Issue` class to find all records matching that severity and UserId.
  HINT: Issue.findAllBySeverityAndUserId() is not correct.
  HINT: User.get() may help.
4. Render a list of issues containing only the results of the filtered query.
5. Rewrite the query to use the `Issue.where()` syntax.
6. EXTRA CREDIT: render the output as JSON using render(contentType: 'text/json') { ... }

# C. Adding to Collections (and using HTTP verbs)
1. Create a new action in `IssueController` called `resolve`.
2. The action should find the Issue specified in the URL (e.g., http://.../issue/resolve/43).
3. The action should mark the issue as resolved.
  NOTE: you may need to modify your domain to give issues a `resolved` flag, or some kind of issue state. You are free to approach this however you like.
4. The action should create a new comment and add it to the issue. The comment can say something like "This issue was resolved at "Wed Aug 03 07:23:55 EDT 2011." NOTE: use the issue.addToComments() method.
5. Since this action modifies the state of the application, make sure it is only accessible through the POST verb.
6. Verify that you can't access the action with a GET
7. Put a button in the `views/issues/show.gsp` view to mark an issue as resolved. This form code may help:
            <g:form action='resolve' method='post'>
              <g:hiddenField name="id" value="${issueInstance?.id}" />
              <g:submitButton name="resolve" value="Resolve Issue" />
            </g:form>
8. EXTRA CREDIT: modify the `list` action in the `issue` controller to show only active issues.


# D. Criteria Builder
1. Create a new action in `ProductController` called `distressedProducts`
2. The action should render a list of active products which have issues of severity greater than 7. Use the `Product.withCriteria { ... }` method to express this query. (You may need to add an `active` field.)
3. You should be able to re-use the `views/product/list.gsp` page, passing in this updated model.
