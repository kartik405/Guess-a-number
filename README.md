# Guess-a-number
#I am a noobie. I saw a question on guess a number with tracking the amount of tries as optional objective. Suggestions and feedbacks are appreciated

import random
import sys

highest = 9
value = random.randint(1, highest)
b = []
i = 0


print("Guess a number between 1-{}".format(highest))

try:
    userInput = int(input("Please enter a number: "))
except ValueError:
    print("U don't seem to understand English. Please type a number")
    userInput = int(input("Please enter a number: "))


while userInput != b:
    if userInput==0:
        print("You have decide to quit the game")
        sys.exit()

    elif userInput < value:
        b.append(userInput)
        i+=1
        userInput=int(input("Please guess higher: "))

    elif userInput > value:
        i += 1
        b.append(userInput)
        userInput=int(input("Please guess lower: "))
    else:
        b.append(userInput)
        i+=1
        print("Your guess is correct")
        break


else:
    print("You haven't entered anything")

print("You have guessed correctly in {} tries".format(i))
print("Here is the list of your guesses")
print(b)









