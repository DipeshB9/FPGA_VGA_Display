This project is a step toward building a framebuffer using the DE1-SOC FPGA board. While a complete framebuffer requires significant memory, this design implements a small 4x4 (16-location) memory for demonstration purposes. The design supports writing and reading to/from memory and displays the results on a VGA display.


The goal of this project is to demonstrate basic memory operations and VGA interfacing on the DE1-SOC FPGA.

Memory Overview: A small 4x4 memory is implemented to simulate framebuffer-like functionality.
Write Phase: After a reset, the system writes predefined values into the memory.
Read Phase: Once the write operation completes, the memory is continuously read to display output on the VGA screen.
This design integrates concepts of finite state machines (FSMs), memory management, and VGA interfacing.
