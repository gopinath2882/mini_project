# mini_projecJ
![Restaurant Order Management System Block Diagram]<img width="1774" height="887" alt="fdb9c46f-4e6f-4ae2-a8a0-bbe6d2c6ba76" src="https://github.com/user-attachments/assets/25d8b529-5feb-445a-85bb-dcd9f55602b4" />
Restaurant Order Management System Using LPC2129 (ARM7)
Here is the project illustration and the important details for your project presentation, record, and viva.
Project image: Hardware arrangement, pin connections, components, working procedure, applications, and LCD output examples.
1. Problem statement
Traditional restaurant order management relies on manual order-taking and verbal communication between waiters and kitchen staff. This can cause order errors, delays, and miscommunication. The proposed system automates table selection and food ordering using an LPC2129 ARM7 microcontroller, keypad, and LCD. It uses an HC-05 Bluetooth module to transmit orders to a mobile phone and receive the chef's order-ready response.
2. Abstract
The Restaurant Order Management System is an embedded system designed to simplify restaurant order processing. It uses an LPC2129 ARM7 microcontroller as the main controller. A 4×4 matrix keypad allows users to select a table, choose food items, adjust quantities, clear orders, and confirm orders. A 16×2 LCD displays table information, menu selections, and order status. An HC-05 Bluetooth module enables wireless communication between the microcontroller and a paired mobile phone through UART0. The chef can send a readiness message from the phone, which is detected by the controller and displayed on the LCD. This project demonstrates the practical application of embedded C programming, GPIO interfacing, LCD interfacing, keypad scanning, UART communication, and Bluetooth technology.
3. Components required
Component	Purpose
LPC2129 ARM7 development board	Processes inputs and controls the system
16×2 LCD	Displays menu and order status
4×4 matrix keypad	Selects tables and food items
HC-05 Bluetooth module	Sends and receives order messages wirelessly
Power supply	Powers the circuit
Connecting wires / breadboard or PCB	Provides electrical connections
Computer with Keil µVision	Develops and compiles the embedded C program
Bluetooth terminal app	Exchanges messages with the microcontroller
4. Uses and applications
- Automates restaurant order entry.
- Reduces manual communication errors.
- Sends food orders wirelessly to the kitchen's paired mobile phone.
- Tracks orders by table number.
- Provides order-ready notifications.
- Can be adapted for cafés, hotels, food courts, and small restaurants.
5. Working procedure
1. Initialize the LPC2129, LCD, keypad GPIO, and UART0.
2. Display the welcome message on the LCD.
3. Select a table number from 1 to 9.
4. Select food items: 1 = Dosa, 2 = Idli, 3 = Meal, 4 = Tea.
5. Press a menu key repeatedly to increase its quantity.
6. Press * to clear the order or # to confirm it.
7. Send the table number and order details to the mobile phone through HC-05 Bluetooth.
8. The chef sends a readiness message from the paired mobile phone.
9. Display “Order is READY!” on the LCD.
6. Important pin connections
Function	LPC2129 pin
UART0 TXD	P0.0
UART0 RXD	P0.1
LCD data D0–D7	P0.16–P0.23
LCD RS	P0.8
LCD E	P0.9
LCD RW	GND
Keypad rows	P0.10–P0.13
Keypad columns	P0.4–P0.7
Important: The keypad column inputs require suitable pull-up resistors, and the HC-05 UART signal levels must be compatible with the LPC2129's 3.3 V logic.
7. Expected result
The system displays the selected table and menu, transmits confirmed orders to a paired mobile phone, and displays an order-ready notification when the chef's reply is received.
8. Conclusion
This project provides a simple, low-cost solution for restaurant order communication using embedded technology. It combines the LPC2129 ARM7 microcontroller, LCD, keypad, UART, and Bluetooth to improve order processing and reduce communication errors.
