ShipFlow - Shipment Order Processing System

Project Overview
This project is a Java console application for processing different types of shipment orders.

It demonstrates core object-oriented programming concepts:
- Interface
- Abstract class
- Inheritance
- Polymorphism
- Template Method design pattern

Design Pattern

This project uses the Template Method design pattern.

The abstract class ShipmentOrder defines the main algorithm in the processOrder() method.
Subclasses implement specific steps such as price calculation and additional fees.



processOrder()

This method defines a fixed sequence of steps:
- Order validation
- Specific rules validation
- Base price calculation
- Additional fee calculation
- Insurance application
- Business discount
- Saving and printing result

Subclasses implement only the variable parts of the algorithm without changing the overall process.

Project Structure

Interface
SummaryPrintable
Defines:
String buildSummaryLine();

Abstract Class
ShipmentOrder

Stores shared data:
- orderNumber
- customerName
- distanceKm
- baseFee
- insured
- lastCalculatedPrice

Contains:
- final processOrder() method
- validation methods
- insurance and discount logic
- summary generation

Concrete Classes

DomesticCourierShipment
- Adds packageWeightKg and weekendDelivery
- Applies weight-based and weekend fees
- Applies discount for long distances

PickupPointShipment
- Adds lockerSize and fragile
- Applies size-based pricing
- Adds fragile fee
- Validates locker size

InternationalShipment
- Adds destinationCountry, customsDocumentsRequired, expressDelivery
- Applies international pricing rules
- Adds customs and express fees
- Applies discount for long non-express deliveries

Main Class

The Main class creates multiple shipment objects and processes them using a loop.
Each order is processed using processOrder() and summarized using buildSummaryLine().

How to Run

1. Open the project in IntelliJ IDEA
2. Run Main.java
3. The program will process all shipment orders and print results in the console

Author

Student project for Java course (PGO)
