# Cyber Bank - Graphical Banking System with PyQt5

## Project Overview
Cyber Bank is a fully graphical banking simulation application built with PyQt5, demonstrating advanced object-oriented programming principles and modern GUI design. Users can create accounts, perform transactions, apply for loans, and manage their finances through an intuitive Persian-language interface.

## Key Features

### Customer Features
- Account Creation: Register new bank accounts with personal information
- Balance Inquiry: View account balance in both Dollar and Rial currencies
- Withdraw Money: Securely withdraw funds from your account
- Transfer Money: Transfer funds between accounts with confirmation steps
- Transaction History: View last 3 transactions with Persian descriptions
- Loan Application: Apply for loans with automatic eligibility checking

### Manager Features
- Secure Login: Dedicated manager panel with authentication
- Loan Management: View and process pending loan applications
- Eligibility Check: Automatic validation of loan requests
- Approve/Reject: Accept or reject loan applications with one click

## Object-Oriented Design
The project showcases core OOP concepts:

### Classes and Inheritance
- BankAccount: Base account class for customer management
- FirstScreen (QDialog): Main entry screen
- All UI screens inherit from QDialog for consistent behavior

### Key OOP Principles
- Encapsulation: Each class manages its own data and behavior
- Inheritance: All UI screens inherit from QDialog
- Polymorphism: Different screens override common methods
- Abstraction: Complex banking logic hidden behind simple interfaces

## Project Structure

### Python Modules
user_interface.py - Main application with all UI classes
firstLook.py - BankAccount class for account management
isnumberic.py - Input validation utilities
test.py - Testing utilities

### UI Files (PyQt5 Designer)
First_Screen.ui - Main entry screen
Create_Account.ui - Account registration form
Features.ui - Main banking features menu
Balance.ui - Balance inquiry screen
Withdraw.ui - Withdrawal interface
Transform.ui - Money transfer form
Transform_Confirmatino.ui - Transfer confirmation
Transform_Final.ui - Transfer completion with progress bar
Turnovers.ui - Transaction history display
Loan.ui - Loan application form
Loan_Final.ui - Loan submission confirmation
Login_Manager.ui - Manager authentication
Manager.ui - Manager dashboard
Info.ui - Account information display

### Data Files
main.csv - Main account database
loan.csv - Loan applications database
turnovers folder - Individual transaction histories
  each file: [account_number].csv - Per-account transaction logs

## How to Run

### Prerequisites
- Python 3.8 or higher
- PyQt5 library
- Required Python packages:
  pip install PyQt5 pandas numpy jdatetime

### Installation
1. Clone or download all project files
2. Ensure all .ui files are in the same directory as Python scripts
3. Create a turnovers folder in the project directory
4. Run the application:
   python user_interface.py

## Key Implementation Highlights

### Persian Language Support
- All UI text in Persian (Farsi) using Vazir font
- Right-to-left (RTL) layout support
- Persian date display using jdatetime

### Real-time Features
- Progress Bar Animation: Live progress during money transfers
- Dynamic Updates: Real-time balance and transaction updates
- Input Validation: Instant feedback on form inputs

### Security Features
- Account number validation before transactions
- Balance verification for withdrawals and transfers
- Manager authentication system
- Access control for account operations

### Data Persistence
- CSV-based database storage
- Individual transaction logs per account
- Loan application tracking with eligibility status

## UI Components

### Main Features Screen
Six main banking operations:
- Balance Inquiry
- Money Transfer
- Recent Transactions (3 most recent)
- Withdraw Money
- Loan Application
- Return to Main Menu

### Manager Panel
- View up to 3 pending loan applications
- See applicant details and eligibility status
- Approve or Reject with automatic database update
- Real-time feedback on actions

## Technical Details

### Libraries Used
- PyQt5: GUI framework for all UI components
- pandas: Data manipulation for loan management
- numpy: Numerical operations for data handling
- jdatetime: Persian calendar support
- csv: Built-in CSV file handling
- random: Account number generation

### Key Functions
Account creation with validation:
BankAccount(firstName, lastName, nationalCode, iaom)

Money transfer with confirmation:
transform(begin, final, value)

Loan eligibility checking:
if balance >= (wanted_amount * 30 / 100):
    eligible = True

## UI/UX Features
- Modern gradient backgrounds
- Custom-styled buttons with hover effects
- Rounded corners and shadows
- Intuitive navigation between screens
- Clear error messages in Persian
- Success confirmations with green indicators

## Example Workflow

1. Customer Login: Enter account number
2. Main Menu: Select desired operation
3. Money Transfer:
   - Enter source and destination card numbers
   - Confirm transaction details
   - Watch progress bar animation
4. View Result: Check updated balance and transaction history

## Manager Access Credentials
- ID: 5224647
- Password: Modir01
- Access to loan approval dashboard
- View and process pending applications

## Author
Arash Tahamtan

## Notes
All data is stored locally in CSV files. The application demonstrates full implementation of object-oriented programming principles in a real-world application with professional GUI design.
