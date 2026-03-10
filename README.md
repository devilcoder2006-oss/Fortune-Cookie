# Fortune-Cookie

import random
import time

# List of fortune messages
fortunes = [
    "Aaj ka din tumhare liye lucky hai!",
    "Bahut jaldi tumhe ek bada opportunity milega.",
    "Hard work ka result jaldi milne wala hai.",
    "Aaj kuch naya seekhne ka mauka milega.",
    "Ek surprise tumhara intezar kar raha hai.",
    "Aane wale time me tumhari success pakki hai.",
    "Dost tumhari life me important role play karenge.",
    "Apni skills par kaam karo, future bright hai.",
    "Jo tum chahte ho wo jaldi mil sakta hai.",
    "Aaj ka din positive energy se bhara hua hai."
]

# Function to print cookie animation
def cookie_animation():
    print("\nOpening your Fortune Cookie", end="")
    for i in range(5):
        time.sleep(0.5)
        print(".", end="")
    print("\n")

# Function to get fortune
def get_fortune():
    fortune = random.choice(fortunes)
    return fortune

# Function to show menu
def show_menu():
    print("\n====== FORTUNE COOKIE MACHINE ======")
    print("1. Open a Fortune Cookie")
    print("2. See all possible fortunes")
    print("3. Exit")
    print("====================================")

# Function to show all fortunes
def show_all_fortunes():
    print("\nAll Possible Fortune Messages:\n")
    for i, msg in enumerate(fortunes, start=1):
        print(f"{i}. {msg}")

# Main program
def main():
    print("🍪 Welcome to the Fortune Cookie Machine 🍪")

    while True:
        show_menu()
        choice = input("Enter your choice: ")

        if choice == "1":
            cookie_animation()
            print("✨ Your Fortune is:")
            print(get_fortune())

        elif choice == "2":
            show_all_fortunes()

        elif choice == "3":
            print("Thanks for using Fortune Cookie Machine. Have a great day! 😊")
            break

        else:
            print("Invalid choice! Please try again.")

# Run program
main()
