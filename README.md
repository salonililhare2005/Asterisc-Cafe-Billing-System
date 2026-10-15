<div align="center">

# ☕ Asterisc Cafe Billing System

**A friendly, interactive console application for taking cafe orders, generating bills, and handling cash payments — built in C++.**

![Language](https://img.shields.io/badge/Language-C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![Interface](https://img.shields.io/badge/Interface-CLI-4EAA25?style=for-the-badge&logo=gnubash&logoColor=white)
![Level](https://img.shields.io/badge/Level-Beginner--Friendly-brightgreen?style=for-the-badge)
![Purpose](https://img.shields.io/badge/Purpose-Educational-blueviolet?style=for-the-badge)

[Overview](#-overview) •
[Features](#-features) •
[Menu](#-the-menu) •
[Quick Start](#-quick-start) •
[How It Works](#%EF%B8%8F-how-it-works) •
[Demo](#-example-session)

</div>

---

## 📖 Overview

Welcome to **Asterisc Cafe**! 👋

This project brings a cafe counter to your terminal. A cashier can browse the menu, add items to an order, and generate a clean, itemised bill — then accept cash and calculate the change, all in a single smooth session.

The customer journey looks like this:

```text
 📋 View Menu ─▶ 🥤 Pick Items ─▶ 🔢 Enter Quantities ─▶ 🧾 Get Bill ─▶ 💵 Pay ─▶ 🪙 Receive Change ─▶ 🙏 Thank You!
```

The system is designed for a **single cashier/customer session** and runs directly from the command line.

---

## ✨ Features

| Feature | Description |
|:--|:--|
| 📋 **Interactive Menu** | Clearly numbered menu with item names and prices |
| 🛒 **Multi-Item Orders** | Add as many items as you like, each with its own quantity |
| ➗ **Automatic Subtotals** | Calculates the cost of every line item instantly |
| 🧾 **Grand Total** | Sums the full order into a single payable amount |
| 💵 **Cash Payments** | Accepts cash and prompts for the balance if payment falls short |
| 🪙 **Change Calculation** | Works out the exact return amount for the customer |
| 🖨️ **Professional Bill Output** | Neatly formatted, receipt-style bill in the console |
| ⚡ **Lightweight** | Pure C++ with no external dependencies |

---

## 🍹 The Menu

<table>
<tr>
<td valign="top">

### 🥤 Shakes

| No. | Item | Price |
|:--:|:--|--:|
| 1 | Chocolate Shake | ₹119.00 |
| 2 | Oreo Shake | ₹119.00 |
| 3 | Choco Seduction | ₹139.00 |
| 4 | Rose Shake | ₹119.00 |
| 5 | Mango Shake | ₹119.00 |
| 6 | Strawberry Shake | ₹119.00 |

</td>
<td valign="top">

### 🧊 Coolers & Mocktails

| No. | Item | Price |
|:--:|:--|--:|
| 7 | Iced Tea | ₹89.00 |
| 8 | Peach Iced Tea | ₹89.00 |
| 9 | Virgin Long Island Iced Tea | ₹109.00 |
| 10 | Blue Lagoon | ₹89.00 |
| 11 | Mojito | ₹99.00 |
| 12 | Kiss on the Beach | ₹109.00 |

</td>
</tr>
</table>

> 🚪 Enter **`0`** at any time during selection to finish the order and generate the bill.

---

## 🚀 Quick Start

Get the cafe open in under a minute.

### ✅ Prerequisites

- A C++ compiler — **GCC**, **Clang**, or **MSVC**
- A terminal or command-line environment

### 🐧 Linux / 🍎 macOS

```bash
# 1. Compile
g++ main.cpp -o cafe_billing_system

# 2. Run
./cafe_billing_system
```

### 🪟 Windows

```cmd
:: 1. Compile
g++ main.cpp -o cafe_billing_system.exe

:: 2. Run
cafe_billing_system.exe
```

> 💡 **Tip:** Add `-std=c++17 -Wall` to the compile command for a modern standard and helpful warnings.

---

## ⚙️ How It Works

| Step | Stage | What happens |
|:--:|:--|:--|
| 1️⃣ | **Welcome** | The program greets the customer and displays the full menu |
| 2️⃣ | **Select** | The cashier enters an item number from the menu |
| 3️⃣ | **Quantity** | The quantity for that item is entered |
| 4️⃣ | **Repeat** | The order is saved and the prompt repeats until `0` is entered |
| 5️⃣ | **Bill** | An itemised bill with the grand total is generated |
| 6️⃣ | **Payment** | The program asks for the cash amount |
| 7️⃣ | **Shortfall Check** | If the cash is less than the total, it asks for the remaining amount |
| 8️⃣ | **Change** | If payment is sufficient, the return amount is calculated and shown |
| 9️⃣ | **Goodbye** | A friendly thank-you message closes the session |

```text
            ┌──────────────┐
            │  Show Menu   │
            └──────┬───────┘
                   ▼
            ┌──────────────┐   choice ≠ 0
     ┌────▶ │ Select Item  │ ─────────────┐
     │      └──────┬───────┘              ▼
     │             │ choice = 0    ┌──────────────┐
     │             ▼               │Enter Quantity│
     │      ┌──────────────┐       └──────┬───────┘
     │      │ Generate Bill│              │
     │      └──────┬───────┘              │
     │             ▼                      │
     │      ┌──────────────┐              │
     │      │  Enter Cash  │ ◀─┐          │
     │      └──────┬───────┘   │ short    │
     │             ▼           │          │
     │      ┌──────────────┐   │          │
     │      │ Enough cash? │ ──┘          │
     │      └──────┬───────┘              │
     │             │ yes                  │
     │             ▼                      │
     │      ┌──────────────┐              │
     │      │Return Change │              │
     │      │ & Thank You  │              │
     │      └──────────────┘              │
     └────────────────────────────────────┘
```

---

## 🎬 Example Session

<details open>
<summary><b>▶️ Sample order: 2 × Chocolate Shake + 1 × Iced Tea</b></summary>

<br>

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
Return Amount: 173.00/-
##### Thank You! #######
Please Visit Us Again
```

**Bill breakdown:**

| Item | Qty | Rate | Amount |
|:--|:--:|--:|--:|
| Chocolate Shake | 2 | ₹119.00 | ₹238.00 |
| Iced Tea | 1 | ₹89.00 | ₹89.00 |
| **Grand Total** | | | **₹327.00** |
| Cash Received | | | ₹500.00 |
| **Change Returned** | | | **₹173.00** |

</details>

---

## 📁 Project Structure

```text
Cafe-Billing-System-main/
├── main.cpp                # Application source code
├── README.md               # Project documentation
└── cafe_billing_system     # Compiled executable (generated after build)
```

---

## 🎓 What You'll Learn

This beginner-friendly project is a great way to practise core C++ concepts:

- 📦 **Arrays and vectors** — storing menu items and orders
- 🔁 **Loops** — repeating prompts until the order is complete
- 🧱 **Object-oriented design** — organising code into clear components
- ⌨️ **User input handling** — reading choices, quantities, and cash
- ➗ **Arithmetic calculations** — subtotals, totals, and change
- 🖨️ **Formatted console output** — printing a neat, aligned bill

---

## 🗺️ Roadmap

Ideas to take the cafe to the next level:

- [ ] 🧾 Add GST / tax calculation to the bill
- [ ] 💳 Support UPI and card payment modes
- [ ] 💾 Save bills to a file for record-keeping
- [ ] ✏️ Allow removing or editing items before billing
- [ ] 📂 Load the menu from a file so prices are easy to update
- [ ] 📊 Generate a daily sales summary

---

## 🤝 Contributing

Have an idea for a new feature or a tastier menu? Contributions are welcome! 🎉

1. **Fork** the repository
2. **Create** a feature branch: `git checkout -b feature/your-feature`
3. **Commit** your changes: `git commit -m "Add your feature"`
4. **Push** the branch: `git push origin feature/your-feature`
5. **Open** a Pull Request

---

## 📄 License

This project is provided as a **learning and demo project** and may be freely used or modified for educational purposes.

<div align="center">

---

☕ **Thanks for stopping by Asterisc Cafe — please visit us again!** ☕

⭐ *If you enjoyed this project, consider giving it a star!* ⭐

</div>
