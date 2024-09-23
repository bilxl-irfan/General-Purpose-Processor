# General-Purpose Processor

## Project Overview
This project focuses on designing a General-Purpose Processor, developed as part of a Digital Systems course. The processor was built using combinational and sequential circuits, incorporating an Arithmetic Logic Unit (ALU), latches, and a control unit with a Finite State Machine (FSM) and a 4:16 decoder. The processor performs operations on two 8-bit inputs based on the FSM's state and a 16-bit control signal from the decoder. The results are displayed on 7-segment displays, and functionality was verified through waveform analysis.

## Components

### 1. **Arithmetic Logic Unit (ALU)**
The ALU is responsible for executing operations dictated by the FSM and decoder. Inputs include A, B, OP, and Student ID, with the ALU performing operations based on the rising clock edge. The ALU outputs include:  
- `Neg`: Triggers the 7-segment display for negative results.  
- `R1`: Displays the first 4 bits of the 8-bit result.  
- `R2`: Displays the last 4 bits of the 8-bit result.

### 2. **7-Segment Display**
The 7-segment display converts binary input from the ALU into decimal and hexadecimal outputs, ranging from 0-15. It also displays negative values when necessary.

### 3. **4:16 Decoder**
The decoder translates a 4-bit input from the FSM into a 16-bit microcode, helping manage operation selection for the CPU.

### 4. **Finite State Machine (FSM)**
The FSM cycles through 9 states (S0 to S8), controlling the processor’s operations. It outputs state changes to the 4:16 decoder, ensuring proper execution sequencing.

### 5. **Latches**
Two D latches are used to store inputs A and B from the FPGA, passing their values on the clock’s positive edge to the processor.

## Summary
This project successfully integrated all components to create a fully functional general-purpose processor. Each part contributed to the overall operation, enabling efficient data processing and output display.

---

Feel free to fork, contribute, or raise issues as needed.
