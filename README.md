# Number-Gussing-Python
import random
import math

mini = int(input("Enter min value: "))
maxi = int(input("Enter max value: "))

x = random.randint(mini, maxi)

chances = round(math.log2(maxi - mini + 1))
print(f"You have {chances} chances only. All the best!")

count = 0

while count < chances:
    count += 1
    guess = int(input("Guess the number: "))

    if x == guess:
        print(f"Great, You choose the correct answer in {count} chance. ")
        break
    elif x < guess:
        print("Your guess is high")
    elif x > guess:
        print("Your guess is low")

if count >= chances:
   print("\nThe number is ",x)
   print("\tBetter Luck Next time!")
