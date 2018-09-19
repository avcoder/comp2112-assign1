# Assignment 1 - Webmail Inbox of Games

Using plain Javascript, this assignment requires you to use template literals, access/change the DOM, event handling and object/arrays methods. Your mark counts for 15% of your final grade.

Due Date: Friday, Oct. 10 2018 @ 11:59 pm

Submission Requirements via Blackboard:

- a link to your private Github repo
- ensure you invite me as a collaborator to your repo so I can see your code
- a hosted url where you've uploaded your code (Azure or other)

All work must be your own. Failure to submit an independent assignment will result in a grade of zero.

## Purpose:

In this assignment you will take an existing, static email-like HTML template, and make it dynamic via Javascript.

## What you'll need:

- HTML/CSS framework for creating webmail https://purecss.io/layouts/email/
- custom API #1 - build your own API from https://www.mockaroo.com that sends 7 emails
- custom API #2 - build another API from mockaroo that sends only 1 email

## Application Requirements:

1. Display 7 random emails from your custom API#1.
   1. Use of template literals to eventually output HTML code from each email object
   1. Use of map (or other looping method) on template literal to display all entries
   1. Putting your HTML code in the appropriate place in the DOM via innerHTML (or similar)
1. Clicking an email in the inbox will add some kind of visual indicator to make it look selected and also, display the email body, subject, name, date in the main section
   1. addEventListener added for each entry to listen for click, when click happens, adding appropriate CSS class to make it look selected
   1. the upper section of main should show the email title, subject, date. In the main section, show the email body
   1. avoid any ‘undefined’ from showing on any fields by gracefully outputting an empty string
1. Clicking on the Compose button will open a form where you to enter form data for a new email where upon submit, will add a new entry to the inbox (as if you're emailing yourself; get picture from github's avatar_url from api.github.com/users/your-username).

   1. Form shows all relevant fields
   1. After data is entered, clicking the Save button will create a new email object whose key/values match the form data, then will be added to your existing array of emails. View is updated to reflect current state.

1) Clicking delete button will remove currently selected email from inbox. Clicking on the trash link will allow you to view all items that have been deleted. Clicking the inbox link again will return you back to the inbox view
   1. addEventListeners implemented for delete button, trash link, inbox link which updates its current view
   1. Deleting an email moves it to the trash. While in trash view, clicking Deleted button undo's the delete and moves the email back to inbox.
   1. Deleting an entry changes the text on the Delete button to “Deleted”. While in trash view, clicking the “Deleted” button will change text to “Delete”
1) Whether you click inbox, or trash, it always displays an accurate, current state of the array of objects
1) Use local storage such that it stores the current state of objects (assume you’ve deleted/added entries) so if the browser refreshes, it does not return back to the view of original state of objects, but rather will return you to the same view you had before refreshing
   1. Use localstorage to set information of the current state of objects whenever a change happens
   1. Use localstorage to get information so that a browser refresh remembers current state of object and does not default back to the original view.
1) Document each section of your script with comments. You do not need to document every single line.

## Evaluation Method

Refer to Word document version in Blackboard to see Evaluation Rubric.

## Conclusion:

In the end, it should function like this: https://youtu.be/re3ZkZQY2bg
