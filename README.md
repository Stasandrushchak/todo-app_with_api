# React Todo App with API

Todo App allows you to add, delete and edit todos to the list:

- hide or disable elements that can't be used at the moment
- focus text fields, so user could start typing without extra clicks
- prevents users from doing the same action twice accidentally (disable controls when action is in progress)
- show spinners on todos immediately to notify the user that action is in progress
- update todos only after successful save to the API (tests expect such behaviour)
- in case of any error show a notification (and hide it after delay)
- clear input values on `success` and preserve and focus on `error`
- text field focused by default;
- if the title is empty show the `Title should not be empty` notification at the bottom;
- trimed the title when checked or saved;
- send a POST request to the API;
- disable the input until receiving a response from the API;
- immediately after sending a request create a todo with `id: 0` and save it to the `tempTodo` variable in the state (NOT to the `todos` array);
- show an independent `TodoItem` after the list if `tempTodo` is not `null`;
- temp TodoItem have the loader;
- in case of success add the todo created by the API to the array;
- in case of an API error showing `Unable to add a todo` notification at the bottom;
- set `tempTodo` to `null` to hide the extra `TodoItem`;
- focus the text field after receiving a response;
- clear the text in case of success;
- keep the text in case of error;
- covered the todo with a loader overlay while waiting for API response;
- the status changed on success;
- show the `Unable to update a todo` notification in case of API error.
- `toggleAll` button have `active` class only if all the todos are completed;
- `toggleAll` click changes its status to the opposite one, and sets this new status to all the todos;
- it work the same as several individual updates of the todos which statuses were actually changed;
- do send requests for the todos that were not changed;

Technoligies that were used in the project:

- typescript;
- fetching data from the server using async function;
- create, update and delete data with the help of methods: GET, POST, PATCH, DELETE;
- custom hook;