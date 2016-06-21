# STM32_EMON

This repository contains the Eagle and KiCad files for my STM32 energy monitoring and display projects,  based on the Open Energy Monitor project's work

NOTE. THIS IS A WORK IN PROGRESS, PLEASE CHECK MY DESIGNS BEFORE COMMITTING TO GETTING A PCB MADE!

The PowerTransmitter board, had 2 faults on the first batch of PCB's. A track was missing (current sense input to the ADC on the STM32),
I also omitted pullups and pulldowns on the ESP8266.
I think the issue with the current input track has been fixed, but the ESP8266 issue still needs to be checked.
 
The PowerReceiver board seems to work, but I've not tested the ESP8266 connections.

 

The PowerTransmitter, is equivalent to the EMonTX, in that it monitors mains voltages and current, and transmits this data via RF
My PowerTransmistter also has an ILI9341 display, and uses a Nordic nRF905 for RF transmission. 
It also has an ESP8266 - however there is currently a mistake in the schematic and PCB as its missing a pullup or pull down

PowerReceiver is a simple display unit to remotely display the same information on the PowerTransmitter, but it also contains an ESP8266.

The reason the Power Receiver has an ESP8266, is because for when the PowerTransmitter can't be located where there is Wifi coverage, hence the PowerReceiver acts as a bridge to Wifi in this case.