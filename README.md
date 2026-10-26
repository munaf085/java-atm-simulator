# Build an ATM simulator

An ATM simulator for one account. The user enters a PIN (3 tries), then picks Balance, Deposit, Withdraw or Exit from a menu.

Withdrawals must be multiples of 100 and not more than the balance. If the user types letters instead of a number, the program asks again instead of crashing.

## Features

- Start with a balance of Rs 5000 and the PIN 4321.
- Allow 3 PIN attempts; after that, print `Card blocked. Please contact your bank.` and stop.
- Show a menu (Balance, Deposit, Withdraw, Exit) until the user picks Exit. Any other number prints `Please choose 1, 2, 3 or 4.`
- Deposit only amounts more than 0; otherwise print `Amount must be more than 0.`
- Withdraw only multiples of 100 that are not more than the balance; too much prints `Not enough balance.`
- Never crash on letters: catch `NumberFormatException` and ask again.

## How to run

```
javac *.java
java AtmSimulator
```

## Sample run

```
=== Java Bank ATM ===
Enter PIN: 1234
Wrong PIN. Attempts left: 2
Enter PIN: 4321
Login successful.

1. Balance  2. Deposit  3. Withdraw  4. Exit
Choose an option: 1
Balance: Rs 5000

1. Balance  2. Deposit  3. Withdraw  4. Exit
Choose an option: 3
Amount to withdraw: 750
Amount must be a multiple of 100.

1. Balance  2. Deposit  3. Withdraw  4. Exit
Choose an option: 3
Amount to withdraw: 2000
Please take your cash: Rs 2000. New balance: Rs 3000

1. Balance  2. Deposit  3. Withdraw  4. Exit
Choose an option: 2
Amount to deposit: abc
Please type digits only.
Amount to deposit: 1500
Deposited Rs 1500. New balance: Rs 4500

1. Balance  2. Deposit  3. Withdraw  4. Exit
Choose an option: 1
Balance: Rs 4500

1. Balance  2. Deposit  3. Withdraw  4. Exit
Choose an option: 4
Thank you for banking with us.
```

## Author

munaf085
