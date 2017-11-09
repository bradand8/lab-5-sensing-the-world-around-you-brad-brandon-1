# Sensors and Signal Conditioning
In this lab we looked into translating signals from the analog world to the digit world. Sensors are necessary for accomplishing this.

## Sensors
Sensors are a way of converting physical data into an electrical value. For this lab, different sensor outputs need to be converted to a voltage, from which the value can be read through and Analog to Digital Converter (ADC) which the MSP430 Microprocessors have built in.

## Signal Conditioning
The signal conditioning was broken into multiple stages depending on the sensor used. First an output from the sensor may need to be amplified. An LM324 Quad OPAMP was used when the signal needed to be boosted. To reduce the noise that was also amplified, a lowpass filter may be needed before the signal is sent to the ADC.  


## ADC Resolution

The MSP430G2553 has a 10 Bit Resolution ADC with a maximum range of 0 to 3V. This results in 2.93mV per step of the ADC. More accurate results of the ADC occur when the input voltage is closer to the maximum value of 3V.  


## ADC Code


<s> Your code for this section should focus heavily on the ADC and being able to pull data from it. Your code need to communicate back to your computer using UART at 9600 Baud and send the ADC contents at 1 reading per second to start. This really is meant for you to see whether or not your signal conditioning is actually working and you can see changes in your sensor reading. This code should be very very similar to code you have written before and should be simple to port between your processors. </s>
  

## Hardware
 1. Temperature Sensor Circuit LM35
 
 
 
 
 2. Photo Resistor Circuit
 
 
 ![giphy-downsized-large](https://user-images.githubusercontent.com/31701000/32585812-490d0cd6-c4cd-11e7-9eff-325a8bda4d10.gif)
 3. Photo Transistor
 
The hardware portion should be the same for each of the processors. You will need to have a total of 3 circuits made, each corresponding to a different sensor. You need to look at the range of measurements and the amount of resolution you can get out of your ADC and determine how to convert, scale, and filter your signal. Don't forget the fact that you will need to convert to a voltage, making some of these circuits not so trivial. The main goal as the hardware designer for these sensors is to provide the microprocessor with the best resolution to maximize the effectiveness of the ADC.

### README
The README for this part of the lab should talk briefly about how the ADC code works, but focus way more on the hardware aspect. You need to include schematics of your circuits, and well as supporting simulation/calculations which show that your circuits should work. You should talk about what types of circuits you are using and how they actually work.
