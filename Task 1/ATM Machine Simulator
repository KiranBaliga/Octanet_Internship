# Simple ATM Machine Simulation

class ATMMachine:
    def __init__(self, initial_balance=0, initial_pin="1234"):
        self.balance = initial_balance
        self.pin = initial_pin
        self.transaction_history = []
    
    def check_balance(self):
        # Display the current balance
        print(f"Your current balance is: ${self.balance}")
        self.transaction_history.append(f"Balance inquiry: ${self.balance}")
    
    def withdraw_cash(self, amount):
        # Withdraw cash if the amount is available
        if amount > self.balance:
            print("Insufficient balance.")
        else:
            self.balance -= amount
            print(f"${amount} has been withdrawn.")
            self.transaction_history.append(f"Withdrew: ${amount}")
    
    def deposit_cash(self, amount):
        # Deposit cash into the account
        self.balance += amount
        print(f"${amount} has been deposited.")
        self.transaction_history.append(f"Deposited: ${amount}")
    
    def change_pin(self, old_pin, new_pin):
        # Change the PIN if the old PIN matches
        if old_pin == self.pin:
            self.pin = new_pin
            print("PIN has been successfully changed.")
            self.transaction_history.append("PIN change")
        else:
            print("Incorrect old PIN.")
    
    def show_transaction_history(self):
        # Display the transaction history
        print("Transaction History:")
        for transaction in self.transaction_history:
            print(transaction)


# Create an instance of the ATM machine
atm = ATMMachine()

# Simple menu to interact with the ATM machine
while True:
    print("\n--- ATM Machine ---")
    print("1. Check Balance")
    print("2. Withdraw Cash")
    print("3. Deposit Cash")
    print("4. Change PIN")
    print("5. Show Transaction History")
    print("6. Exit")
    
    choice = input("Choose an option (1-6): ")
    
    if choice == "1":
        atm.check_balance()
    elif choice == "2":
        amount = float(input("Enter amount to withdraw: "))
        atm.withdraw_cash(amount)
    elif choice == "3":
        amount = float(input("Enter amount to deposit: "))
        atm.deposit_cash(amount)
    elif choice == "4":
        old_pin = input("Enter old PIN: ")
        new_pin = input("Enter new PIN: ")
        atm.change_pin(old_pin, new_pin)
    elif choice == "5":
        atm.show_transaction_history()
    elif choice == "6":
        print("Thank you for using the ATM. Goodbye!")
        break
    else:
        print("Invalid option. Please choose a number between 1 and 6.")
