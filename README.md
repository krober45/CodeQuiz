# Javascript Code Quiz
* A quiz built on Javascript. Link to deployed site (via GitHub pages): 

## What it does

* This quiz is comprised of 5 questions. It is a timed quiz. If you get a question wrong, you lose 10 seconds off the timer. Your score at the end is how many seconds are left on the timer. You can submit your initials and this is saved to the high scores page.

## Technologies Used

* I used the framework Bootstrap to create my NavBar and all the cards and buttons. On top of this I used plain vanilla Javascript to add functionality.

## How I built it

* The HTML and CSS are built on the Bootstrap framework. I used their compenents Navbar, Buttons, Card, and Forms.

* I start my Javascript with an array of objects, each object representing a question, possible answers, and the correct answer. The correct answer was a string that matched the ID of the button element associate with it.

* Next I grabbed all the necessary elements from the DOM (buttons and forms)

* The quiz begins with a Welcome page that explains the rules. When the Start Quiz button is pressed it runs a function that clears the screen, starts the timer, and renders the Quiz Question page by starting a Quiz Question Function.

* The Quiz Question Function displays the first object in my array of questions. When a user clicks an answer button, it checks the button ID (e.g 'answer1') against the answer key in the corresponding object. The answer buttons are disable at this point, the Next Question button appears, and a message appears (either "Correct Answer!" or "Wrong Answer!"). Clicking the Next question button moves us on to the next question.

* Clicking the Next Question button for the final question in the array does multiple things. First it grabs the timer value (users score) then it clears the screen and renders the High Score submission page.

* The High Score submission page shows the users score (the timer value) and has a form for the user to input initials. When the user clicks submit it saves the initials into an array. Now the users initials and the high score are in separate arrays at the same index. This page is cleared and the High Score page is shown.

* The High Score page shows all the high scores and initials saved in Localstorage. The options on this page are retaking that quiz (which is linked to a function that just refreshes the page) or you can clear the high scores which clears out localStorage.

## GIF of it in action

![Javascript Quiz] (./Javascript_Quiz.gif)


 * BUG: Currently you can put nothing into the initials submit field, and it will just show the high score without initials on the High Score page. Add an if statement that forces users to input text.


