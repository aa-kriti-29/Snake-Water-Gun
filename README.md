# Snake-Water-Gun
Snake-Water-Gun game.
import random
print('Welcome to Snake-Water-Gun game!!! ')
print('Instructions:\n 1. You will get 10 chances. \n 2. If your total wins are more you will be declared as winner else not.\n 3.To exist in between '
      'just press E or Exit')
wins_comp=0
wins_user=0
lst=['snake','water','gun']
for i in range(10):
    choice_user = input('Choose: snake/water/gun ')
    choice_comp=random.choice(lst)
    if(choice_user=="E" or choice_user=="Exit"):
        break
    elif(choice_comp=="snake" and choice_user=="snake"):
        print('Same choice')
    elif (choice_comp == "snake" and choice_user== "gun"):
        print('You win this round.')
        wins_user+=1
    elif (choice_comp == "snake" and choice_comp == "water"):
        print('You lose this round.')
        wins_comp+=1
    elif (choice_comp == "water" and choice_comp == "snake"):
        print('You win this round')
        wins_user+=1
    elif (choice_comp == "water" and choice_comp == "water"):
        print('Same choice')
    elif (choice_comp == "water" and choice_comp == "gun"):
        print('You lose this round.')
        wins_comp+=1
    elif (choice_comp == "gun" and choice_comp == "snake"):
        print('You lose this round.')
        wins_comp+=1
    elif (choice_comp == "gun" and choice_comp == "water"):
        print('You win this round')
        wins_user+=1
    elif (choice_comp == "gun" and choice_comp == "gun"):
        print('Same choice')
    else:
        print('Invalid Choice')

if(wins_comp>wins_user):
    print('YOU LOSE \n Better luck next time! ')
elif(wins_user>wins_comp):
    print('You WIN!!! \n Congratulations!!')
else:
    print('Tie!!!')

