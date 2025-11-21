## Task 1

**Task Type:** Feature Implementation

**Prompt:**
```
Need to implement a Snippet feature, mainly for saving snippets, including information such as title, filename, code, tags, etc.

- Add Snippet Entity class
- Add Snippet Repository class
- Add Snippet Service class
- Create SnippetListView, mainly used to display snippets, including adding new snippets, modifying snippets, deleting snippets, searching snippets
- Add the new SnippetListView to the MenuBar

Please refer to the Task implementation code to complete the Snippet implementation.
```


## Task 2

**Task Type:** Code Modification

**Prompt:**
```
Please add a tags field to the Task class. Tags is a comma-separated string, such as `vip,paid`. After adding the tags field, please modify the TaskListView class to add an input box for the tags field and implement search functionality.
```
            
## Task 3:

**Task Type:** Code Modification
**Prompt:**

```
Add login support for Vaadin application, requiring authentication before accessing the app, with the following requirements:

Create a corresponding account table, including fields such as username, email, roles, password, etc., where passwords use the bcrypt encryption algorithm, and roles include ADMIN and USER
Place account-related code under the org.mvnsearch.account package
Add default data to the account table, such as user and admin accounts
Add a top navigation bar that displays the logged-in user's avatar and username on the right side, and include a logout button
```

## Task 4:

**Task Type:** Code Modification
**Prompt:**

```
Based on the wallet prototype diagram in the excalidraw file, create the corresponding Vaadin View, including the operation for adding expense records.
```