   Supermarket Management System

Project Title
**Supermarket Management System** - A Python-based retail management solution

Overview
The Supermarket Management System is a comprehensive console-based application designed to streamline supermarket operations. It provides distinct interfaces for customers and employees, enabling efficient product management, shopping cart functionality, and inventory control. The system organizes products into five logical phases (categories) and offers a seamless experience for both shoppers and staff members.

Features

Customer Features
- **Shopping Cart System**: Add multiple items with quantities
- **Product Validation**: Real-time checking of product availability
- **Automatic Pricing**: Calculate totals based on quantity and price
- **Detailed Receipts**: Professional bill generation with itemized breakdown
- **Phase Information**: Show product location within supermarket layout

Employee Features
- **Inventory Management**: Add, remove, and update products
- **Price Control**: Modify product pricing dynamically
- **Product Categorization**: Organize items into 5 phases
- **Complete Inventory View**: Display all products with details
- **Access Control**: Separate interface for management tasks

System Features
- **Dual User Interface**: Separate workflows for customers and employees
- **Input Validation**: Comprehensive error handling and data validation
- **Real-time Calculations**: Instant price and total computations
- **User-Friendly Menu**: Intuitive navigation system

Technologies Used

Programming Language
- **Python 3.6+** - Core programming language

Standard Libraries
- No external dependencies required
- Uses built-in Python modules only

Architecture
- **Object-Oriented Programming (OOP)**
- **Modular Design**
- **In-Memory Data Storage**
- **Console-Based Interface**

Key Programming Concepts
- Classes and Objects
- Dictionaries for data management
- Lists for shopping cart operations
- Input/Output handling
- Conditional statements and loops
- Error handling with try-except blocks

Installation Steps

Prerequisites
- Python 3.6 or higher installed on your system
- Basic terminal/command prompt knowledge

Step-by-Step Installation

1. **Download the Project**
   # Clone or download the supermarket.py file to your local machine

2.Verify Python Installation
  python --version
  # Should show Python 3.6 or higher

3.Navigate to Project Directory
  cd path/to/project/directory

4.Ready to Run
   No additional packages or installations required
   System is ready to use

Running the Project

Execution Command
python supermarket.py

Initial Setup
Open terminal/command prompt
Navigate to project directory
Run the command above
System starts immediately
First Run Experience
Application loads instantly
No configuration required
Sample products pre-loaded
Ready for immediate use


Project Infrastructure

File Structure
supermarket_management/
├── supermarket.py      # Main application file
├── README.md          # Project documentation
└── (optional test files)

Data Storage
Type: In-memory storage during runtime
Structure: Python dictionaries and lists
Persistence: Session-based (resets on application close)
Backup: No external file dependencies

System Architecture
Input Layer → Processing Layer → Output Layer
    ↓              ↓              ↓
User Input → Business Logic → Console Output
Testing Infrastructure

Manual Testing Steps

1. Customer Functionality Testing
# Test Case 1: Basic Shopping
1. Run application
2. Select '1' for Customer
3. Enter 'milk'
4. Enter quantity '2'
5. Enter 'bread'
6. Enter quantity '1'
7. Type 'done'
8. Verify receipt totals


2. Employee Functionality Testing
# Test Case 2: Inventory Management
1. Run application
2. Select '2' for Employee
3. Select '1' to Add Item
4. Enter: name='test', phase=1, price=100
5. Select '4' to View Items (verify addition)
6. Select '3' to Update Price
7. Enter: name='test', new_price=150
8. Select '2' to Remove Item
9. Enter: name='test'

3. Error Handling Testing
# Test Case 3: Input Validation
1. Test invalid product names
2. Test negative quantities
3. Test invalid phase numbers
4. Test non-numeric prices
5. Verify error messages are user-friendly



Test Scenarios

Scenario 1: Complete Customer Journey
Add multiple items with different quantities
Verify phase information in receipt
Check total calculation accuracy
Test 'done' command functionality



Scenario 2: Employee Management Cycle
Add new product → Verify addition → Update price → Verify update → Remove product → Verify removal



Scenario 3: Boundary Testing
Maximum quantity values
Phase number boundaries (1-5)
Price range testing
Special character inputs


Expected Output Verification
Customer Receipt Should Show:
Sequential item numbering
Proper product names (title case)
Correct phase numbers
Accurate individual prices
Correct quantities
Proper line totals
Accurate grand total

Employee Operations Should:
Provide success confirmation messages
Show updated inventory immediately
Handle errors gracefully
Maintain data consistency

System Requirements

Minimum Requirements
OS: Windows 7+, macOS 10.9+, or Linux
RAM: 512 MB minimum
Storage: 10 MB free space
Python: Version 3.6 or higher

Recommended Requirements
OS: Windows 10, macOS 11+, or Ubuntu 18.04+
RAM: 1 GB or more
Storage: 50 MB free space
Python: Version 3.8 or higher

Support
For issues or questions:
Check Python version compatibility
Verify file execution permissions
Ensure correct command syntax
Review error messages in console
License
Open-source project for educational and commercial use.

