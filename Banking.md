# Python program to create bank account class
# with both a deposit() and a withdraw() function


class Bank_Account:
	def __init__(self):
		self.balance = 0
		print("\nWelcome User to Deposit & Withdrawal Machine \n")

	def deposit(self):
		amount = float(input("Enter amount to be Deposited: \nRs."))
		self.balance += amount
		print("\n Amount Deposited:\nRs.\n", amount)

	def withdraw(self):

		amount = float(input("Enter amount to be Withdrawn: \nRs.\n"))
		if self.balance >= amount:
			self.balance -= amount
			print("You Withdrew:\nRs.\n", amount)
		else:
			print("Insufficient balance ")

    

	def display(self):
		print("Net Available Balance=\nRs.\n",self.balance)

# Driver code

# creating an object of class
s = Bank_Account()

# Calling functions with that class object
s.deposit()
s.withdraw()
s.display()
