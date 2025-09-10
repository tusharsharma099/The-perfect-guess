# 🎯 Number Guessing Game (Python)

This is a simple **Number Guessing Game** written in Python.  
The program generates a random number between **1 and 100**, and the player has to guess it.  

---

## 📝 How It Works
1. The program uses the `random` module to generate a random number.  
2. The player is repeatedly asked to guess the number.  
3. If the guessed number is:
   - **Higher** than the actual number → the program says: *"Lower Number Please"*  
   - **Lower** than the actual number → the program says: *"Higher Number Please"*  
4. The game ends when the player guesses the correct number.  
5. Finally, the program displays the number of attempts the player took.

---

## 💻 Code
```python
import random

n = random.randint(1, 100)
a = -1
guesses = 0

while (a != n):
    guesses += 1
    a = int(input("Guess The Number : "))
    if (a > n):
        print("Lower Number Please")
    elif (a < n):
        print("Higher Number Please")

print(f"You have guessed the number {n} correctly in {guesses} attempts")
