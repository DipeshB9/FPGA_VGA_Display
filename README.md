# Digital Displayer using DE1-SOC FPGA Board

## Project Overview
Using Verilog, we designed and implemented a digital displayer on a DE1-SOC FPGA board. This displayer shows a horizontal line with a vertical line centered in the middle of the horizontal line, allowing the vertical line to move either left or right in degrees by pressing switches. This is the final project by John and Dipesh for ECE 287 at Miami University.

## Background
To complete our project, we first had to understand how to control the device ports on the DE1-SOC FPGA board. The project required understanding the VGA controller and how to generate display signals, such as horizontal and vertical sync pulses, to interact with a VGA display. Additionally, we familiarized ourselves with switch input handling and logic synthesis for hardware implementation.

## System Design
### Hardware Components
1. **DE1-SOC FPGA Board**: Utilized for logic implementation and signal generation.
2. **VGA Display**: Used to visualize the digital displayer output.
3. **Switches**: Enabled user interaction to move the vertical line left or right.

### Functional Modules
#### 1. VGA Controller
The VGA controller module generates synchronization signals to display content on a monitor. Key components include:
- **Horizontal and Vertical Sync Generators**: For pixel and frame timing.
- **Pixel Clock**: To control the drawing speed on the screen.

#### 2. Line Generator
This module computes the pixel data for the horizontal and vertical lines. It ensures the vertical line's position updates correctly when switches are pressed.

#### 3. Input Handling
Switch inputs are processed to determine whether the vertical line should move left or right. Debouncing logic ensures reliable signal interpretation.

## Implementation
### Verilog Code
The design was implemented in Verilog, leveraging the hardware description language's ability to describe concurrent operations. Key components include:
1. **VGA Timing Logic**: Responsible for generating synchronization pulses.
2. **Coordinate Calculations**: Tracks and updates the position of the vertical line.
3. **Switch-Based Movement Logic**: Handles the left and right movement of the vertical line.

### Simulation
Before deploying to the FPGA board, the design was simulated to verify timing and logic correctness. ModelSim was used to confirm the VGA signals and movement behavior.

### FPGA Deployment
The verified design was synthesized and uploaded to the DE1-SOC FPGA board using Quartus Prime. Switch inputs were mapped to the FPGA’s GPIO pins, and the VGA output was connected to a monitor.

## Results
When deployed, the system successfully displayed a horizontal line with a vertical line centered on the screen. The vertical line moved left or right in response to switch inputs, providing an interactive display.

## Challenges
1. **VGA Timing Calibration**: Ensuring correct synchronization pulses for proper display.
2. **Debouncing Switch Inputs**: Required additional logic to filter out noise from user input.
3. **Position Calculation**: Accurate calculation of pixel positions to avoid display artifacts.

## Conclusion
This project demonstrated the integration of Verilog programming, FPGA hardware design, and VGA signal generation to create an interactive display system. It provided hands-on experience with digital design concepts and hardware implementation on the DE1-SOC board.

## Future Work
1. **Enhanced Graphics**: Adding more shapes or animations to the display.
2. **Dynamic Input Control**: Using a joystick or keyboard for finer control.
3. **Optimized Resource Usage**: Reducing FPGA resource utilization for scalability.

## Repository Details
All project files, including Verilog code, simulation scripts, and documentation, are available in this repository. Contributions and feedback are welcome!


