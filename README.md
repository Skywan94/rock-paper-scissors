# rock-paper-scissors
functional rock paper scissors assignment

useful code:

//choices array
const choices = ["rock", "paper", "scissors"];


//for loop
for (let i = 0; i < 5; i++) {}


//picks random value for npc
function getComputerChoice() {
    return Math.floor(Math.random() * choices.length);    
}


//converts string into number to work with array positions
function getPlayerChoice(input) {      
    if (input == "rock") {
      return 0;
    }
    else if (input == "paper") {
      return 1;
    }
    else if (input == "scissors") {
      return 2;
    }
    /*else (alert("Wrong selection!"));*/
}


//returns choice as a string
function computerSelection() {
    return choices[getComputerChoice()];
}
function playerSelection(input) {
    return choices[getPlayerChoice(input)];
}


//win-loss conditions
function playGame(playerSelection, computerSelection) {
    if (playerSelection === "rock" && computerSelection === "scissors" ||
        playerSelection === "paper" && computerSelection === "rock" ||
        playerSelection === "scissors" && computerSelection === "paper") {
          alert("you win!");
        }
    else if (
        playerSelection === "rock" && computerSelection === "paper" ||
        playerSelection === "paper" && computerSelection === "scissors" ||
        playerSelection === "scissors" && computerSelection === "rock") {
           alert("you lose!");
                }
    else (alert("it's a tie!"));
}


