# Asterisc Cafe Billing System

A simple, interactive console-based billing application built in C++ for managing cafe orders, calculating bills, and processing cash payments.

## Overview

This project simulates a cafe ordering experience where the user:

- views the menu,
- selects one or more items,
- enters quantities,
- generates a detailed bill,
- pays the total amount,
- receives change,
- ends with a thank-you message.

The system is designed for a single cashier/customer session and runs directly from the terminal.

## Features

- Interactive cafe menu display
- Item selection with quantity input
- Automatic subtotal calculation per item
- Grand total calculation
- Cash payment processing
- Change calculation
- Professional console-style bill output
- Simple, lightweight C++ implementation

## Menu Items

The application includes these menu items and prices:

| No. | Item | Price |
| --- | --- | ---: |
| 1 | Chocolate Shake | Rs. 119.00 |
| 2 | Oreo Shake | Rs. 119.00 |
| 3 | Choco Seduction | Rs. 139.00 |
| 4 | Rose Shake | Rs. 119.00 |
| 5 | Mango Shake | Rs. 119.00 |
| 6 | Strawberry Shake | Rs. 119.00 |
| 7 | Iced Tea | Rs. 89.00 |
| 8 | Peach Iced Tea | Rs. 89.00 |
| 9 | Virgin Long Island Iced Tea | Rs. 109.00 |
| 10 | Blue Lagoon | Rs. 89.00 |
| 11 | Mojito | Rs. 99.00 |
| 12 | Kiss on the Beach | Rs. 109.00 |
| 0 | Exit | — |

## How It Works

1. The program displays the full menu and welcomes the customer.
2. The cashier selects an item number from the menu.
3. The user enters the quantity for that item.
4. The program stores the order and continues prompting until the user enters `0`.
5. Once the customer exits the selection process, the bill is generated.
6. The program asks for the cash amount.
7. If the payment is less than the bill total, it prompts for the remaining amount.
8. If payment is sufficient, it calculates and prints the return amount.
9. The system displays a friendly closing message.

## Project Structure

```text
Cafe-Billing-System-main/
├── main.cpp
├── README.md
└── compiled executable (generated after build)
```

## Run the Program

### Compile

```bash
g++ main.cpp -o cafe_billing_system
```

### Run on Linux/macOS

```bash
./cafe_billing_system
```

### Run on Windows

```bash
cafe_billing_system.exe
```

## Example Workflow

```text
##### Welcome to Asterisc Cafe! #####
Menu:
1 Chocolate Shake 119/-
2 Oreo Shake 119/-
...
0 Exit
Enter your Choice : 1
Enter the Quantity : 2
Enter your Choice : 7
Enter the Quantity : 1
Enter your Choice : 0
::::: Your Bill :::::
...
Enter Your Cash: 500
Return Amount: 123.00/-
##### Thank You! #######
Please Visit Us Again
```

## Requirements

- C++ compiler (GCC, Clang, or MSVC)
- Basic terminal/command-line environment

## Notes

This application is a beginner-friendly billing system intended for learning C++ concepts such as:

- arrays and vectors,
- loops,
- object-oriented design,
- user input handling,
- arithmetic calculations,
- formatted console output.

## License

This project is provided as a learning/demo project and can be freely used or modified for educational purposes.