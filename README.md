# JavaScript-Projects
//Rock,Paper,Scissors Game java

function getUserChoice() {
  var userInput = prompt('Rock, Paper, or Scissors?');
  userInput = userInput.toLowerCase();
  if (userInput ==='rock' || userInput === 'paper'|| userInput === 'scissors' || 'bomb') {
  return userInput;
  } else {
 console.log('Error!');    
  }  
}
// that is for prompt to delcare user choice. 
function getComputerChoice () {
  var randomNumber = Math.floor(Math.random() *3);
  switch (randomNumber){
    case 0:
      return 'rock';
    case 1:
      return 'paper';
    case 2:
      return 'scissors'; }
}
// set up for the computer to pick a random number then make an action depending on the number. 
function determineWinner (userChoice,computerChoice){

  if (userChoice === computerChoice) {
  return 'the game is a tie!'; 
} 
  if (userChoice === 'rock') {
   if (computerChoice ==='Paper')
  {
    return 'The computer won!';
  } else{
    return 'you won!'; 
  	}
  }
  if (userChoice === 'Paper') {
   if (computerChoice === 'scissors')
  {
    return 'the computer won!';
  } else { 
  return 'you won!';
  }
}

  if (userChoice === 'scissors') {
   if(computerChoice === 'rock')
    {
      return 'the computer won!';
     } else {
       return 'you won!';
    }
    if (userChoice === 'bomb') {
     if (computerChoice === 'scissors')
       return 'WINNER WITH A BOMB';
    } else {
      return 'WINNER WITH A BOMB'; 
    }
  }
}

function playGame (){
  var userChoice =
      getUserChoice();
  var computerChoice =
      getComputerChoice();
  console.log('You threw: ' + userChoice);
  console.log('The computer threw: ' + computerChoice);
  console.log(determineWinner(userChoice, computerChoice));
}

playGame();
