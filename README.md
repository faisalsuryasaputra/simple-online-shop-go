# 🛒 Online Shop Management System (Go)

![Go](https://img.shields.io/badge/go-%2300ADD8.svg?style=flat&logo=go&logoColor=white)
![Status](https://img.shields.io/badge/status-educational-yellow)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux-lightgrey)

A console-based E-Commerce application built with **Go (Golang)**. This project was developed as a final assignment for the **Algorithm and Programming** course to demonstrate the manual implementation of core computer science concepts without relying on high-level abstractions or databases.

## 📋 Project Overview

This application simulates a backend system for an online shop. It manages inventory, users, and transactions using static arrays and structs. The primary focus is on the implementation of fundamental algorithms, including:

* **Data Structures:** Structs and Arrays (Fixed size).
* **Sorting:** Manual implementation of **Selection Sort** and **Insertion Sort**.
* **Searching:** Sequential/Linear Search.
* **Validation:** Input validation and password complexity checks.

## ✨ Features

The application is divided into three main modules:

### 1. Admin Module
* **Authentication:** Secure login for administrators.
* **Master Data Management:** Add new products with automatic ID generation based on category (e.g., `P-001` for Clothes, `B-001` for Books).
* **Inventory Management:** Update stock levels for existing products.
* **Pricing:** Adjust product buying prices (automatically updates selling price with a margin).
* **Reporting:**
    * View "Dead Stock" (Products with no transactions for > 6 months).
    * View all products sorted by Brand (Merk).

### 2. User/Customer Module
* **Registration:** Create a new account with password strength validation (requires alphanumeric combination).
* **Login:** Access the shopping menu.
* **Browsing:**
    * Search products by Brand (utilizes Sorting).
    * View catalog sorted by Price (Low to High).
* **Transactions:** Buy items, calculate total costs, and automatically deduct stock.

### 3. System Utilities
* **Cross-Platform UI:** Automatically clears the terminal screen on both Windows and Linux for a cleaner user experience.
* **Data Persistence:** Uses in-memory storage (RAM) for the duration of the runtime (Arrays).

## 🧠 Algorithmic Implementation

This project focuses on the logic behind the code:

| Function | Algorithm Used | Description |
| :--- | :--- | :--- |
| `urut1` | **Insertion Sort** | Sorts data based on Name. |
| `urut2` | **Selection Sort** | Sorts data based on Brand (Merk). |
| `urut3` | **Insertion Sort** | Sorts data based on Selling Price. |
| `urut4` | **Selection Sort** | Sorts data based on Date (for dead stock analysis). |
| `validPass` | **String Traversal** | Iterates through string ASCII values to ensure alphanumeric complexity. |
| `search` | **Linear Search** | Used to find Item IDs during transactions and updates. |

## 🚀 Getting Started

### Prerequisites
* [Go (Golang)](https://go.dev/dl/) installed on your machine.

### Installation & Run
1.  Clone this repository:
    ```bash
    git clone [https://github.com/yourusername/online-shop-golang.git](https://github.com/yourusername/online-shop-golang.git)
    ```
2.  Navigate to the directory:
    ```bash
    cd online-shop-golang
    ```
3.  Run the application:
    ```bash
    go run main.go
    ```

## 🔐 Credentials

To test the **Admin** features, use the following hardcoded credentials:

* **Username:** `informatika`
* **Password:** `if10`

To test **User** features, please select Option `2` (Non Login User) to register an account first.

## 📂 Data Structure

The data is modeled using the following Go Structs:

```go
type Tanggal struct {
    tahun, bulan, hari int
}

type RecType struct {
    createuser, createpass     string // Auth
    merk, nama, jenis, id      string // Product Info
    hargabeli, hargajual       float64
    jumharga, stok             float64
    tanggal                    Tanggal // Transaction Date
}
```
🤝 Contributing
This project is for educational purposes. Suggestions for optimizing the sorting algorithms or implementing Binary Search are welcome!

✍️ Author
Faisal - Initial Work - faisalsuryasaputra
Note: As this is a CLI application using in-memory arrays, all data is lost when the program is terminated.
