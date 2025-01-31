# Payment Application Simulation
This is a Payment Application Simulation project for the EgFWD Embedded Systems Professional NanoDegree Scholarship. This project was written in C. It includes a Luhn card PAN generation and validation.

## Program Flow Chart
![payment-flowchart](https://user-images.githubusercontent.com/62207434/183305187-4d1241fb-fa97-4daf-8a6b-a1f41a540ac7.jpg)

## Functions

These are some of the functions I thought I should highlight:
- `appStart()` : this would be called in `Main.c` to start the application
- `getTransactionDate()` : asks for a date in the form `DD/MM/YYYY` or can retrieve `System Date` automatically
- `getCardPAN()` : this functions asks either to generate a Luhn valid card PAN or enter manually
  * Uses `GenerateLuhn()` which essentially applies the Luhn algorithm to generate the card PAN
- `readAccountDB()` : this load the accounts database from the database file (*read [database](https://github.com/FahdSeddik/ESND-Payment-Application#databases) section*)
- `saveTransaction()` : saves APPROVED transactions with all details into the transactions database (*read [database](https://github.com/FahdSeddik/ESND-Payment-Application#databases) section*)

## Instructions
- You would find demonstrated test cases in the "Submission Files/User Stories" Folder.
- This demonstrates how someone would use the Simulator.
- The test cases describe different scenarios that would happen:
  * `EXCEED_MAX_AMOUNT` : means that the user tried to make a transaction with more than specified max amount for card
  * `DECLINED_STOLEN_CARD` & `INVALID_ACCOUNT` : the card number is not present in the account database for the bank
  * `DECLINED_INSUFFECIENT_FUND` : transaction amount is greater than account balance
  *  `APPROVED` : the transaction was successful and saved to transactions database
