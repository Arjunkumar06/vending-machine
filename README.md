# Vending Machine Simulation using State Design Pattern

## Author

**Arjunkumar**

## Project Overview

This project is a Java-based simulation of a vending machine implemented using the **State Design Pattern**. The application demonstrates how object behavior changes dynamically based on its internal state.

The vending machine can handle different scenarios such as:

* Inserting a coin
* Ejecting a coin
* Pressing a button
* Dispensing a product
* Refilling inventory
* Handling sold-out situations

The project illustrates clean state transitions and avoids large conditional statements by encapsulating behavior into separate state classes.

## Design Pattern Used

### State Design Pattern

The State Design Pattern allows an object to alter its behavior when its internal state changes.

### States Implemented

1. **NoCoinState**

   * Machine waiting for a coin
   * Allows coin insertion
   * Prevents purchase without payment

2. **HasCoinState**

   * Coin inserted successfully
   * Allows button press or coin ejection
   * Prevents inserting multiple coins

3. **DispenseState**

   * Dispenses the selected product
   * Updates inventory
   * Handles inventory checks

4. **SoldOutState**

   * Activated when inventory reaches zero
   * Rejects transactions
   * Allows machine refill

## Project Structure

```text
VendingMachineMain.java
│
├── State Interface
│
├── VendingMachine (Context Class)
│
├── NoCoinState
│
├── HasCoinState
│
├── DispenseState
│
└── SoldOutState
```

## Features

* Object-oriented implementation
* State Design Pattern usage
* Inventory management
* Product dispensing
* Coin insertion/ejection
* Refill functionality
* Error handling for invalid actions
* Automatic state transitions

## How to Compile

Open terminal and run:

```bash
javac VendingMachineMain.java
```

## How to Execute

Run:

```bash
java VendingMachineMain
```

## Sample Output

```text
--- Booting up Vending Machine (Inventory: 2) ---

[1: Happy Path]
Coin inserted.
Button pressed...
A product comes rolling out the slot...

[2: Invalid Action (Eject without coin)]
You haven't inserted a coin.

[3: Ejecting Coin before dispense]
Coin inserted.
Coin returned.

[4: Buying the last item]
Coin inserted.
Button pressed...
A product comes rolling out the slot...

Oops, out of inventory!

[5: Trying to buy when sold out]
You can't insert a coin, the machine is sold out.

[6: Refilling the machine]
Machine refilled. Total inventory: 5
```

## Learning Outcomes

This project helps understand:

* State Design Pattern implementation
* Object-Oriented Programming concepts
* Encapsulation
* Polymorphism
* Dynamic behavior handling
* Real-world software design approaches

## Future Improvements

* Support multiple product types
* Add product selection feature
* Add digital payment support
* Display remaining inventory
* Create GUI interface using Java Swing/JavaFX

## License

This project is developed for educational purposes.
