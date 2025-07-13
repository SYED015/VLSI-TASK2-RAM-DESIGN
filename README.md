# VLSI-TASK2-RAM-DESIGN

COMPANY: CODTECH IT SOLUTIONS

NAME: SYED TAUSEEF ASHRAF

INTERN ID: COMPANY: CT06DF1544

DOMAIN: VLSI

DURATION: 6 WEEKS

MENTOR: NEELA SANTOSH

In task 2 of my internship, I received the development of a simple synchronous RAM module with basic reading and recording operations using Verilog. This task aimed to strengthen my understanding of memory modules in digital design and implement them through hardware description languages. According to the task instructions, deliveries included the Verilog code, a check test and simulation results demonstrating the RAM functionality.

To achieve this, I used the Playground EDA, an online simulation platform that supports Verilog and provides embedded tools such as Icarus Verilog 12.0 for compilation and open Epwave for waveform viewing. This platform allowed me to codify, simulate and observe outputs directly in the browser, making the design and clearance process much more efficient and affordable.

The RAM module I implemented was a synchronous memory block, which means that reading and recording operations are performed in sync with the upward edge of the watch signal. Design accepts inputs such as a clock sign (CLK), memory address (ADDR), data to be written (data_in) and control signals (Write_enable, Read_enable). Based on these control signals, the module stores the data at the specified address or recovers its data.

I first wrote the Verilog code for the RAM module using an internal record matrix to store data. Conditional statements within a block always triggered by the clock signal determined that memory operation would be performed. If write_enable was active, the module stored the data received at the address provided. If read_enable was active, the output provided the data from the specified address. Care has been taken to ensure adequate synchronization and separation between reading and recording phases.

After the implementation of the main module, I developed a check in Verilog to check the RAM functionality. Testbench has generated clock signs and systematically applied entries for reading and recording operations. It included several test cases to record values in different memory locations and then read them again to check the correct operation. Testbench also found how RAM behaved with simultaneous or conflicting control signs to ensure robust handling of all <img width="1907" height="592" alt="T2" src="https://github.com/user-attachments/assets/bc486ca3-e42f-4be7-be78-114e2e319ff5" />
possible conditions.

I performed the simulation using Icarus Verilog and used the Open Epwave to view the waveform exits. The wave form clearly showed address transitions, data lines and control signals. He also confirmed that the data recorded in memory were recovered correctly, validating the successful operation of the RAM module. The simulation output corresponded to the expected results, meeting all the functional requirements mentioned in the task.

In general, this task significantly improved my understanding of how synchronous RAM operates at the logical digital level. Also improved my Verilog coding skills, creation of test tests and interpretation of simulation waveforms. At the end of this task, I was able to project, simulate and successfully verify a simple RAM system that has shown to write and read memory.
