# Contact Form

[solution step 1 AT](./step1.md)
[solution step 2 AT](./step2.md)
[see live version on vercel](https://hackerrank-react-contact-form.vercel.app/)

You need to create a simple React application called "Contact Form" that collects user information and displays it below the form upon submission. This task will help you practice handling form inputs, validation, and conditional rendering in React.

Detailed Requirements
1. Form Structure:

    The form should have the following fields:
        Name: Text input for the user's name.
        Email: Text input for the user's email address.
        Message: Textarea for the user's message.

2. Form Submission:

    There should be a "Submit" button to submit the form.

3. Form Validation:

    Validate that none of the fields are empty upon submission.
    If any field is empty, display an error message: "All fields are required." The form should not be submitted.

4. Displaying Submitted Data:

    If the form is successfully submitted, display the entered information below the form.
    Clear the input fields after a successful submission.


Sample Interaction

Initial State

    The form is displayed with empty fields.
    No submitted information or error messages are shown.

User Action 1

    User fills in all fields (Name: "John Doe", Email: "john@example.com", Message: "Hello there!").
    User clicks the "Submit" button.
    The entered information ("John Doe", "john@example.com", "Hello there!") is displayed below the form.
    The input fields are cleared.

User Action 2

    User fills in some fields and leaves others empty.
    User clicks the "Submit" button.
    No information is displayed.
    An error message "All fields are required." is shown.

## [HackerRank Web Page Challenge Requirements](https://www.hackerrank.com/challenges/react-contact-form/)
![screenshot](./public/Screenshot.jpg)