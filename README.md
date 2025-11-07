IMPLEMENTATION AND CODE:

import time

def guess_number():
print("●◎’" ´ Think of a number between 1 and 100.") print("'’˘⬛*_' The AI will try to guess it!")
input("Press Enter when ready...")


low = 1
high = 100
attempts = 0
 


while low <= high: attempts += 1
guess = (low + high) // 2 print(f"\nAI guesses: {guess}") time.sleep(1)

feedback = input("Is it (H)igh, (L)ow, or (C)orrect? ").lower()


if feedback == 'c':
print(f"\n Yay! The AI guessed your number {guess} correctly in {attempts} attempts!") break
elif feedback == 'h': high = guess - 1
elif feedback == 'l': low = guess + 1
else:
print("+ Invalid input! Please enter H, L, or C.")


if low > high:
print("\n● • ^ ˙ Seems there was a mistake. Try again!")
 
# Run the game
if _name_ == "_main_": guess_number()
