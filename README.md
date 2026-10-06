# 🚗 Vehicle Rental System

A simple **Vehicle Rental System built using Python and Object-Oriented Programming (OOP)**. This project allows users to view available vehicles, rent vehicles, return rented vehicles, and view customer details through a simple console-based menu.

## 📌 About the Project

The Vehicle Rental System is a console-based Python application designed to demonstrate the practical use of **Object-Oriented Programming concepts**.

The system manages different types of vehicles such as **Cars, Bikes, and SUVs**. Users can rent an available vehicle for a specific number of days, calculate the total rental cost, return the vehicle, and view registered customers.

## ✨ Features

* 🚘 Display all available and rented vehicles
* 🔑 Rent a vehicle using Vehicle ID
* 🔄 Return a rented vehicle
* 👤 Automatically generate Customer IDs
* 📋 Display registered customer details
* 💰 Calculate total rental cost based on number of days
* ⚠️ Handle invalid user input
* 📊 Track vehicle availability
* 🖥️ Simple menu-driven console interface

## 🛠️ Technologies Used

* **Python 3**
* **Object-Oriented Programming (OOP)**
* Abstract Base Classes
* Inheritance
* Encapsulation
* Polymorphism
* Exception Handling

## 🧠 OOP Concepts Used

### 1. Abstraction

The `Vehicle` class is an abstract base class using Python's `ABC` module.

```python
class Vehicle(ABC):
```

The `calculate_rent()` method is defined as an abstract method:

```python
@abstractmethod
def calculate_rent(self, days):
    pass
```

### 2. Inheritance

The `Car`, `Bike`, and `SUV` classes inherit from the `Vehicle` class.

```python
class Car(Vehicle):
class Bike(Vehicle):
class SUV(Vehicle):
```

### 3. Encapsulation

Vehicle information is stored using private attributes such as:

```python
self.__vehicle_id
self.__brand
self.__model
self.__rent_per_day
self.__available
```

Getter and setter methods are used to access and modify the data.

### 4. Polymorphism

Each vehicle type implements the `calculate_rent()` method.

```python
def calculate_rent(self, days):
    return days * self.get_rent_per_day()
```

This allows the rental system to calculate the rent through the common `Vehicle` interface.

### 5. Exception Handling

The project uses `try-except` blocks to handle invalid inputs, such as entering text where a number is expected.

```python
try:
    vehicle_id = int(input("Enter Vehicle ID: "))
except ValueError:
    print("Please enter a valid Vehicle ID.")
```

## 🚘 Vehicles Included

| Vehicle ID | Brand         | Model       | Rent Per Day |
| ---------- | ------------- | ----------- | -----------: |
| 101        | Toyota        | Camry       |        ₹1500 |
| 102        | Royal Enfield | Classic 350 |         ₹700 |
| 103        | Mahindra      | XUV700      |        ₹2500 |

## 📂 Project Structure

```text
Vehicle-Rental-System/
│
├── vehicle_rental_system.py
└── README.md
```

> The Python file name can be changed according to the name of your actual `.py` file.

## ▶️ How to Run

### 1. Clone the repository

```bash
git clone https://github.com/your-username/vehicle-rental-system.git
```

### 2. Open the project folder

```bash
cd vehicle-rental-system
```

### 3. Run the Python program

```bash
python vehicle_rental_system.py
```

## 🖥️ Menu

When the program starts, it displays:

```text
=======================================================================
VEHICLE RENTAL SYSTEM
=======================================================================
1. Show Vehicles.
2. Rent Vehicle.
3. Return Vehicle.
4. Show Customers.
5. Exit
```

### Example

To rent the Toyota Camry:

```text
Enter your choice: 2
Enter Vehicle ID: 101
Enter customer name: Vaishnavi
Enter phone number: 9876543210
Enter number of days: 3
```

The total rent will be calculated automatically:

```text
Rent/Day: ₹1500
Total Rent: ₹4500
```

After renting, the vehicle status changes from **Available** to **Rented**.

When the vehicle is returned, its status changes back to **Available**.

## 🎯 Learning Outcomes

Through this project, I practiced:

* Designing classes and objects in Python
* Implementing abstraction and inheritance
* Understanding encapsulation and private attributes
* Applying polymorphism
* Handling user input and exceptions
* Building a menu-driven console application
* Managing vehicle and customer data using Python lists

## 🔮 Future Improvements

Some features that can be added in the future:

* 📅 Rental history
* 👤 Customer login and registration
* 💳 Payment management
* 🗄️ Database integration using MySQL or SQLite
* 🌐 Web-based interface
* 🔍 Vehicle search and filtering
* 📊 Admin dashboard
* 📧 Rental confirmation notifications

## 👨‍💻 Author

**Vaishnavi Pokhriyal**

B.Tech CSE Student | Python | AI & Data Science | Web Development

---

⭐ If you found this project useful, feel free to give the repository a star!
