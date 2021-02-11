# -Python-Project-8
#8 Does a number is Even or Odd ?

def main():
    def inputNumber(message):
        while True:
            try:
                inputNumber = int(input(message))
            except ValueError:
                print("Please, use a valid number.\n")
                continue
            else:
                return inputNumber
                break

    def inputAnswer(question):
        userInput = str(input(question)).lower()
        if userInput == "yes":
            return "yes"
        elif userInput == "no":
            return "no"
        else:
            return inputAnswer("Please, use 'yes' or 'no'.\n")

    number = inputNumber("Please, put a number.\n")

    if number % 2 == 0:
        print(f"{number} is even.\n")
    else:
        print(f"{number} is odd.\n")

    answer = inputAnswer("Thank you, do you need to check other number?\n")

    if answer == "yes":
        main()
    if answer == "no":
        print("See ya! Take care.\n")
main()
