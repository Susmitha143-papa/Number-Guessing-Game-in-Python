# Number-Guessing-Game-in-Python
import random
lowest_num=1
highest_num=100
answer=random.randint(lowest_num,highest_num)
guesses=0
is_running=True
print("Number guessing game in python")
print(f"Select a number between {lowest_num} and {highest_num}")
while True:
    guess=input("Enter a guess:")
    if not guess.isdigit():
        print("Invalid guess")
        print("Please select a number between {lowest_num} and {highest_num}")
    guess=int(guess)
    guesses+=1
    if guess<lowest_num and guess>highhest_num:
        print(f"{guess} is out of range")
        print("Please select a number between {lowest_num} and {highest_num}")
    elif guess<answer:
        print("Too low! Try Again..")
    elif guess>answer:
        print("Too high! Try Again..")
    else:
        print(f"Corrcet! The answer was :{answer}")
        print(f"The number of guesses are :{guesses}")
        is_running=False
