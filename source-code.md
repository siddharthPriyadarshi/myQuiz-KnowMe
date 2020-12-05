# Source Code
***

```
var readlineSync = require("readline-sync");
const chalk = require('chalk');

var userName = readlineSync.question("Enter your name: ");
console.log("\nWelcome ",userName," to my Quiz\nLets chek your friendship power \n");
console.log("Rules:\n1. There are 7 questions.\n2. 1 point will be rewarded for every correct answer\n3. No minus marking\n4.Use valid credentials");

var score = 0; //default value of score
var highestScore=3;
var questions=[ {
  question: "What is my name? ",
  answer:"sid"
},
{
  question: "What is my age? ",
  answer: "20"
},
{
  question: "What is my fav color ? ",
  answer:"black"
},
{
  question: "Who is my fav Bollywood Actor ? ",
  answer: "Hrithik Roshan"
},
{
  question: "Which is my fav food ? ",
  answer: "paneer"
},
{
  question: "Which is my fav sub ? ",
  answer: "computer"
},
{
  question: "Who is my favourite super hero ? ",
  answer: "superman"
}]

for(var i=0; i<questions.length; i++) {
  var userAns = readlineSync.question(questions[i].question)
  console.log()
  if (userAns === questions[i].answer) {
    score = score +1;
    console.log("You are right!\nYour score: ",score);

  }
  else {
    console.log("You are wrong!");
  }
}

console.log("\nThanks for playing\n\nYour final score: ",score);
if (score > highestScore) {
  console.log("Congratulations! You have beaten the highest scorer.")
}
console.log("Hihgest Score   :",highestScore);

console.log("** If you have beaten the highest score then dm the screenshot to let it update!")
```
