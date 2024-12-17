# Code_Challenge15.py
import os

isGo = True
nt = 0  # Counter for triangle size

while isGo:
    ask = input("Do you wish to create more triangles (yes or no)? ")
    if ask.lower() == "no":
        os.system('cls' if os.name == 'nt' else 'clear') # Clear the console (cross-platform)
        print("Program terminated")
        isGo = False
    elif ask.lower() == "yes":
        os.system('cls' if os.name == 'nt' else 'clear') # Clear the console (cross-platform)
        nt += 1
        for x in range(1, nt + 1):  #Corrected range to nt+1
            for y in range(1, x + 1):
                print("^", end="")
            for z in range(5, x, -1): #Corrected range to 5, x, -1
                print(" ", end="")
            print()
