# TeensyJenny
JEN SX-1000 synthesizer midification design, based on a Teensy 3.2 controller board.

## Aim of the project

The JEN is a basic, and cheap, Italian monosynth from the late-70s, which lends itself to modding - although the quirky oscillator design centered on a rare chip called SGS M110, it means that there is no way to control the synth externally, as it won't understand CV. 

The aim is to have a version of the JEN synth that can be controlled digitally, understands MIDI, and does not lose any of the charms of the very basic JEN SX-1000 synth: a mainly analog oscillator design, and immediacy. The digital controller can then be used to implement additional functions like pitch bend, vibrato, portamento legato. With more hardware, the controller might take control of more and more of the JEN's analog voltages, allowing for more and more flexibility.

The full outline of what I intend to do is here: https://www.untergeek.de/2017/08/midifying-jenny-a-call-to-arms/

## How far have we gotten yet?

In the first step, the controller board does not do much more than scan the keyboard and put out the appropriate frequencies - basically, what the M110 chip does, the one truly digital component in the JEN.

To keep the design simple, it is no 1:1 replacement of the M110 chip in the JEN, but needs you to cut a couple of pullup resistors from the keyboard PCB, and to wire the board to the JEN's 5V supply. 

The whole thing should not take more than 2 hours to build, once it is running. 

Please mind what it doesn't do yet (Jan 2019): 
- No VCF tracking voltage generated
- No reading and evaluating of portamento yet

Find the details on http://www.untergeek.de/?p=3551

![breadboard](https://github.com/untergeekDE/TeensyJenny/blob/master/m110-teensy_Steckplatine.png)

This repository contains: 
- Fritzing design
- Demo code for simple keyboard scanning/frequency output
