+++
date = '2026-10-27T11:33:40+03:00'
draft = false
title = 'Remote-Controlled Night Lamp'
+++
## Assignment 03 — Remote-Controlled Night Lamp

### Overview

For this assignment, I created a remote-controlled night lamp using two micro and a NeoPixel LED strip. One micro acts as the remote control, while the other controls the lights.

My goal was to create a lamp that switches between three colors—red, green, and blue—each time button B on the remote is pressed. After blue, the sequence returns to red and repeats.

### Tools and Materials

- Two BBC micro
    
- NeoPixel LED strip with three LEDs
    
- Alligator clip wires
    
- Battery packs
    
- Microsoft MakeCode
    

### Programming the Remote Control

I first programmed one micro to work as the remote control using Microsoft MakeCode.

I set the radio group to **5** so that both micro could communicate. I then programmed button B to send the number 1 whenever it is pressed.

This allows the remote to send instructions wirelessly to the night lamp.

_The MakeCode program for the remote control._

### Programming the Night Lamp

Next, I programmed the second micro to control the NeoPixel LED strip connected to pin P0.

I initialized the strip with three LEDs and set the starting color to red. I then created a variable called `color` to track the color sequence.

Each time the micro receives a radio signal, the variable increases by one. Conditional statements determine which color appears:

- **0:** Red
    
- **1:** Green
    
- **2:** Blue
    

When the variable reaches the end of the sequence, it resets to 0, returning the lights to red.

_The MakeCode program for the night lamp._

### Circuit Assembly and Testing

After preparing both programs, I connected the NeoPixel LED strip to the micro using alligator clip wires and connected the power components.

I checked the wiring and tested the LED strip. The LEDs initially did not light up as expected, so I needed to examine the connections and power supply.

_The electronic circuit with two micro and the illuminated LED strip._

### Challenges and Solutions

The main challenge was getting the external LED strip to work correctly. Although the programs were ready, the physical connections and power supply also needed attention.

This showed me the importance of checking both the code and the circuit when troubleshooting an electronics project.

### Final Result

The night lamp was designed to cycle through red, green, and blue using button B on the remote control. After the third color, the program returns to the first color, allowing the sequence to repeat.

### What I Learned

Through this assignment, I learned how to use radio communication between two micro and how variables and conditional statements can control an LED color sequence.

I also gained experience working with external electronic components and troubleshooting hardware connections.