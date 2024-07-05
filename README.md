# 5bit ALU-Verilog-Code
This repository contains Verilog module files required for basic ALU. The project implements a 5-bit Arithmetic Logic Unit (ALU) that can perform three operations: addition, subtraction, and multiplication.

This project provides the Verilog implementation of a 5-bit Arithmetic Logic Unit (ALU) capable of performing addition, subtraction, and multiplication. The design includes various sub-modules such as FullAdder, Adder, FullSubtractor, Subtractor, Multiplier, RegisterFile, and the main ALU module. The project also includes a top-level module to integrate all the components.

## Features

- **Addition**: Performs 5-bit addition.
- **Subtraction**: Performs 5-bit subtraction.
- **Multiplication**: Performs 5-bit multiplication.
- **Registered Input and Output**: Inputs and outputs are registered for stable and accurate operations.

## Why This Project is Useful

This project is a fundamental building block for understanding digital design and FPGA programming. It can be used in educational settings, for prototyping complex digital circuits, or as a component in larger digital systems.

## Getting Started

### Prerequisites

- [Intel Quartus Prime Lite](https://www.intel.com/content/www/us/en/software/programmable/quartus-prime/download.html) (or any other compatible Verilog simulation and synthesis tool)
- [ModelSim](https://www.intel.com/content/www/us/en/software-kit/750368/modelsim-intel-fpgas-standard-edition-software-version-18-1.html)
- Basic knowledge of Verilog and digital circuit design

2. **Open the Project in Quartus Prime Lite**
   - Launch Quartus Prime Lite.
   - Create a new project and add the Verilog files (`FullAdder.v`, `Adder.v`, `FullSubtractor.v`, `Subtractor.v`, `multiplier_5bit.v`, `RegisterFile.v`, `ALU.v`, `TopLevel.v`) to the project.

3. **Set Top-Level Entity**
   - Set `TopLevel` as the top-level entity for synthesis.

4. **Compile and Synthesize**
   - Compile the design and synthesize it using Quartus Prime Lite.
   - Ensure that the synthesis completes without errors and meets timing requirements.

5. **Program the FPGA (if applicable)**
   - If targeting an FPGA, program the synthesized design onto the FPGA device.

### Usage

Once synthesized and programmed onto an FPGA, the ALU can be tested by providing 5-bit inputs `A` and `B`, and selecting the operation via the `Op` input:
- `00` for addition
- `01` for subtraction
- `10` for multiplication

The result is provided as a 10-bit output `Result`.

### Example

Here's a simple example of how to instantiate the ALU in your Verilog code:

```verilog
module ExampleUsage (
    input [4:0] A,
    input [4:0] B,
    input [1:0] Op,
    input clk,
    output [9:0] Result
);

    TopLevel top_level_inst (
        .A(A),
        .B(B),
        .Op(Op),
        .clk(clk),
        .Result(Result)
    );

endmodule
```

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For any questions or suggestions, please open an issue on GitHub or contact me at [aya@example.com](mailto:your.email@example.com).
```

Feel free to customize the content according to your specific needs and preferences.
