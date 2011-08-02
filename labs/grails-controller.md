# A. Static scaffolding
1. Run `grails generate-all org.grails.Product`. If prompted to overwrite any files, answer yes.
2. Explore the code generated in the controllers and views directories.
3. Add a field to org.grails.Product and re-run the application. Note that the scaffolding does not change.
4. Run `grails generate-views org.grails.Product`. Note the updated scaffolding.
5. Generate static scaffolding for `org.grails.Issue` and any other domain classes you've created.
5. EXTRA CREDIT: run the `grails install-templates` command, then look in the `src` directory for the template code. Try modifying some of the markup (don't spend much time on it, but try to make a visible change) then re-generate a controller. Note the difference in the view.

# B. Reorganizing GSP templates
1. Extract the markup for the data entry controls in `views/issue/edit.gsp` and put them in a file called `_form.gsp`.
2. Replace that markup in `edit.gsp` with the appropriate `<g: render />` tag. Refresh the page to make sure it still looks right.
3. Do the same with the row rendering markup in `views/issue/list.gsp` (calling the template `_issue_summary.gsp`) and the detail display in `views/issue/show.gsp` (calling the template `_issue_detail.gsp`').
4. Do the same with the GSPs for the `Product` domain class.
5. PALTRY EXTRA CREDIT: do the same with any other domain classes you've created. Feel free to do any other refactoring of the GSPs you want to do, using page templates liberally.

# C. Adding a controller action
1. Add an action to `IssueController` that returns a static string. How does this action interact with page templates?
2. Add another action to `IssueController` that returns an HTML fragment for a single issue. Copy the database query from another action in the scaffolding. The URI should look something like this: `.../issue/show_single/32`.

# D. Redirecting Requests
1. After creating or updating a new `Issue` or `Product`, the UI should redirect to the list view, not the show view. 
