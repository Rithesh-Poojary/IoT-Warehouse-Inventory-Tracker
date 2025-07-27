# IoT-Warehouse-Inventory-Tracker
 Automated Inventory Verification and Tracking System for Warehouses
 This project, titled "Automated Inventory Verification and Tracking System for Warehouses," leverages IoT and cloud-based technologies to address common challenges in manual inventory management, such as misplaced items and stock discrepancies. The system is designed to enhance accuracy, reduce costs, and optimize warehouse operations by minimizing manual intervention.

Features
- Automated Verification: The system uses RFID technology to automatically verify incoming products against a cloud database.
- Real-time Tracking: It provides real-time inventory status updates to stakeholders through a centralized dashboard and a custom-built Android app.
- Automated Sorting & Storage: Verified products are assigned a storage location, and a servo-controlled gate, triggered by an IR sensor, guides them to the correct slot.
- Error Prevention: Non-compliant items are rejected to prevent errors.
- Scalability: The framework is designed to be scalable for future multi-lane warehouse configurations.

Hardware Requirements
- ESP32-WROOM-DA microcontroller 
- RC522 RFID Reader 
- NFC Tags 
- IR Sensors (x2) 
- SG90 Servo Motor 
- 16x2 LCD Display 
- Breadboard & Jumper Wires 
- USB Power Supply 
- Wooden Frame (modeled conayer belt)

Software Requirements
- Arduino IDE 
- ESP32 Board Package & Libraries (including WiFi.h, Firebase_ESP_Client.h, MFRC522.h, LiquidCrystal_I2C.h, and Servo.h) 
- Firebase Console for real-time data storage and monitoring 
- Custom Android App developed with Kotlin and XML in Android Studio 


Methodology
- An IR sensor detects a product on the conveyor, activating the system.
- An RFID reader scans the product's ID tag.
- The ID is sent to a Firebase cloud database for verification via Wi-Fi.
- If verified, a slot number is assigned and shown on an LCD screen. Unverified products are rejected.
- A second IR sensor triggers a servo motor to open a gate, guiding the product to its designated slot.
- An Android app connected to the same Firebase database allows for real-time monitoring of inventory status.

Results

The system successfully automates product verification, slot allocation, and inventory tracking. It demonstrated responsiveness, accuracy in identifying and placing products, and power efficiency through a sleep/wake feature. Firebase integration ensured real-time data synchronization between the microcontroller and the mobile app, which provided immediate feedback and extended accessibility.
