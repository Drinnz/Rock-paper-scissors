# Rock-Paper-Scissor

This is project proposed by The Odin Project.
function getComputChoice() {
    let j = 0;
    let choice;
    let odd = Math.floor(Math.random() * 100) + 1;
    if (odd >= 0 && odd <= 33) {
        choice = "Rock";
    } else if (odd >= 34 && odd <= 67) {
        choice = "Paper";
    } else choice = "Scissors";

    return choice;
}

function gameRound() {
    playerSelection = prompt("What is your move?", "");
    computerSelection = getComputChoice();

    playerSelection = playerSelection.toUpperCase();
    computerSelection = computerSelection.toUpperCase();
    let gameResult ="";
    console.log(computerSelection);
    if (playerSelection === "ROCK" && computerSelection === "SCISSORS") {
        gameResult = "You win, Rock beats Scissors.";
       
    } else if (playerSelection === "SCISSORS" && computerSelection === "ROCK") {
        gameResult = "You lost, Rock beats Scissors";
       
    } else if (playerSelection === "PAPER" && computerSelection === "ROCK") {
        gameResult = "You Win, Paper beats Rock";
       
    } else if (playerSelection === "PAPER" && computerSelection === "SCISSORS") {
        gameResult = "You lost, scissors beats paper";
       
    } else if (playerSelection === "SCISSORS" && computerSelection === "PAPER") {
        gameResult = "You Win, Scissors beats Paper";
    
    } else if (playerSelection === "ROCK" && computerSelection === "PAPER") {
        gameResult = "You Lost, Paper beats Rock";

    } else if(playerSelection===computerSelection){
        gameResult = "Draw";

    }
    return gameResult;
}

function game(){
    let l = 0;
    let w = 0;
    let d = 0;
    let result = "";
    for(let i=0;i<5;i++){
    result = gameRound();
    if(result==="Draw"){
        w++;
    }
}
    return w;
}


//const playerSelection = prompt("What is your move?", "");
//const computerSelection = getComputChoice();


console.log(game());

