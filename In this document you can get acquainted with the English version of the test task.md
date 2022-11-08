# test_task_2.0
Testing on a screenshot of a payment form without requirements and valid data


Test
Task: Provided a screenshot of the payment form, test the form
Position : Junior Manual QA
Performer: Kuznets Sergey Olegovich



Preface for the test task prepare test data taken from these sources:

https://docs.assist.ru/pages/viewpage.action?pageId=5767473

https://www.kobzarev.com/other/testoviye-nomera-kreditnyh-kart


test data
Table 1.

Number Card type Length EXP number CVV result


1 Discover 16 6011111111111117 Any Any (successful payment)

2 Dinners Club 14 38520000023237 Any Any (successful payment)

3 American Express 15 371449635398431 Any Any (successful payment)

4 Visa 16 4652060573334999 01/2021 067 (Not successful payment)

5 MasterCard 16 5124990000000002 12/2021 123 ( unknown error )

6 Visa 16 4444 4444 1111 1111 2024/12 123 (The network rejected the transaction)
 
7 Visa 16 4444 4444 4444 6666 2024/12 123 (Limit locked)

8 Mastercard 16 5432 5432 5432 5430 2022/12 123 (insufficient funds)

9 Visa 16 4444 4444 4444 4455 2024/12 123 (Card limits exceeded)




Test case 1 "Successful payment card type Discover"

Play steps :

1.Open the payment form
2. From Table No. 1, take the card data (1)
3.Enter the card number "6011111111111117"
4.In the "Expiry Day" field, enter the month "12"
5.In the "Expiry Day" field, enter the year "2023"
6.In the "CVV / CVC / CID" field, enter "123"
7.Press the "PAY" button

Expected result: "After clicking on the payment button, the user is presented with an informational pop-up window about successful payment"


Test case 2 "Successful payment card type Dinners Club"

Play steps :

1.Open the payment form
2. From Table No. 1, take the card data (2)
3.Enter the card number "38520000023237"
4.In the "Expiry Day" field, enter the month "12"
5.In the "Expiry Day" field, enter the year "2023"
6.In the "CVV / CVC / CID" field, enter "123"
7.Press the "PAY" button

Expected result: "After clicking on the payment button, the user is presented with an informational pop-up window about successful payment"

Test case 3 "Successful payment type American Express card"

Play steps :

1.Open the payment form
2. From Table No. 1, take the card data (3)
3.Enter the card number "371449635398431"
4.In the "Expiry Day" field, enter the month "12"
5.In the "Expiry Day" field, enter the year "2023"
6.In the "CVV / CVC / CID" field, enter "123"
7.Press the "PAY" button

Expected result: "After clicking on the payment button, the user is presented with an informational pop-up window about successful payment"


Test case 4 "Payment not successful, expired Visa card"

Play steps :

1.Open the payment form
2. From Table No. 1, take the card data (4)
3.Enter the card number "4652060573334999"
4.In the "Expiry Day" field, enter the month "01"
5.In the "Expiry Day" field, enter the year "2021"
6.In the "CVV / CVC / CID" field, enter "067"
7.Press the "PAY" button

Expected result: "After clicking on the payment button, the user is presented with an informational pop-up window that his card is expired"


Test case 5 "Unknown MasterCard error"

Play steps :

1.Open the payment form
2. From Table No. 1, take the details of the MasterCard card (5)
3.Enter the card number "5124990000000002"
4.In the "Expiry Day" field, enter the month "12"
5.In the "Expiry Day" field, enter the year "2021"
6.In the "CVV / CVC / CID" field, enter "123"
7.Press the "PAY" button

Expected result: "After clicking on the payment button, the user is presented with an informational pop-up window that the operation cannot be
completed "An unknown error has occurred."


Test case 6 "The network rejected the Visa card transaction"

Play steps :

1.Open the payment form
2. From Table No. 1, take the data of the Visa card (6)
3.Enter the card number "4444 4444 1111 1111"
4.In the "Expiry Day" field, enter the month "12"
5.In the "Expiry Day" field, enter the year "2024"
6.In the "CVV / CVC / CID" field, enter "123"
7.Press the "PAY" button

Expected result: "After clicking on the payment button, the user is presented with an informational pop-up window that the operation cannot be
completed "The network rejected the transaction."


Test case 7 "Limit blocked, Visa card"

Play steps :

1.Open the payment form
2. From Table No. 1, take the data of the Visa card (7)
3.Enter the card number "4444 4444 4444 6666"
4.In the "Expiry Day" field, enter the month "12"
5.In the "Expiry Day" field, enter the year "2024"
6.In the "CVV / CVC / CID" field, enter "123"
7.Press the "PAY" button

Expected result: "After clicking on the payment button, the user is presented with an informational pop-up window that the operation cannot be
completed "Limit locked".

Test case 8 "insufficient funds, Mastercard"

Play steps :

1.Open the payment form
2. From Table No. 1, take the details of the Mastercard card (8)
3.Enter the card number "5432 5432 5432 5430"
4.In the "Expiry Day" field, enter the month "12"
5.In the "Expiry Day" field, enter the year "2022"
6.In the "CVV / CVC / CID" field, enter "123"
7.Press the "PAY" button

Expected result: "After clicking on the payment button, the user is presented with an informational pop-up window that the operation cannot be
completed "insufficient funds."


Test case 9 "Card limits exceeded, Visa card"

Play steps :

1.Open the payment form
2. From Table No. 1, take the data of the Visa card (9)
3.Enter the card number "4444 4444 4444 4455"
4.In the "Expiry Day" field, enter the month "12"
5.In the "Expiry Day" field, enter the year "2024"
6.In the "CVV / CVC / CID" field, enter "123"
7.Press the "PAY" button

Expected result: "After clicking on the payment button, the user is presented with an informational pop-up window that the operation cannot be
completed "Map limits exceeded".

Test case 10 "Leave card number blank"

Play steps :

1.Open the payment form
2.Field "Card number leave blank"
4.In the "Expiry Day" field, enter the month "12"
5.In the "Expiry Day" field, enter the year "2024"
6.In the "CVV / CVC / CID" field, enter "123"
7.Press the "PAY" button

Expected result: "After clicking on the payment button, the user is presented with an informational pop-up window that "the required field Card number is not filled"".

Test Case 11 "Leave Expiry Day blank"

Play steps :

1.Open the payment form
2. From Table No. 1, take the data of the Visa card (8)
3.Enter the card number "5432 5432 5432 5430"
4. In the "Expiry Day" field, do not enter a month
5. In the field "Expiry Day" do not enter the year
6.In the "CVV / CVC / CID" field, enter "123"
7.Press the "PAY" button

Expected result: "After clicking on the payment button, the user is presented with an informational pop-up window that the operation cannot be
completed "Required field Expiry Day is empty ".

Test case 12 "СVV/CVC/CID leave blank"

Play steps :

1.Open the payment form
2. From Table No. 1, take the data of the Visa card (8)
3.Enter the card number "5432 5432 5432 5430"
4.In the field "Expiry Day" enter the month 12
5.In the field "Expiry Day" enter the year 2022
6. In the field "CVV / CVC / CID" leave empty after
7.Press the "PAY" button

Expected result: "After clicking on the payment button, the user is presented with an informational pop-up window that the operation cannot be
completed "Required field CVV/CVC/CID not filled in".


Test case 13 "Returning to the previous step of Checkout"

Play steps :

1.Open the payment form
2. From Table No. 1, take the data of the Visa card (8)
3.Enter the card number "5432 5432 5432 5430"
4.In the field "Expiry Day" enter the month 12
5.In the field "Expiry Day" enter the year 2022
6.In the field "CVV / CVC / CID" enter "123"
7.Click the "Cancel" button

Expected result: "After clicking on the "Cancel" button, the user is returned to the previous checkout page, with the saved data that he entered earlier."

Test case 14 "Checking if the Card number field accepts special characters"

Play steps :

1.Open the payment form
2.Enter the special characters "?*:*;#;*#(;*%;*("
3.Go to the next field "Expiry Day"

Expected result: "The user will be warned that this field only accepts numeric values"

Test Case 15 "Checking if the Card Number field accepts HTML tags"

Play steps :

1.Open the payment form
2. Enter "<img>" in the CARD NUMBER field
3.Go to the next field "Expiry Day"

Expected result: "The user will be warned that this field only accepts numeric values"

Test case 16 "Checking if the CVV/CVC/CID field accepts special characters"

Play steps :

1.Open the payment form
2.Enter special characters in the field CVV/CVC/CID "#$%"
3.Press the "PAY" button

Expected result: "The user will be warned that this field only accepts numeric values"

Test case 17 "Checking for the maximum number of characters in the Card number field"

Play steps :
1.Open the payment form
2.Enter the Card number "5432 5432 5432 5430 5430 5430" - 24 characters
3.Go to the next field "Expiry Day"

Expected result: "The user will be warned that this field can accept a maximum of 22 characters according to the standards" (Suggestion for the CARD NUMBER FIELD "DO
INPUT MASK according to usability will be much more convenient for the user to enter data for placing an order and quick and convenient use when buying ")

Test case 18 "Checking for the minimum number of characters to be entered for the Card number field"

Play steps :

1.Open the payment form
2. From Table No. 1, take the data of the Visa card (8)
3.Enter the card number "5432"
4.In the field "Expiry Day" enter the month 12
5.In the field "Expiry Day" enter the year 2022
6. In the field "CVV / CVC / CID" leave empty after
7.Press the "PAY" button

Expected result: "After clicking on the payment button, the user is presented with an informational pop-up window that the value in the CARD NUMBER field is too short."

Test case 19 "Checking if the Card number field accepts literal values"

Play steps :

1.Open the payment form
2. Enter in the field CARD NUMBER "HEADLIGHT"
3.Go to the next field "Expiry Day"

Expected result: "The user will be warned that this field only accepts numeric values"

Test case 20 "Checking if the CVV/CVC/CID field accepts literal values"

Play steps :

1.Open the payment form
2. In the card number field, enter the data taken from table 1 Number (8) 5432 5432 5432 5430
3.Go to the next field "Expiry Day" enter the month "12"
4.Go to the next field "Expiry Day" enter the year 2022
5.Enter in the field СVV/CVC/CID "BAR"
6.Press the "PAY" button

Expected result: "The user will be warned that the given field "CVV/CVC/CID" accepts only numeric values"
