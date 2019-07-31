# IEEE-CIS_Fraud_Detection

Fraud prevention system is protecting our daily transaction and actually saving consumers millions of dollars per year. However, the fraud detection system may be so "sensitive" that places us in an awkward situation. Just imagine standing at the check-out counter at a grocery store with a long line waiting for service and the cashier not-so-quietly announces that your card has been declined. And you step aside and allow the cashier to tend to the next customer. Then you receive a text message from your bank. ?Press 1 if you really tried to spend $500 on nachos.?               
In view of such cumbersome moment, this project is proposed and trying to improve the customer experience as well as fraud detection accuracy. The data comes from Vesta's real-world e-commerce transactions and contains a wide range of features from device type to product features.

## Goal:
improve the efficacy of fraudulent transaction

##  Data details:
The data is broken into two files identity and transaction, which are joined by TransactionID. Not all transactions have corresponding identity information.

- Transaction table:
	- TransactionID
	- TransactionDT: timedelta from a given reference datetime (not an actual timestamp)
	- TransactionAMT: transaction payment amount in USD
	- ProductCD: product code, the product for each transaction
	- card1 - card6: payment card information, such as card type, card category, issue bank, country, etc.
	- addr: address
	- dist: distance
	- P_ and (R__) emaildomain: purchaser and recipient email domain
	- C1-C14: counting, such as how many addresses are found to be associated with the payment card, etc. The actual meaning is masked.
	- D1-D15: timedelta, such as days between previous transaction, etc.
	- M1-M9: match, such as names on card and address, etc.
- Identity table:
	- TransactionID
	- id_12-id_38: identity information including network connection information (IP, ISP, Proxy, etc) and digital signature (UA/browser/os/version, etc) associated with transactions.
	- DeviceType
	- DeviceInfo
