# IR Object Pass-by Counter with 7-Segment Display

This project implements a **hardware-based object pass-by counter** using:
- An **IR sensor** for detecting objects
- **7490 decade counters** for counting units and tens
- **4511 BCD to 7-segment decoders** to display the count
- **7-segment displays** for visual output
- **NAND gates (7400)** and an **RC debouncing circuit** for signal conditioning

The counter displays counts from **00 to 20**, then automatically resets.

---

## 📦 Components Used
- **IR Sensor Module**
- **7490 Decade Counter ICs** (2x)
- **4511 BCD to 7-Segment Decoder ICs** (2x)
- **7-Segment Displays** (2x)
- **7400 NAND Gate IC**
- **Resistors and Capacitors** (for signal conditioning)
- **Power Supply (5V DC)**

---

## ⚙️ Features
- Counts each time an object passes the IR sensor
- Displays the count on a two-digit 7-segment display
- Resets to 00 after counting 99 objects
- Uses NAND gates and an RC filter to eliminate bounce and noise from the IR sensor
- Simple, reliable design using basic logic ICs

---

## 🔌 How It Works
1. The **IR sensor** detects passing objects and sends a pulse.
2. A **NAND gate and RC filter** condition the signal into a clean clock pulse.
3. The **7490 counter** counts units (0–9) and triggers a second **7490** for tens counting.
4. **4511 decoders** convert BCD outputs to drive **7-segment displays**.
5. When the count reaches **20**, a reset circuit resets both counters.

---

## 📚 Usage Instructions
1. Assemble the components on a **breadboard** or **PCB**.
2. Power the circuit with a **5V DC supply**.
3. Pass objects in front of the **IR sensor** to increment the counter.
4. Watch the count increment on the **7-segment displays** up to 20, then reset.

---

## 📷 Demo
*(Add a picture or video of your circuit in action here)*

---

## 📝 Future Improvements
- Add an **audio/visual alert** when reaching 20.
- Replace logic ICs with a **microcontroller (e.g. Arduino)** for more flexibility.
- Implement a **memory function** to retain count on power-off.

---

## 📄 License
This project is open-source and available under the **MIT License**.
