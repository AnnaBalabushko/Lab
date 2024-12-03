
Certificate
# Technology Certification System

This project simulates an organization providing technology certifications. The system allows assessors to verify if a person has passed a certification test based on certain criteria. The certificate is awarded if the person meets or exceeds the passing score defined by the certification criteria.

## Overview

The system consists of three main classes:

1. **Assessor**: The class responsible for verifying the certificate. It checks if the test score meets the passing score and generates a certification if the score is high enough.
2. **CertificationTest**: Represents the certification test taken by a candidate, containing the candidate's name, email, and test score.
3. **CertificationCriteria**: Defines the certification test's criteria, including the test name and passing score.


## Features

- Allows assessors to verify if a candidate passed the test based on predefined criteria.
- Provides a certificate with the candidate's details, assessor's details, and test information if the passing score is met.
- Allows easy extensibility to add more tests and criteria for other certifications.

## How It Works

1. **Assessor**:
   - The assessor enters their name and ID.
   - The assessor verifies whether the candidate has passed the test by comparing the candidate's score with the passing score from the `CertificationCriteria`.

2. **CertificationTest**:
   - Contains the candidate's details: name, email, and test score.
   
3. **CertificationCriteria**:
   - Defines the test's name and the passing score required to get certified.

If the candidate's test score is equal to or higher than the passing score, a certificate is generated with all relevant details. If not, the candidate is informed that they are not eligible for certification.



## Usage

After running the program, the following prompts will appear:

1. The **Assessor** is asked to enter their name and ID.
2. The **CertificationTest** and **CertificationCriteria** are predefined in the `main` method. You can modify these objects as needed.
3. The program will then evaluate whether the test score meets the passing criteria. If it does, the certification details will be displayed; otherwise, it will inform the user that the candidate is not eligible.

Example output:

```
Enter your name:
Anna Balabushko
Enter your id:
12345
Certificate:
Certification name: Java Programming
Recipient's name: Anna Balabushko
Recipient's email: annabalabushko@gmail.com
Assessor's name: Anna Balabushko
Assessor's id: 12345
```

## Classes and Methods

### Assessor Class

The `Assessor` class is responsible for verifying whether a candidate's score meets the criteria for certification. It contains the following methods:

- **Constructor**: 
  - Prompts the user to input their name and ID.
  
- **verifyCertificate**: 
  - Accepts a `CertificationTest` and a `CertificationCriteria` object. If the test score is higher than or equal to the passing score, the method generates a certification; otherwise, it notifies the user that the candidate is not eligible.

- **getName()**: 
  - Returns the name of the assessor.
  
- **getId()**: 
  - Returns the ID of the assessor.

### CertificationTest Class

The `CertificationTest` class represents the test that a candidate has taken. It holds the candidate's name, email, and test score. The class contains the following methods:

- **Constructor**: 
  - Takes the candidate's name, email, and test score as arguments.

- **getName()**: 
  - Returns the candidate's name.
  
- **getEmail()**: 
  - Returns the candidate's email.
  
- **getTestScore()**: 
  - Returns the candidate's test score.

### CertificationCriteria Class

The `CertificationCriteria` class defines the certification test and the passing score. It contains the following methods:

- **Constructor**: 
  - Takes the test name and the passing score as arguments.
  
- **getTestName()**: 
  - Returns the name of the certification test.
  
- **getPassingScore()**: 
  - Returns the passing score for the test.

______________________________________________________________________________________________________________________________________________________


CeasarCipher
# Caesar Cipher Encryption and Decryption

This Python script implements the **Caesar Cipher**, a basic encryption technique that shifts letters of the alphabet by a specified number. It can both **encrypt** and **decrypt** messages using a given shift value.

## Overview

The script provides two main functions:
1. **Encrypting a message**: It shifts the letters of the input message by a specified number (shift value).
2. **Decrypting a message**: It reverses the encryption process using the same shift value.

## Features

- Encrypt and decrypt messages using the Caesar Cipher.
- Handles both uppercase and lowercase letters.
- Non-alphabet characters (spaces, punctuation, etc.) are preserved.
- The shift value is customizable (1-25).

## How It Works

The Caesar Cipher works by shifting each letter of the plaintext by a fixed number of positions down or up the alphabet. For example, with a shift of 3:
- 'A' becomes 'D'
- 'B' becomes 'E'
- and so on.

To decrypt, the process is reversed by shifting in the opposite direction.

### Example:

- **Encryption**:  
  - Plaintext: `Hello World`  
  - Shift: 3  
  - Encrypted: `Khoor Zruog`

- **Decryption**:  
  - Ciphertext: `Khoor Zruog`  
  - Shift: 3  
  - Decrypted: `Hello World`


## Usage

1. When the script runs, you will be prompted to choose whether you want to **encrypt** or **decrypt** a message. 
2. You will then need to enter the message you want to process.
3. Finally, you'll be asked to input the **shift value** (an integer between 1 and 25).

Example Interaction:

```
Caesar Cipher Encryption/Decryption
Do you want to (E)ncrypt or (D)ecrypt a message? e
Enter your message: Hello World
Enter the shift value (1-25): 3
Encrypted message: Khoor Zruog
```

For decryption:

```
Caesar Cipher Encryption/Decryption
Do you want to (E)ncrypt or (D)ecrypt a message? d
Enter your message: Khoor Zruog
Enter the shift value (1-25): 3
Decrypted message: Hello World
```

## Code Explanation

### Functions

1. **`encrypt_message(plaintext, shift)`**:
   - Encrypts the given plaintext using the Caesar Cipher with the specified shift.
   - Handles both uppercase and lowercase letters and leaves non-alphabet characters unchanged.

2. **`decrypt_message(encrypted_text, shift)`**:
   - Decrypts the given encrypted text by reversing the shift used during encryption.
   - Preserves non-alphabet characters.

3. **`main()`**:
   - The main function that drives the script, prompting the user to select the action (encrypt or decrypt), input the message, and provide the shift value.
   - Calls the `encrypt_message` or `decrypt_message` functions based on the user's input and displays the result.

______________________________________________________________________________________________________________________________________________________

CheckProducer
# Personal Check Generator

This Java program simulates the creation of a personal check. It takes user input to generate the payee's name, check number, and check amount, and then prints out a formatted check with the amount written in words.

## Features

- Allows users to input the payee's name, check number, and check amount.
- Converts the check amount into words (e.g., `123.45` becomes `One hundred twenty-three dollars and forty-five cents`).
- Displays a formatted check with the payee's name, check number, and amount in words.

## How It Works

1. **User Input**: The program prompts the user for three inputs:
   - **Payee's Name**: The name of the person or entity the check is being paid to.
   - **Check Number**: A unique check number for the transaction.
   - **Check Amount**: The amount of the check (in decimal format).
   
2. **Amount Conversion**: The amount entered is converted into English words using the `EnglishNumberToWords` function.

3. **Check Generation**: The program generates and prints a formatted check displaying the following details:
   - **Check Number**
   - **Payee Name**
   - **Check Amount** (numeric and in words)


## Usage

1. Run the program, and you will be prompted to input:
   - The **payee's name**.
   - The **check number**.
   - The **amount of the check**.
   
2. After entering the values, the program will display a formatted check, including the check amount written in English words.

Example Interaction:

```
Enter the payee name:
John Doe
Enter the check number:
12345
Enter the amount of the check:
1500.75

----------------------------------------------------------------------------------------------------
Check #: 12345
Paid to the order of: John Doe                                                          $: 1500.75
One thousand five hundred dollars and seventy-five cents.
```

## Code Explanation

### Key Components

1. **`EnglishNumberToWords(int number)`**:
   - Converts a numeric value into its English word representation.
   - Handles values from 0 to 999,999,999,999.
   - Uses helper functions `convertLessThanOneThousand` and `convert` to break down large numbers into smaller parts (billions, millions, thousands).

2. **`generateCheck(String name, int number, double amount, String text)`**:
   - Prints out the formatted check with the check number, payee name, check amount, and the amount in words.
   
3. **Main Method**:
   - Collects input from the user.
   - Calls the conversion function to turn the check amount into words.
   - Calls the `generateCheck` method to print the formatted check.




CheckProducer2
# Personal Check Generator (CheckProducer2)

This Java program simulates creating a personal check by taking user input for the **payee's name**, **check number**, and **check amount**. The program formats the information and also converts the check amount into words (e.g., `2500.75` becomes `Two thousand five hundred and 75/100`).

## Features

- **Generate Check**: Formats the check information, including the payee's name, check number, and the amount in both numeric and word format.
- **Amount in Words**: Converts the check amount (dollars) into words. For example:
  - `1500.75` becomes `One thousand five hundred and 75/100`
  - `250.50` becomes `Two hundred and 50/100`
- Supports up to **four digits** for the check amount.

## How It Works

1. **User Input**: 
   - The program prompts the user to enter:
     - **Payee Name**: The person or organization receiving the check.
     - **Check Number**: The unique check number.
     - **Check Amount**: The amount of the check in numeric format (e.g., `1000.25`).

2. **Check Generation**: 
   - The program uses the input to generate a string that displays:
     - **Payee Name**
     - **Check Number**
     - **Check Amount in Numeric Format**
     - **Check Amount in Word Format**

3. **Amount Conversion**:
   - The amount is converted to words, separating the dollars from the cents (e.g., `1250.75` is converted to "One thousand two hundred and 75/100").


## Usage

1. When you run the program, it will ask for the following inputs:
   - **Payee Name** (e.g., `John Doe`).
   - **Check Number** (e.g., `12345`).
   - **Check Amount** (e.g., `1500.75`).

2. After entering the required information, the program will display the formatted check information, including the amount in words.

### Example Interaction:

```
Enter Payee Name:
John Doe
Enter Check Number:
12345
Enter check Amount:
1500.75

Output:
Payee Name: John Doe, Check Number: 12345, Amount: 1500.75 (One thousand five hundred and 75/100)
```

## Code Explanation

### Key Components

1. **`generateCheck(int checkNumber, String payeeName, double dollarAmount)`**:
   - Generates the formatted string with payee name, check number, and the amount both numerically and in words.
   - Calls the `amountToWord()` method to convert the numeric amount into words.

2. **`amountToWord(double dollarAmount)`**:
   - Converts the dollar amount into its English word representation.
   - Divides the amount into the whole number (before the decimal point) and the fractional part (after the decimal).
   - Calls `numberToWord()` to convert the whole dollar amount into words and formats the cent amount as a fraction (e.g., `75/100` for `0.75`).

3. **`numberToWord(char[] number)`**:
   - Converts an array of digits into a readable word format. Handles numbers from **1 to 9999**.
   - Uses arrays like `single_digit`, `two_digit`, and `multiple_10` to convert individual numbers into words.
   
4. **`main()`**:
   - Takes user input for the payee name, check number, and check amount.
   - Displays the generated check with the formatted output.


## Limitations

- The program currently supports check amounts up to **four digits** for the whole number part (i.e., it handles numbers from 0 to 9999 for the whole number).
- The decimal portion (cents) is displayed as a fraction of `100` (e.g., `50/100` for `0.50`).
- Only supports **whole numbers and fractional cents**, and will not correctly handle amounts with more than two decimal places.


______________________________________________________________________________________________________________________________________________________



MyPayments
# MyPayments - Payment Simulation

This Java program simulates different payment methods: **Cash Payment** and **Credit Card Payment**. It demonstrates object-oriented programming by using classes and inheritance. The program allows the user to create `CashPayment` and `CreditCardPayment` objects, set values, and display payment details.

## Features

- **CashPayment Class**: Represents a payment made in cash. Allows setting and displaying the payment amount.
- **CreditCardPayment Class**: Represents a payment made using a credit card. Includes credit card details like the card number, expiration date, and cardholder name. 
- **Polymorphism**: Both `CashPayment` and `CreditCardPayment` inherit from the base `Payment` class, demonstrating inheritance and polymorphism.

## Classes and Methods

### `Payment` Class
The base class for both `CashPayment` and `CreditCardPayment`.

- **Attributes**:
  - `double payment`: Stores the payment amount.
  
- **Methods**:
  - `double getPayment()`: Returns the payment amount.
  - `void setPayment(double payment)`: Sets the payment amount.
  - `void paymentDetails()`: Displays the payment details.

### `CreditCardPayment` Class
This class inherits from `Payment` and represents payments made with a credit card.

- **Attributes**:
  - `int expirymonth`: The expiry month of the card.
  - `int expiryyear`: The expiry year of the card.
  - `long cardNumber`: The card number.
  - `String name`: The cardholder's name.
  
- **Constructors**:
  - `CreditCardPayment()`: Default constructor with predefined values.
  - `CreditCardPayment(int expiryMonth, int expiryYear, String name, long cardNumber)`: Constructor to set custom values.

- **Methods**:
  - `void setExpire(int ex_month, int ex_year)`: Sets the expiration month and year.
  - `void setMonth(int ex_month)`: Sets the expiration month.
  - `void setYear(int ex_year)`: Sets the expiration year.
  - `void setName(String name)`: Sets the cardholder's name.
  - `void setNumber(long card_num)`: Sets the card number.
  - `String getNumberFormat()`: Formats the card number as `XXXX XXXX XXXX XXXX`.
  - `String getExpire()`: Returns the expiration date in the format `MM/YYYY`.
  - `void paymentDetails()`: Displays the credit card payment details.

### `CashPayment` Class
This class also inherits from `Payment` and represents payments made in cash.

- **Constructors**:
  - `CashPayment()`: Default constructor with a payment amount of 0.
  - `CashPayment(double payment)`: Constructor that initializes the payment amount.
  
- **Methods**:
  - `void paymentDetails()`: Displays the payment details for cash payments.

### `MyPayments` (Main Class)
The main class that executes the program and handles user input for the payment amounts.

- **Methods**:
  - `public static void main(String[] args)`: Prompts the user for input, creates `CashPayment` and `CreditCardPayment` objects, and displays their details.

## Example Workflow

1. **Create a CreditCardPayment**:
   - The user enters the expiration date, cardholder name, and card number.
   - The user enters a payment amount.
   
2. **Create a CashPayment**:
   - The user enters a cash payment amount.

3. **Display Payment Details**:
   - The program prints out the details of both `CashPayment` and `CreditCardPayment` using their `paymentDetails()` methods.

### Example Interaction:

```
Enter the amount you'd like to pay: 150.75
Enter the amount you'd like to pay (in cash): 50.00
The amount you entered was: 50.0
The current payment amount is: $50.0 in cash.
Enter the amount you'd like to pay (in cash): 200.00
The current payment amount is: $200.0 in cash.
Enter the expiration month: 12
Enter the expiration year: 23
Enter the card holder's name: John Doe
Enter the card number (16 digits): 1234567890123456
Name on card: John Doe
Card Number: 1234 5678 9012 3456
Expiration date: 12/23
Payment amount: 150.75
```

### Output Format:
- For `CashPayment`: 
  - Displays the payment amount followed by "in cash".
- For `CreditCardPayment`:
  - Displays the cardholder's name, card number (formatted), expiration date, and payment amount.


3. **Input Data**:
   Follow the prompts to enter the payment details for both credit card and cash payments.

## Code Explanation

1. **Scanner Input**:
   - The program uses `Scanner` to gather input from the user for the payment amount, card details, and expiration date.
   
2. **Object Creation**:
   - It creates instances of `CreditCardPayment` and `CashPayment` and sets their properties based on user input.
   
3. **Polymorphism**:
   - Both `CashPayment` and `CreditCardPayment` inherit from the `Payment` class. The `paymentDetails()` method is overridden in each class to display the relevant payment details.
   
4. **Formatted Card Number**:
   - The credit card number is formatted in groups of four digits for readability (e.g., `1234 5678 9012 3456`).

## Limitations

- The program does not handle invalid input such as non-numeric characters for payment or card number.
- It assumes that the card number is always 16 digits long, and does not validate if it follows actual card number formats (e.g., Luhn's algorithm for credit card validation).


______________________________________________________________________________________________________________________________________________________


NmapScan
# Nmap Scanner in Python

This is a simple Python script that uses the `nmap` library to perform a port scan on a specified target host. The script scans the target host `scanme.nmap.org` (an example of a publicly accessible target for testing) and outputs the scan results, including the host state, protocols, and open ports.

## Features

- **Port Scanning**: The script scans the specified target for open ports using `nmap.PortScanner()`.
- **Protocol Detection**: It detects and prints protocols (e.g., TCP, UDP) for each open port.
- **Host Information**: The script prints out the state of each host and the state of each open port.

## Requirements

- **Python 3.x**: This script is written in Python 3.x.
- **nmap module**: The script uses the `nmap` module, which is a Python wrapper for the Nmap security scanner.

### Installation

To use this script, you need to install the `python-nmap` library and ensure that Nmap is installed on your system.

1. **Install Nmap**:

   If you don't have Nmap installed, you can install it as follows:

   - On **Linux** (Debian/Ubuntu):
     ```bash
     sudo apt-get install nmap
     ```

   - On **macOS**:
     ```bash
     brew install nmap
     ```

   - On **Windows**:
     Download and install Nmap from the official site: [https://nmap.org/download.html](https://nmap.org/download.html).

2. **Install the Python `nmap` Module**:

   Install the Python wrapper for Nmap using pip:

   ```bash
   pip install python-nmap
   ```

### Script Overview

The script uses the `nmap` library to scan a target host and gather information about open ports and services. Here's a breakdown of the code:

1. **Import the Nmap Module**:
   ```python
   import nmap
   ```

2. **Create a PortScanner Object**:
   ```python
   scanner = nmap.PortScanner()
   ```

3. **Specify the Target**:
   - The target in this case is set to `scanme.nmap.org`, a public test server provided by Nmap.
   ```python
   target = "scanme.nmap.org"
   ```

4. **Perform the Scan**:
   - The `scan()` method is called on the target, which starts the scan process. By default, this scans the most common 1000 ports.
   ```python
   scanner.scan(target)
   ```

5. **Print Results**:
   - The script then loops over all hosts detected and prints the state of the host, protocols, and port states.
   ```python
   for host in scanner.all_hosts():
       print("Host: ", host)
       print("State: ", scanner[host].state())
       for proto in scanner[host].all_protocols():
           print("Protocol: ", proto)
           ports = scanner[host][proto].keys()
           for port in ports:
               print("Port: ", port, "State: ", scanner[host][proto][port]['state'])
   ```

### Output

The script outputs information about the scanned host, including its state (up or down), the protocols (e.g., TCP, UDP), and the open ports along with their states (open, closed, filtered). Here's an example of what the output might look like:

```
Host:  scanme.nmap.org
State:  up
Protocol:  tcp
Port:  22 State:  open
Port:  80 State:  open
Protocol:  udp
Port:  161 State:  open
```

### Customization

- **Target**: You can modify the `target` variable to scan different IP addresses or domain names.
  ```python
  target = "example.com"  # Replace with your target
  ```
- **Port Range**: To scan specific ports, you can pass a range of ports to the `scan()` method:
  ```python
  scanner.scan(target, '22-80')  # Scan ports 22 to 80
  ```
- **Specific Protocols**: If you want to scan a specific protocol, you can specify it:
  ```python
  scanner.scan(target, arguments="-p 22 --tcp")  # Only scan TCP port 22
  ```

### Usage

1. **Run the Script**:
   You can run the script from the terminal or command prompt:
   ```bash
   python nmap_scan.py
   ```

2. **Modify Target**:
   If you want to scan a different target, simply replace the `target` variable with the IP address or domain name of your choice:
   ```python
   target = "192.168.1.1"  # Replace with your target
   ```

3. **Viewing Results**:
   After running the script, the results will be printed in the terminal, showing the host state, protocol, and open ports.

### Notes

- **Permissions**: Depending on your operating system and the ports being scanned, you might need to run the script with elevated privileges (e.g., as an administrator or with `sudo` on Linux).
- **Legal and Ethical Considerations**: Always ensure you have explicit permission before scanning networks or systems that you do not own. Unauthorized port scanning can be illegal and unethical.




______________________________________________________________________________________________________________________________________________________


NumbersFromFile
# NumbersFromFile Java Program

This Java program reads a text file (`numbers.txt`) that contains integers (one per line) and performs the following tasks:

- Counts the total number of integers in the file.
- Finds the largest integer.
- Finds the smallest integer.
- Calculates the average of the integers.
- Calculates the sum of all integers.

## Features

- **Input**: The program reads a text file (`numbers.txt`) containing integers.
- **Output**: The program prints the following information to the screen:
  - The total count of integers.
  - The smallest integer.
  - The largest integer.
  - The average of the integers.
  - The sum of all integers.

## Requirements

- **Java 8 or higher**: This program requires at least Java 8 to run.
- **Text file with integers**: The input file (`numbers.txt`) must contain integers (one per line).

### Input File Format

The input file `numbers.txt` should contain one integer per line, like so:

```
34
56
23
12
89
5
```

Each line should represent one integer value. The program reads the file line by line and processes each integer.


### Sample Output

If the `numbers.txt` file contains the following integers:

```
34
56
23
12
89
5
```

The output will look like:

```
Count of integers in the file: 6
Smallest Integer in the file: 5
Largest Integer in the file: 89
Average of the integers in the file: 36.5
Sum of all integers in the file: 219
File was closed
```

## Error Handling

The program includes error handling for common issues:

- **FileNotFoundException**: If the `numbers.txt` file is not found, an error message is displayed.
- **NumberFormatException**: If a line in the file contains something other than an integer (e.g., a string), the program will display an error message.
- **NoSuchElementException**: If the file is empty, the program will display an error message.

### Example Error Messages

1. **File Not Found**:
   ```
   Error: file was not found.
   ```

2. **Invalid Integer Format**:
   ```
   Error: A line contains more than one int or it contains a String
   ```

3. **Empty File**:
   ```
   Error: file was Empty
   ```

## Code Explanation

### Key Components of the Program

- **File Reading**: The program uses a `Scanner` object to read the file line by line.
- **Integer Parsing**: Each line is parsed as an integer using `Integer.parseInt()`.
- **Tracking Values**:
  - The program tracks the smallest integer (`sNum`), largest integer (`lNum`), sum (`sum`), and count (`countNum`).
  - The sum and count are updated during the loop over the file content.
  - The program also calculates the average using the formula:
    ```java
    average = sum / countNum;
    ```

- **Error Handling**: The program has multiple `catch` blocks to handle potential exceptions (such as file not found, invalid integer format, or an empty file).

- **Finally Block**: The `finally` block ensures that the `Scanner` object is closed properly, even if an error occurs.

### Closing the File

The program makes sure to close the `Scanner` object when it finishes reading the file or encounters an error, ensuring proper resource management:
```java
finally {
   scFile.close();
   System.out.print("File was closed");
}
```



______________________________________________________________________________________________________________________________________________________


PasswordStrengthChecker
# Password Strength Checker - Python Program

## Overview

This Python program checks the strength of a user's password based on certain criteria and provides feedback to help improve it. The program checks if the password meets the following requirements:

1. Minimum length of 8 characters.
2. Maximum length of 20 characters.
3. At least one uppercase letter.
4. At least one lowercase letter.
5. At least one digit.
6. At least one special character (e.g., !, @, #, $, %, etc.).

If the password meets all the requirements, it is considered strong. Otherwise, the program will give detailed feedback on what needs to be improved.

## Features

- **Checks password strength**: Evaluates the password against multiple criteria (length, character types).
- **Feedback mechanism**: Provides clear feedback for users to strengthen their passwords.
- **Customizable criteria**: The password strength criteria (such as minimum length, required characters) are set in the code and can be modified easily.

## Requirements

- **Python 3.x**: This program is written in Python 3.x, so make sure you have Python installed.
- **No external libraries required**: The program only requires Python’s built-in `re` library for regular expressions, which is included by default in Python 3.x installations.


## How to Use

1. **Run the Program**:
   - Open a terminal or command prompt.
   - Navigate to the directory where the `password_strength_checker.py` file is located.
   - Run the script using the following command:
     ```bash
     python password_strength_checker.py
     ```
   
2. **Enter Password**:
   - When prompted, enter the password that you want to check for strength.

3. **View Feedback**:
   - The program will evaluate the password and print out feedback on whether the password is strong or suggestions for improvement.

### Example Usage

1. **Strong Password**:
   ```bash
   Welcome to the Password Strength Checker!
   Please enter your password: SuperStrong123!
   
   Password Strength Report:
   Password is strong!
   ```

2. **Weak Password**:
   ```bash
   Welcome to the Password Strength Checker!
   Please enter your password: weakpass
   
   Password Strength Report:
   Password should be at least 8 characters long.
   Password should contain at least 1 uppercase letter(s).
   Password should contain at least 1 digit(s).
   Password should contain at least 1 special character(s) (e.g., !@#$%).
   ```

## Code Explanation

### `check_password_strength(password)` Function

This function takes the password as input and evaluates it against several criteria using regular expressions and simple checks:

1. **Length Check**: Ensures the password is between 8 and 20 characters.
2. **Uppercase Check**: Ensures the password contains at least one uppercase letter.
3. **Lowercase Check**: Ensures the password contains at least one lowercase letter.
4. **Digit Check**: Ensures the password contains at least one digit.
5. **Special Character Check**: Ensures the password contains at least one special character (e.g., `!@#$%`).

It returns a string of feedback messages, or a success message if the password is strong.

### `main()` Function

This function is the entry point of the program:
- It prompts the user to enter a password.
- It calls the `check_password_strength` function to evaluate the password.
- It prints the password strength report to the console.

### Regular Expressions Used

- `[A-Z]`: Matches any uppercase letter.
- `[a-z]`: Matches any lowercase letter.
- `[0-9]`: Matches any digit.
- `[\W_]`: Matches any non-word character (special characters like `!@#$%`).

### Error Handling

- The program does not explicitly handle input errors since the `input()` function takes user input as a string. However, if users enter a password that doesn't meet the criteria, the program will provide appropriate feedback.

## Customization

The password strength criteria can be easily modified by changing the values of the following variables inside the `check_password_strength` function:

- `min_length`: Minimum length of the password.
- `max_length`: Maximum length of the password.
- `min_uppercase`: Minimum number of uppercase letters required.
- `min_lowercase`: Minimum number of lowercase letters required.
- `min_digits`: Minimum number of digits required.
- `min_special`: Minimum number of special characters required.

Example:
```python
min_length = 10
min_uppercase = 2
```

This would change the criteria to:
- Minimum length of 10 characters.
- Minimum of 2 uppercase letters.



______________________________________________________________________________________________________________________________________________________


**Note:** These projects are for educational purposes to demonstrate the use of classes and basic logic in Java and Python. 
