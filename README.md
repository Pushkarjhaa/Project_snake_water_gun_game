# snakeWatergunGame_
snake water gun game!
import random

def gameWin(comp, you):
    if comp==you:
        return None

    elif comp=='s':
        if you=='w':
            return False
        elif you== 'g':
            return True
    elif comp=='w':
        if you=='g':
            return False
        elif you=='s':
            return True
    elif comp=='g':
        if you=='s':
            return False
        elif you== 'w':
            return True

print("comp turn: snake(s) water(w) gun(g)?")
randno= random.randint(1, 3)
if randno==1:
    comp ='s'
elif randno==2:
    comp = 'w'
elif randno==3:
    comp = 'g'


you=(input("your turn : snake(s) water(w) gun(g)?:"))
a= gameWin(comp, you)
print(f"computer choose {comp}")
print(f"you choose {you}")

if a==None:
    print("The game is tie ")
elif a:
    print("You win the game")
else:
    print("You loose the game")
