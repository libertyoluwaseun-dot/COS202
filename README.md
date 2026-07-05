
def calculator():
    print("=================================")
    print("     MATHEMATICAL CALCULATOR")
    print("=================================")

    while True:
        print("\nChoose an operation")
        print("1. Addition (+)")
        print("2. Subtraction (-)")
        print("3. Multiplication (*)")
        print("4. Division (/)")
        print("5. Modulus (%)")
        print("6. Clear Screen")
        print("7. OFF")

        choice = input("Enter your choice (1-7): ")

        if choice == "7":
            print("Calculator is OFF. Goodbye!")
            break

        elif choice == "6":
            print("\n" * 50)
            continue

        elif choice in ["1", "2", "3", "4", "5"]:
            num1 = float(input("Enter first number: "))
            num2 = float(input("Enter second number: "))

            if choice == "1":
                print("Result =", num1 + num2)

            elif choice == "2":
                print("Result =", num1 - num2)

            elif choice == "3":
                print("Result =", num1 * num2)

            elif choice == "4":
                if num2 == 0:
                    print("Error! Division by zero is not allowed.")
                else:
                    print("Result =", num1 / num2)

            elif choice == "5":
                print("Result =", num1 % num2)

        else:
            print("Invalid choice. Try again.")

calculator()