# GSM SMS & Call System using LPC2148 (ARM7)

This project demonstrates how to use the **LPC2148 ARM7 microcontroller** with a **GSM module (SIM800L)** to receive SMS messages, respond via SMS, and make automated voice calls.

## 📱 Features

- Receive SMS using GSM module
- Check if message contains **"call me"**
- Reply with a message: *"I am Sanket Mali"*
- Initiate a call to the sender
- Automatically hang up after a delay
- Deletes the message to save SIM storage

## 🔧 Hardware Requirements

- LPC2148 ARM7 Development Board
- SIM800L GSM Module
- 12V Power Supply (recommended for GSM)
- RS232 Level Converter / UART Connection
- SIM card with valid balance

## 🔌 Connections

| GSM Module | LPC2148 (UART0) |
|------------|------------------|
| TX         | P0.1 (RXD0)      |
| RX         | P0.0 (TXD0)      |
| GND        | GND              |
| VCC        | 4V - 5V (external supply) |

## 🛠 Software Details

- IDE: Keil uVision or any ARM7 supported toolchain
- Compiler: ARM RealView / GCC for ARM
- Communication: UART0 @ 9600 baud
- Written in C
- Interrupt-driven UART receive

## 📂 File Structure


## 🔄 Working Principle

1. **System Initialization**:
   - UART0 is configured.
   - GSM is initialized using `AT` commands.

2. **SMS Detection**:
   - GSM module receives an SMS.
   - If it contains `"call me"`, the system responds with an SMS saying *"I am Sanket Mali"*.

3. **Call Functionality**:
   - A call is initiated to the sender's number.
   - After 15 seconds, the call is disconnected automatically.

4. **Clean-up**:
   - The received message is deleted from the SIM memory.

## 🧪 How to Test

1. Power your GSM module separately (5V, 2A).
2. Upload the code to LPC2148.
3. Insert a working SIM card (no PIN lock).
4. Send an SMS with: `call me`
5. Watch the system:
   - Responds with an SMS
   - Calls the sender
   - Disconnects after 15 sec
   - Deletes the SMS

## 👨‍💻 Author

**Sanket Mali**  
Department of Electronics and Telecommunication  
Project for Embedded Systems / IoT Applications

---

> *This embedded project is ideal for learning GSM communication, interrupt-driven UART, and automation using ARM7 (LPC2148).*

