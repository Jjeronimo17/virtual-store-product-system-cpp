
---

# 🛒 Virtual Store – Product Management System

Console-based system developed in **C++** to organize and query products in a virtual store. Academic project for the **Data Structures and Algorithms** course.

---

## 📋 Description

The program loads a database of **120 products** from a text file and allows the user to perform **searching, sorting, and filtering** through an interactive menu.

---

## ⚙️ Features

* **Search product by name:** sorts the catalog alphabetically using **QuickSort** and locates the product using **binary search**. The search is case-insensitive.
* **Sort products by name or price:** uses **QuickSort** to sort the entire catalog alphabetically (A→Z) or by price (lowest to highest).
* **Filter by category:** iterates through the catalog and displays only products from the selected category (Electronics, Food, Clothing, Home, Sports, Stationery).
* **Show top N cheapest or most expensive products:** sorts by price using QuickSort and displays the first or last N products depending on the user’s choice.

---

## 🧠 Algorithms Implemented

| Algorithm                | Use                       | Average Complexity |
| ------------------------ | ------------------------- | ------------------ |
| QuickSort (middle pivot) | Sorting by name and price | O(n log n)         |
| Binary Search            | Search by name            | O(log n)           |
| Linear Traversal         | Category filtering        | O(n)               |

---

## 🏗️ Data Structure

```cpp id="c5k6kt"
struct Product {
    string name;
    double price;
    string category;
};
```

Products are stored in a `vector<Product>` due to:

* O(1) direct access
* Compatibility with QuickSort
* Dynamic size

---

## 📄 Data File Format

The `productos.txt` file contains 120 products with the following format:

```id="fdg3q6"
Name|Price|Category
```

They are evenly distributed across 6 categories:

* Electronics
* Food
* Clothing
* Home
* Sports
* Stationery

---

## 🚀 How to Run

1. Clone the repository
2. Make sure `productos.txt` is in the same folder as the executable
3. Compile and run:

```bash id="szpk5o"
g++ -o store main.cpp
./store
```

---

## 🛠️ Technologies

* **C++**
* **STL** (`vector`, `string`, `fstream`, `sstream`)

---
