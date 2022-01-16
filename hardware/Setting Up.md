---
label: Setting Up
order: 0
icon: zap
---

# Getting Gatego Autonomous+ out of the box

Get everything out othe the box, you will also need a Philipps 1 screwdriver to complete all of the connections with your gate.

==- Box Contents
1x Logic Board

1x Processor Module

1x 6-Led Strip with a 3-Pin connector

1x Screen

1x 4-Pin cable

1x Mounting system
===

If not already assembled, place the screen in the top area of the mounting system, screwing it in with the 4 screws on the corners of the screen and placing the 4-Pin cable into the exposed connector on the side of the screen. Do not connect the other end yet.

Next, place the LEDs in position in the top area of the mount, making sure to feed the connector back into the main chamber and placing the diffusion layer back in.

Now, insert the processor module into the logic board, making sure all of the pins are in the correct socket, use the drawing to guide you. The ethernet jack should be looking towards the opposite side of the white connectors.

We're nearly done, now connect the LED cable to the smaller white 3-pin connector in the logic board, and the screen on the bigger 4-pin connector next to it.

Lastly, place the board inside the mounting system and screw it in with the 4 provided screws.

# Connections

Gatego Autonomous+ has a number of connections that it needs to communicate to the outside world. You will find them all in the bottom of the logic board. The first is the ethernet jack. You will need to connect it to a PoE (IEEE 802.3-compliant) injector or switch. If you do not have one, please contact us and we will provide an injector free of charge. This connector allows Gatego Autonomous+ to have power and internet connection.

Next, there is a 2-Pin screw terminal. This is used to check the gate status and will need to be connected to the gate controller. Connect the positive terminal of you gate's NO (Normally open) port into the positive treminal in the device, and the GND of your gate into the negative terminal of the screw terminal. 


!!!warning Voltage Limits
Gatego Autonomous+ was designed with versatility in mind and this connector should be able to support a large range of voltages, anywhere from 12v to 35v. Please contact us if your gate is not inside the voltage range so we can send you a board the will accept the voltage you need.
!!!

Lastly, let's connect the 3-pin screw terminal. This will be used to control the gate through the gatego app. Please refer to your barrier's manual to check what connector should be connected. Typically, the COM should be connected to the GND terminal of your gate controller, and the NO terminal into the entry button location.

# First Power-up


# Register device


!!!success Success
You are all set! Gatego Autonomous+ is ready to be used.
!!!