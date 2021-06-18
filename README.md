# Python_Game

import random

def gameIntro():  //The games introduction
  print("You have landed on the ")
  print(" planet Wefhrui\n")
  print("You exit the spaceship and")
  print("look to the left and see")
  print("trees. You look to the right")
  print("and see water\n\n")
  
  print("Do you want to go left or right?") //Asks player a question
  
  choice = input("Enter left or right") //Player can answer with left or right
  
  if choice == "left" or choice == "Left": //If player says left, take them to the trees
    trees()
   elif choice == "right" or choice == "Right": //If player says right, take them to the water
    water()
    
def trees():
  print("You enter the trees and meet a giant monster\n") //Asks if you want to fight the monster or talk
  print("Do you want to fight the monster or ")
  print("attempt to talk with him?\n\n")
  
  choice = input("Enter fight or talk")
  
  if choice == "fight" or choice == "Fight": //If you fight the monster you die
    youDie()
    elif choice == "talk" or choice == "Talk": //Lets you talk to the monster
      talk()

def youDie(): //Tells the player they died
  print("You made a bad choice...\n")
  print("You are dead.\n\n")
  
def talk(): //Tells player to guess a number between 1 and 10
  print("The monster says for you to guess the number\n")
  print("between 1 and 10 that he is thinking of.\n")
  print("If you guess right, you may pass\n")
  
  monsterNumber = random.randint(1, 10) //The monsters number will be a random number between 1 and 10
  userGuess = int(input("Enter a number between 1 and 10")) //Player can guess between 1 and 10
  
  if userGuess == monsterNumber: //If player guessed right they live, if not they die
    print("You may pass the monster and enter the trees\n")
  else:
    youDie()
    
def water(): //Asks player to ride a boat or swim
  print("You approach the water and see a boat")
  print("Do you want to get in the boat to ")
  print("cross the water or do you want to swim?")
  
  choice = input("Enter boat or swim") //Player can pick boat or swim
  
  if choice == "boat" or choice == "Boat": //Asks player to take gold
    print("You look and the boat and see ")
    print("10 pieces of gold. How many pieces")
    print("of gold do you take\n")
    
    takeGold = int(input("Enter number of pieces")) //Player can say how much gold they take
    
    boatGold(takeGold)
   elif choice == "swim or choice == "Swim": //If you swim you make it, if not you die
    levelSwim = swim()
    if levelSwim == "yes" or levelSwim == "Yes":
      print("You start across the water")
    elif levelSwim == "no" or "No":
      youDie()
      
def boatGold(takeGold): //If the player took gold they die
  if takeGold > 0:
    youDie()
  else:
    print("Good for you for not stealing\n")
    print("You set off in the boat across the water")
    
def swim(): //asks player if they can swim
  print("You decide to swim across the water\n")
  print("Do you know how to swim? Yes or No")
  
  truth = input("Enter yes or no")
  
  return truth
  
gameIntro() //restart game
    
    
