# Masrofi
a technical draft of an e-Payment system for algeria

## I. Introduction:
It is when the COVID19 tragedy struck our beloved Algeria, We as a nation felt the shortcomings of not having reliable e-Payment systems. Systems that help us reduce the pressure posed on our social structure.
‘Masrofi’ is an e-Payment system based entirely on the fact that you could use your phone as an easy way to pay virtually everything you can buy, even from the free market.
## II.	Basic Idea:
Flexy is the key word for this system. What we can do is simplify the process of sending money from one phone number account to another, the same way as you go to a Kiosk to charge your phone (phone number account) with money then use it to activate one of the offers given to you by your carrier (Djezzy, Mobilis, Ooredoo). However, instead of using that for internet or credit, you use it for buying stuff and transferring the right amount to the seller.
## III. Accounts and balance management:
For each number there will be an account, and when you dial for example the USSD CMD‘*790#’ you will receive back your balance in a Msg:

> Your balance is 1253.45 DA.

   ### 1. Account characteristics:
All accounts have these features:

*	 By design, each account is both a buyer and seller of type (so it is easy to spread the use of this system and remove bureaucracy).
*	 There is no max limit of how much the balance can go up.
*	 There is no credit mechanism nor possibility to have one (we are a poor country this would ruin our future with unnecessary debt).
*	 Each account has its own updated log of transactions with the possibility to access the log with a common USSD CMD.

   ### 2. Transactions CMDs:
For making it easy to build future APIs over this system, we define the following USSD commands
*	 Check Balance USSD CMD ‘*790#’.
*	 Transfer Balance USSD CMD ‘*791*TragetNumber*Amount*00001#’.
*	 Check Balance Log (for last 10 transactions) ‘*792#’.
*	 Get Transactions ledger ( for all transactions) ‘*799#’.
As for the number exact, we could replace the digit 7 with 6 or 5 based on the carrier.

   ### 3. Account Security:
   
For insuring, that all transactions are owner verified we would require the end user to enter a predefined pin code each time He/She wants to preform one of the above CMDs.

## IV.	Practical use:
When the end user goes to the free market and he wants to buy some fruits for example, he will find the QR code of the vendor or the vendor can supply him with his code from phone. The end user then scans the QR code and enters the amount of the purchase. The vendor receives the conformation message and all is well.     
 
The same way, we could implement an automatic system where a software will generate the QR code based on the amount of the cart (mall scenario) and the end user only scans and confirms the purchase.
## V. Concerns:
   *	This system is a financial system where the carriers will be the intermediary between the banks and the end user. As such, there might be laws to respect that are currently implemented in the constitution of the Republic of Algeria and could be the end of this system. 
   *	Users need to be educated of this system and how it can be used.
   *	There will be a need of some return or cancel mechanism.
   *	Inter carrier transactions are not thought of here and are left for the carriers to solve as a problem.
