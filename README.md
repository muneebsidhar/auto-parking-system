# Smart Parking Gate System

This is an Arduino project that runs a parking gate on its own. It notices when a car comes close, opens the gate, counts the cars going in and out, and shows the free slots on a small LCD. When the parking is full, the buzzer goes off and the gate stays closed.

I built it because manual gates need someone to stand there all day, and that leads to mistakes and delays. I wanted to see how much of that work a few cheap sensors and an Arduino could handle.

## What it does

- Detects an approaching vehicle with an ultrasonic sensor
- Opens and closes the gate with a servo motor
- Counts cars entering and leaving with two IR sensors, one for entry and one for exit
- Shows the total vehicles and the remaining slots on a 16x2 LCD
- Sounds a buzzer and keeps the gate shut when the parking is full

## Hardware

- Arduino UNO R3
- HC-SR04 ultrasonic sensor
- Two IR sensor modules
- SG90 servo motor
- 16x2 LCD
- 10k potentiometer for the LCD contrast
- Piezo buzzer
- 5V power supply
- Breadboard and jumper wires

Software: Arduino IDE

## How it works

When a car comes within a set distance of the ultrasonic sensor, the Arduino turns the servo from 0 to 90 degrees and the gate opens. The IR sensors then keep track of cars going in and out, and the count is updated on the LCD right away. If the number of cars reaches the maximum, the buzzer is triggered and the gate will not open any more, even if another car comes. Once a car leaves and a slot is free, the gate works normally again.

## How to run it

1. Wire the components as in your circuit and connect the Arduino to your computer.
2. Open the sketch in the Arduino IDE.
3. Select Arduino Uno under Tools, Board, and pick the right port.
4. Upload the sketch.
5. Turn the potentiometer until the text on the LCD is clear.

I have not added a pin table here, so add your own wiring list or a circuit photo in this section if you want people to be able to rebuild it.

## Limitations

- It controls one gate only
- It counts cars only up to a maximum capacity that is set in the code

## Ideas for later

- Save the car count so it is not lost when the power goes off
- Add a second gate for separate entry and exit
- Show the parking status on a phone

## Report

The full project report is in this repository as project-report-smart-parking-system.docx.

## Author

Muneeb Ur Rehman
