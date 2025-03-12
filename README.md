I2C_SV_Verification:

This project implements the Verification module of the I2C (Inter-Integrated Circuit) communication protocol using SystemVerilog (SV). It consists of two main components:

1. I2C_Protocol_Design
This file contains the RTL design for the I2C Master and I2C Slave modules. The Master initiates communication by sending read/write requests, while the Slave responds according to the I2C protocol. The design follows standard I2C communication principles, including start/stop conditions, ACK/NACK responses, and clock synchronization.

2. I2C_Protocol_Verification
This file contains the testbench code, which verifies the I2C protocol using different SystemVerilog classes, including:

Generator: Creates randomized transactions (read/write operations with addresses and data).
Driver: Converts transactions into I2C signals and drives them into the DUT.
Monitor: Observes the bus transactions and captures the responses.
Scoreboard: Compares the expected and actual results to check correctness.
Mailbox & Events: Synchronize data between components for efficient communication.
The verification environment follows an object-oriented approach, leveraging SystemVerilog classes to create a modular and reusable testbench. UVM (Universal Verification Methodology) is not used, but the structure ensures a scalable and well-organized verification methodology.

Steps to Run the Code:
1. Copy & Run the Code in EDA Playground
Go to EDA Playground.
Select the SystemVerilog simulation environment (e.g., QuestaSim, VCS, or Xcelium).
Create two files:
Design_I2C.sv → Copy & paste the I2C Master-Slave RTL design code.
TestBench_I2C.sv → Copy & paste the testbench verification code.
2. Run the Simulation
Verify that the I2C Master and Slave modules communicate correctly under different test scenarios.
Check the waveforms (VCD file) to analyze the signal behavior.
Ensure correct data transfer using the scoreboard and monitor logs.
