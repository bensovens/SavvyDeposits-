# SavvyDeposits-
SavvyDeposits
class Me2uATM:
    def __init__(self):
        self.voucher_code = None

    def deposit_cash(self, amount):
        # Simulate depositing cash into ATM and generating a unique voucher code
        print(f"Depositing ${amount} into me2u ATM...")
        self.voucher_code = "ABC123"  # Simulated unique voucher code
        print("Cash deposited successfully.")
        return self.voucher_code

class CashTransacts:
    def __init__(self):
        self.balance = 0

    def access_funds(self, voucher_code):
        # Simulate accessing funds using voucher code
        if voucher_code:
            print(f"Accessing funds using voucher code: {voucher_code}")
            self.balance += 1000  # Simulated amount deposited
            print(f"Current balance: ${self.balance}")
        else:
            print("No voucher code provided.")

    def convert_vouchers(self):
        # Simulate converting Cashsend vouchers between banks
        print("Converting Cashsend vouchers between banks...")

    def receive_payments(self):
        # Simulate receiving payments such as payroll and SASSA payments
        print("Receiving payroll and SASSA payments...")

def main():
    me2u_atm = Me2uATM()
    cash_transacts = CashTransacts()

    print("Welcome to Me2u ATM and CashTransacts!")
    while True:
        print("\nChoose an option:")
        print("1. Deposit cash into me2u ATM")
        print("2. Access funds using voucher code")
        print("3. Convert vouchers between banks")
        print("4. Receive payments")
        print("5. Exit")

        choice = input("Enter your choice: ")

        if choice == '1':
            amount = float(input("Enter the amount to deposit: $"))
            voucher_code = me2u_atm.deposit_cash(amount)
        elif choice == '2':
            voucher_code = input("Enter your voucher code: ")
            cash_transacts.access_funds(voucher_code)
        elif choice == '3':
            cash_transacts.convert_vouchers()
        elif choice == '4':
            cash_transacts.receive_payments()
        elif choice == '5':
            print("Exiting program. Thank you for using Me2u ATM and CashTransacts!")
            break
        else:
            print("Invalid choice. Please try again.")

if __name__ == "__main__":
    main()
