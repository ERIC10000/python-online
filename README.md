# python-online- Data Science

## Project1

```
# SIMPLE BANKING SYSTEM
# VARIABLES, DATA TYPES AND DECISIONS, IMPROVED(LOOPING AND FUNCTION.)

# Bank Account Information
account_name = "ERICK OTIENO"
account_pin = 1234
account_balance = 5000
account_status = "active"

# Bank Agents.
agent1 = 1234
agent2 = 5678
agent3 = 9876


# The System:
print("=======================")
print("WELCOME TO MARTIAL BANK")
print("=======================")

if account_status == "active":
    user_pin = int(input("Please Enter Your pin?"))
    if user_pin == account_pin:
        print("ACCESS GRANTED")
        print(f"WELCOME {account_name}")
        print("=========================")

        # Menu
        print("Please to Choose the Options Below")
        print("1. Withdraw Cash")
        print("2. Deposit Cash")
        print("3. Send Money")
        print("4. Check Balance")
        print("5. Change pin")
        print("0. Exit Account")

        # Request for the choice
        user_option = int(input("Enter Your Choice?"))
        if user_option == 1:
            print("Proceeding to Withdraw...")
            user_amount = int(input("Enter the Amount?"))
            # Check weather amount is less than the Balance
            if user_amount <= account_balance:
                print("TRANS. APPROVED")
                print(f"Successfully Withdrawn {user_amount}")
                print(f"Your Account Balance is {account_balance-user_amount} KSHS")
                print("======================================")
            else:
                print("INSUFFICIENT ACCOUNT BALANCE")
                print(f"YOUR BALANCE IS {account_balance} KSHS")
                print("TRY, AGAIN")
                print("=============================")

        elif user_option == 2:
            print("Proceeding to Deposit...")
            agent_no = int(input("Enter Your Agent No.?"))
            if agent_no == agent1 or agent_no == agent2 or agent_no == agent3:
                user_amount = int(input("Enter Amount to Deposit?"))
                account_balance = account_balance + user_amount
                print("TRANS. APPROVED")
                print(f"Successfully Deposited {user_amount} KSHS at Agent No. {agent_no}. Your Current Balance is {account_balance}")
            else:
                print("ENTERED WRONG AGENT NO")
                print("TRY, AGAIN")
                print("=======================")


        elif user_option == 3:
            print("Proceeding to Send Money...")
        elif user_option == 4:
            print("Proceeding to Check Balance...")
        elif user_option == 0:
            print("Proceeding to Exit...")
        else:
            print("Invalid Choice, Try Again..")
        
    else:
        print("WRONG PIN!!!")
        print("TRY AGAIN!!!")
        print("=====================")
else:
    print("YOUR ACCOUNT IS NOT ACTIVE")
    print("PLEASE VISIT C.CARE FOR ACTIVATION")
    print("===================================")



# LOOPING STATEMENTS IN PYTHON
# FOR LOOPS
# WHILE LOOPS
# INFINITE LOOPS
# BREAK KEYWORD
# CONTINUE KEYWORD.
# project2: Cont of Project1
```


### Project2 with Loops
```
# SIMPLE BANKING SYSTEM WITH LOOPS:
# VARIABLES, DATA TYPES AND DECISIONS, IMPROVED(LOOPING AND FUNCTION.)

# 1. The System Should Always be Running -> Infinite Loop
# 2. Request Pin 3 times(trial)

# Bank Account Information
account_name = "ERICK OTIENO"
account_pin = 1234
account_balance = 5000
account_status = "active"

# Bank Agents.
agent1 = 1234
agent2 = 5678
agent3 = 9876


# The System:
print("=======================")
print("WELCOME TO MARTIAL BANK")
print("=======================")

if account_status == "active":
    for attempts in range(1, 4, 1):
        user_pin = int(input(f"Please Enter Your pin? Attempt {attempts}"))
        if user_pin == account_pin:
            print("ACCESS GRANTED")
            print(f"WELCOME {account_name}")
            print("=========================")

            # Menu
            while True:
                print("Please to Choose the Options Below")
                print("1. Withdraw Cash")
                print("2. Deposit Cash")
                print("3. Send Money")
                print("4. Check Balance")
                print("5. Change pin")
                print("0. Exit Account")

                # Request for the choice
                user_option = int(input("Enter Your Choice?"))
                if user_option == 1:
                    print("Proceeding to Withdraw...")
                    user_amount = int(input("Enter the Amount?"))
                    # Check weather amount is less than the Balance
                    if user_amount <= account_balance:
                        print("TRANS. APPROVED")
                        print(f"Successfully Withdrawn {user_amount}")
                        print(f"Your Account Balance is {account_balance-user_amount} KSHS")
                        print("======================================")
                    else:
                        print("INSUFFICIENT ACCOUNT BALANCE")
                        print(f"YOUR BALANCE IS {account_balance} KSHS")
                        print("TRY, AGAIN")
                        print("=============================")

                elif user_option == 2:
                    print("Proceeding to Deposit...")
                    agent_no = int(input("Enter Your Agent No.?"))
                    if agent_no == agent1 or agent_no == agent2 or agent_no == agent3:
                        user_amount = int(input("Enter Amount to Deposit?"))
                        account_balance = account_balance + user_amount
                        print("TRANS. APPROVED")
                        print(f"Successfully Deposited {user_amount} KSHS at Agent No. {agent_no}. Your Current Balance is {account_balance}")
                    else:
                        print("ENTERED WRONG AGENT NO")
                        print("TRY, AGAIN")
                        print("=======================")


                elif user_option == 3:
                    print("Proceeding to Send Money...")
                elif user_option == 4:
                    print("Proceeding to Check Balance...")
                elif user_option == 0:
                    print("Proceeding to Exit...")
                else:
                    print("Invalid Choice, Try Again..")
            
        else:
            print("WRONG PIN!!!")
            print("TRY AGAIN!!!")
            print("=====================")
else:
    print("YOUR ACCOUNT IS NOT ACTIVE")
    print("PLEASE VISIT C.CARE FOR ACTIVATION")
    print("===================================")



# LOOPING STATEMENTS IN PYTHON
# FOR LOOPS
# WHILE LOOPS
# INFINITE LOOPS
# BREAK KEYWORD
# CONTINUE KEYWORD.
# project2: Cont of Project1
```

