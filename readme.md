# 🚗 Comic-Con Multi-Zone Parking System ER Diagram

This ER diagram models a large-scale event parking system designed for venues like Comic-Con India, where thousands of vehicles arrive across multiple days and require structured parking management.

---

## Key Features

- Support for multiple vehicle types (Bike, Car, SUV, EV, etc.)
- Multi-zone and multi-level parking structure
- Reserved parking categories (VIP, Staff, Exhibitors, Cosplayers, EV Charging)
- Automated parking spot allocation based on vehicle type and availability
- Parking session tracking with entry and exit timestamps
- Ticket generation for each parking entry
- Real-time parking availability management
- Support for multiple visits by the same vehicle across event days
- Payment tracking for each parking session

---

## Entities Included

- **Vehicles** – Stores vehicle details
- **Vehicle Categories** – Defines types of vehicles
- **Parking Zones** – Represents different parking areas and levels
- **Parking Spots** – Individual parking spaces within zones
- **Spot Categories** – Reserved parking types (VIP, Staff, EV, etc.)
- **Parking Sessions** – Tracks entry and exit of vehicles
- **Parking Tickets** – Ticket issued for each session
- **Payments** – Handles parking fee transactions

---

## Relationships Overview

- One **Vehicle** can have multiple **Parking Sessions**
- One **Parking Spot** can be reused across multiple sessions over time
- Each **Parking Spot** belongs to a **Zone**
- Each **Parking Spot** has a **Category** (General, VIP, EV, etc.)
- Each **Session** generates one **Ticket**
- Each **Session** is linked to a **Payment**

---

## Design Highlights

- **Parking Session is the central entity**, connecting:
  - Vehicle
  - Parking Spot
  - Ticket
  - Payment

- Proper separation of:
  - Entry/Exit tracking (Session)
  - Billing (Payment)
  - Resource allocation (Parking Spot)

- Ensures:
  - Scalability for large events
  - Efficient parking space reuse
  - Accurate tracking of currently parked vehicles
