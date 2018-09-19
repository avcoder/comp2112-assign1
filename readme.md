# Assignment 1 - Webmail Inbox of Games

Using plain Javascript, this assignment requires you to use template literals, access/change the DOM, event handling and object/arrays methods. Your mark counts for 15% of your final grade.

Due Date: Friday,Oct. 6 @ 11:59 pm

Submission Requirements via Blackboard:

- a single .zip file containing all your pages
- a link to your github repository where this assignment is also stored

All work must be your own. Failure to submit an independent assignment will result in a grade of zero.

## Purpose:

In this assignment you will take an existing, static email-like HTML template, and make it dynamic via Javascript.
![Screenshot of Sample Assignment](Capture.JPG)

## What you'll need:

- HTML/CSS framework for creating webmail https://purecss.io/layouts/email/
- An array of objects that lists game information taken from: https://archive.org/details/softwarelibrary_msdos_games

```
let games = [
    {'publisher' : 'Namco', 'avatar' : 'https://archive.org/services/img/msdos_Pac-Man_1983', 'subject' : 'Pac-Man', 'body' : 'Pac-Man stars a little, yellow dot-muncher who works his way around to clear a maze of the dots.', 'date' : '1983', 'ifrmSrc' : 'https://archive.org/embed/msdos_Pac-Man_1983'},
    {'publisher' : 'Broderbund', 'avatar' : 'https://archive.org/services/img/msdos_Where_in_the_World_is_Carmen_Sandiego_1985', 'subject' : 'Where in the World is Carmen Sandiego', 'body' : 'Capture the thief that stole the artifact using clues dealing with your knowledge of geography.', 'date' : '1985', 'ifrmSrc' : 'https://archive.org/embed/msdos_Where_in_the_World_is_Carmen_Sandiego_1985'},
    {'publisher' : 'Ingenuity', 'avatar' : 'https://archive.org/services/img/msdos_Crosscountry_Canada_1991', 'subject' : 'Crosscountry Canada', 'body' : 'Drive an 18-wheel truck picking up and delivering a variety of commodities with typed-in commands.', 'date' : '1991', 'ifrmSrc' : 'https://archive.org/embed/msdos_Crosscountry_Canada_1991'},

];
```

## Application Requirements:

1. Display a set of games in the style of your student webmail but instead of emails, using game information--game title, producer, avatar picture of game, iframe of url
   1. Use of template literals to eventually output HTML code and each game object’s info for each entry
   1. Use of map (or other looping method) on template literal to display all entries
   1. Putting your HTML code in the appropriate place in the DOM via innerHTML (or similar)
1. Clicking a game in the inbox will add some kind of visual indicator to make it look selected and also, display the game in the main section
   1. addEventListener added for each entry to listen for click, when click happens, adding appropriate CSS class to make it look selected
   1. the upper section of main should show the game title, publisher, year published. In the main section, show the iframe game.
   1. avoid any ‘undefined’ from showing on publisher, year, body, and game title by testing if those fields/keys exist on the object. If it doesn’t, then gracefully output an empty string
1. Clicking on the Compose button will open a form where you to enter data for a new game where upon submit, will add a new entry to the inbox.

   1. Form shows all relevant fields
   1. After data is entered, clicking the Save button will create a new game object whose key/values match the form data, then will be added to your existing array of game objects. View is updated to reflect current state.

   For example, entering the following data should reveal a new game entry in the inbox and an interactive game in the main section.

   ```
   Game Title: Monopoly
   Publisher: VirginGames
   Year Published: 1992
   Description: the classic board game
   Avatar: https://archive.org/services/img/msdos_Monopoly_Deluxe_1992
   iframe URL: https://archive.org/embed/msdos_Monopoly_Deluxe_1992
   ```

1. Clicking delete button will remove entry from inbox. Clicking on the trash link will allow you to view all items that have been deleted. Clicking the inbox link again will return you back to the inbox view
   1. addEventListeners implemented for delete button, trash link, inbox link which updates its current view
   1. Deleting an entry moves game to the trash. While in trash view, clicking Deleted button moves the entry back to inbox.
   1. Deleting an entry changes the text on the Delete button to “Deleted”. While in trash view, cslicking the “Deleted” button will change text to “Delete”
1. Whether you click inbox, or trash, it always displays an accurate, current state of the array of objects
1. Use local storage such that it stores the current state of objects (assume you’ve deleted/added entries) so if the browser refreshes, it does not return back to the view of original state of objects, but rather will return you to the same view you had before refreshing
   1. Use localstorage to set information of the current state of objects whenever a change happens
   1. Use localstorage to get information so that a browser refresh remembers current state of object and does not default back to the original view.
1. Document each section of your script with comments. You do not need to document every single line.

## Evaluation Method

Refer to Word document version in Blackboard to see Evaluation Rubric.

## Conclusion:

In the end, it should function like this: https://youtu.be/re3ZkZQY2bg
