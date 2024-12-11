---
layout: home
title: FPGA VGA Driver Project
tags: fpga vga verilog
categories: demo
---

Welcome to my VGA project blog for the System on Chip Design and Verification module. In this project, I was tasked with displaying my own image from a given code template.

## **Template VGA Design**
### **Project Set-Up**
To begin the project I created a new project in Vivado, with the artix 7 product family and the "xc7a35tcpg236-1" project part. I then imported the modules, testbench and constraint files.
As usual, I had to move the testbench to simulation sources and set the VGATop module as top. Following this, in "IP catalog" I had to change the clock frequency to 25MHz.
Upon completion, the colour cycle template then ran successfully, which loops through diffferent colours on the screen.

<img src="https://raw.githubusercontent.com/melgineer/fpga-vga-verilog/main/docs/assets/images/VGAPrjSum.png">

### **Template Code**
Fistly, the VGASync module create the timing signals needed for a VGA display to know when to start a new row or frame. It keeps track of the current position of the pixel on the screen. The row and col outputs 
allow other modules to access the pixel's coordinates.

The VGATop module is the top-level module of the system. It includes the VGA synchronization logic, a clock divider for generating the required 25 MHz clock, and the ColourCycle and ColourStripes module.
### **Simulation**
Simulation is a useful tool to allow us to verify the timing, functionality and output of the modules.
The testbench is used to simulate the system. 
### **Synthesis**
The synthesis process converts Verilog code into a hardware description made of logic gates and flip-flops, optimized for the target FPGA.
The implementation process places the hardware components on the chip and connects them and then generates a bitstream to program the FPGA.
### **Demonstration**


## **My VGA Design Edit**
Introduce your own design idea. Consider how complex/achievabble this might be or otherwise. Reference any research you do online (use hyperlinks).
### **Code Adaptation**
Briefly show how you changed the template code to display a different image. Demonstrate your understanding. Guideline: 1-2 short paragraphs.
### **Simulation**
Show how you simulated your own design. Are there any things to note? Demonstrate your understanding. Add a screenshot. Guideline: 1-2 short paragraphs.
### **Synthesis**
Describe the synthesis & implementation outputs for your design, are there any differences to that of the original design? Guideline 1-2 short paragraphs.
### **Demonstration**
If you get your own design working on the Basys3 board, take a picture! Guideline: 1-2 sentences.

## **More Markdown Basics**
This is a paragraph. Add an empty line to start a new paragraph.

Font can be emphasised as *Italic* or **Bold**.

Code can be highlighted by using `backticks`.

Hyperlinks look like this: [GitHub Help](https://help.github.com/).

A bullet list can be rendered as follows:
- vectors
- algorithms
- iterators

Images can be added by uploading them to the repository in a /docs/assets/images folder, and then rendering using HTML via githubusercontent.com as shown in the example below.

<img src="https://raw.githubusercontent.com/melgineer/fpga-vga-verilog/main/docs/assets/images/VGAPrjSrcs.png">
