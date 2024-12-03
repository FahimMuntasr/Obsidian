# Introduction
The Delivery Tracker is a modular, object-oriented system designed to manage various types of deliveries, such as food and parcel deliveries. It calculates delivery fees dynamically based on user-provided data and includes robust exception handling for enhanced reliability.

---

# Project Objectives

- To provide a structured, extensible solution for handling diverse delivery types.
- To dynamically compute delivery fees based on customizable parameters.
- To ensure error resilience through custom exception handling.
- To offer an intuitive user interface for system interaction.

---

# Package Structure

The system is divided into three main packages:

1. `application`: Contains GUI and file handling
	- `DeliveryUI` (console-based user interface class)
2. `delivery`: Contains core classes for the delivery system:
	- `Delivery` (abstract base class)
	- `FoodDelivery` (specialized subclass for food deliveries)
	- `ParcelDelivery` (specialized subclass for parcel deliveries)
3. `exceptions`: Contains custom exception classes for robust error handling.
	- `ConflictingID`
	- `InvalidInputLength`
	- `NegativeInput`
	- `NonAlphabetInput`
	- `NonNumericInput`



---
``
# Application Package
### DeliveryUI class

#### **Overview**

The `DeliveryUI` application provides a user-friendly graphical interface for managing delivery services, which include both **Food Delivery** and **Parcel Delivery**. It allows users to calculate delivery fees, store customer information, and manage records via file operations. The program utilizes Java Swing components for the user interface and custom exceptions for robust error handling.
#### **Key Functionalities**

1. **Form Input Handling**
    - A detailed form collects delivery-related inputs such as:
        - Delivery ID
        - Customer Name
        - Contact Number
        - Address
        - Delivery Type (Food or Parcel Delivery)
        - Additional features like online payment, express delivery, and fragile options.
    - Specific inputs (e.g., tip for food delivery, weight for parcel delivery) are dynamically enabled/disabled based on the selected delivery type.
2. **Dynamic Table View**
    - A `JTable` dynamically displays delivery details, including:
        - Delivery ID, Customer Name, District, Fee, and other attributes.
    - Allows users to view and manage delivery records effectively.
3. **Delivery Type Management**
    - Two delivery types:
        - **Food Delivery**: Includes tip management.
        - **Parcel Delivery**: Includes weight and fragile options.
    - The fee calculation logic is encapsulated in separate classes: `FoodDelivery` and `ParcelDelivery`.
4. **Error Handling with Custom Exceptions**
    - Custom exceptions ensure data integrity and user feedback:
        - `ConflictingID`: Prevents duplicate Delivery IDs.
        - `InvalidInputLength`: Validates input lengths for Delivery IDs and contact numbers.
        - `NegativeInput`: Disallows negative numeric values.
        - `NonAlphabetInput` and `NonNumericInput`: Validate text and numeric inputs.
5. **File Operations**
    - **Load**: Reads saved delivery records from a file and populates the table.
    - **Save**: Writes current delivery records to a file.
    - Uses `BufferedReader` and `BufferedWriter` for file I/O operations.
6. **Update and Delete Functionality**
    - **Update**: Modifies existing records based on the Delivery ID.
    - **Delete**: Removes a record, ensuring the ID is also removed from the internal array.
7. **Validation Logic**
    - Extensive input validation ensures data integrity and compliance with requirements:
        - Delivery ID must be numeric and 4 characters long.
        - Contact numbers must be exactly 11 numeric digits.
        - Negative inputs are strictly disallowed for numeric fields.
        - Names must consist only of alphabetical characters.

# Delivery Package
### Delivery class

#### **Overview**
The `Delivery` class is designed as an abstract representation of a delivery service system. It contains the fundamental properties and behaviors associated with a delivery request, such as delivery ID, recipient details, base fee, and delivery method preferences (priority and online payment). The class is structured to be extended by concrete subclasses that will implement specific delivery types, each with its own method for calculating the delivery fee.
#### **Key Functionalities**

1. **Storing data in an object**
	- `DeliveryId`,`name`,`contact`,`district`,`address`,`baseFee`,`priority`,`onlinePayment` 
2. **Implements Encapsulation**
	- Access modifiers set to private
	- Data only accessible through getters and setters
### FoodDelivery class
#### **Overview**
The `FoodDelivery` class extends the base **Delivery** class to represent a food delivery service. It introduces an optional `tip` attribute and overrides the `calculateFee` method to include specific fee calculations for food deliveries.
#### **Key Features**

1. **Fee Calculation Logic**:
    - Uses the inherited `getBaseFee` method and adds the `tip`.
    - Dynamically adjusts fees based on:
        - **Priority Delivery:** Applies a surcharge proportional to the base fee.
        - **Online Payment:** Adds an additional fee proportional to the base fee.
2. **Encapsulation**:
    - All attributes (`tip`) are private, with public getters and setters for controlled access.
3. **Inheritance**:
    - Leverages the parent class **Delivery** for shared functionality like base fee, priority status, district, and online payment options.
### ParcelDelivery class
#### **Key Features**

1. **Advanced Fee Calculation**:
    - Dynamically adjusts fees based on multiple parameters (e.g., weight, fragility, location).
    - Handles overweight charges proportionally using a weight percentage formula.
2. **Encapsulation**:
    - Attributes are private, with controlled initialization through constructors.
3. **Inheritance**:
    - Effectively reuses the attributes and methods of the **Delivery** base class.
4. **Constants for Fixed Charges**:
    - Constants (`fragileFee`, `weightLimit`, `outsideCityFee`) make the code easy to maintain and modify.
5. **District-Based Logic**:
    - Automatically determines if the delivery is outside Dhaka based on the `district` parameter.
# Exception Package
### **Overview**
The exception package contains custom exceptions that check for conflicting ID, invalid Input Length, Negative Inputs, Non Alphabet Inputs and Non Numeric Inputs