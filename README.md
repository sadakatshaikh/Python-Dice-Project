# Python-Dice-Project
import math
import random
loses=0
score=0
looprun=0
print("_______________________\n")
print("Welcome To Dice Gameπ²")
print("_______________________\n")
while True:
  a=input(">>>Enter Your Guess π€«:  ")
  if a.lower()=='quit':
    if score==0:
      a1="times! π"
    elif score==1:
      a1="time! π₯±"
    elif score==2:
      a1="times! π"
    else:
      a1="times! π€©"
    print("\nThanks for playing the game. You won",score, a1 )
    exit()
  def dice_game(user_guess,loses,score):
    if user_guess>6:
      print("\nπ«π«π«\nEnter a valid guess within the range 1-6\n")
    else:
      print("\nRolling π²...")
      dice_value=random.randint(1,6)
      print("π²"+ "="+str(dice_value))
      if user_guess==dice_value:
        print("Congratulations You won!!! π₯³\n")
        score+=1
      else:
        if loses>0:
          print("You lost again π€ but don't give up keep trying!π€\n")
        else:
          print("You lost π\n")
          loses+=1
    b=[loses,score]
    return b       
  b=dice_game(int(a),loses,score)
  loses=b[0] 
  score=b[1]


