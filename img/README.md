# ATM

 # Itachi ATM Simulation
 
 A simple Python script that simulates a basic ATM machine. Users can check their balance, deposit, and withdraw money after entering the correct PIN.

***Features*** <br>
  - PIN authentication for security
  - Check account balance
  - Deposit money
  - Withdraw money (with insufficient funds check)
  - Realistic transaction processing delays using ``` time.sleep() ```
  - Friendly prompts and messages

***How It Works*** <br>

  1. The script waits a few seconds to simulate an ATM booting up.
  2. The user is prompted to insert their card and enter their PIN.
  3. If the PIN is correct, the user can:
     - Check their balance
     - Deposit money
     - Withdraw money
  4. Each transaction simulates processing time for a more realistic experience.
  5. The script handles incorrect PINs and insufficient balance scenarios.

***Usage*** <br>
 1. Copy the following code into a Python file (e.g., atm.py):
  
    ```
    import time
    time.sleep(2)
    pin = 1234
    bal = 1000
    print("Welcome to Itachi Atm")
    time.sleep(3)
    print("Insert a your card")
    time.sleep(1)
    p = int(input("Enter a Pin:"))
    if pin == p:
        time.sleep(1)
        print("Transcation Processing.........")
        while True:
        time.sleep(4)
        print("1.Check Balance\n2.Desopit\n3.Withdrawal")
        opt = int(input("Enter a No:"))
        if opt == 1:
            time.sleep(1)
            print("Transcation Processing.........")
            time.sleep(3)
            print("Current balance $", bal)
            time.sleep(2)
            print("Remove your card\n Thanks for visiting a ATM")
            pass
        elif opt == 2:
            print("Transcation Processing.........")
            amt = int(input("Enter a amout to Deposit $ :"))
            bal += amt
            time.sleep(1)
            print("Your Desopit amount $", amt)
            time.sleep(1)
            print("Your current balance is $", bal)
            time.sleep(1)
            print("Deposit Successfully ")
            continue  
        elif opt == 3:
            print("Transcation Processing.........")
            amt = int(input("Enter a amout to Withdirwal $:"))
            if amt < bal:
                bal -= amt
                print("Trancsation procesing...")
                time.sleep(2)
                print("Collect you cash.....")
                time.sleep(2)
                print("Successfully Withdrwal cash\nPlease remove your atm card")
            elif amt > bal:
                print("Insufficient amount\nRemove your atm card\nThanks u for visiting atm")
            else:
                print("Trascation processing....")
                time.sleep(4)
                print("Invaild pin")
                break
    else:
        print("Trascation processing....")
        time.sleep(4)
        print("Invaild pin")

    ```
 3. Run the script:
     ```
     python atm.py
     ```
 4. Follow the on-screen instructions.

***Example Interaction*** <br>

 ```
  Welcome to Itachi Atm
  Insert a your card
  Enter a Pin: 1234
  Transcation Processing.........
  1.Check Balance
  2.Desopit
  3.Withdrawal
  Enter a No: 1
  Transcation Processing.........
  Current balance $ 1000
  Remove your card
  Thanks for visiting a ATM

 ```
***Notes*** <br>

  - The default PIN is 1234 and the initial balance is $1000.
  - Transactions are simulated with delays for realism.
  - The script does not persist data between runs.
  - There are some spelling mistakes in the prompts (e.g., "Desopit" instead of "Deposit", "Withdirwal" instead of "Withdrawal"). You can correct these for a more polished experience.


 # V 1.1
  # ATM Simulation – Deposit Feature Update

This project is a Python script simulating a simple ATM machine. It allows users to check balance, deposit, and withdraw money after PIN authentication.
This version highlights an improved deposit feature with enhanced transaction feedback and processing simulation.

***What's New in Deposit Feature?***<br>
 
  - Added an extra transaction processing message and delay after entering the deposit amount, making the experience more realistic.

 - Improved user feedback during the deposit process.

***New Deposit Code***

  ```
  elif opt==2:
            print("Transcation Processing.........")
            amt=int(input("Enter a amout to Deposit $ :"))
            bal +=amt
            print("Transcation Processing.........")  # New line added
            time.sleep(3)
            print("Your Desopit amount $",amt)
            time.sleep(1)
            print("Your current balance is $",bal)
            time.sleep(1)
            print("Deposit Successfully ")
            continue
  ```

***How to Use***

  1. Copy the updated code into your Python file (e.g., atm_simulator.py).
  2. Run the script:
  ```
  python atm_simulator.py
  ```
  3. Enter your PIN and select the deposit option to experience the improved feedback.

***Example Deposit Interaction***

 ```
Transcation Processing.........
Enter a amout to Deposit $ : 200
Transcation Processing.........
Your Desopit amount $ 200
Your current balance is $ 1200
Deposit Successfully 

 ```

***Notes**
  - The extra processing message and delay simulate real ATM behavior, improving user experience.
  
  - The script still includes options for balance check and withdrawal.
  
  - You can further customize prompts and delays as needed.
