# word_clock_v2
Second version of the word clock

I have made a lot of changes to the word clock since v1, and hope to get manufacturing up and running during the Spring semester. One of the main problems with the previous design was wiring the PCB to the lights and resistors. The end result was a jumble of wires that took up so much space that I had to cut a bigger box, about 8 inches deep. Another problem that the word sets were hard coded into the Arduino code, meaning that if you wanted to change the template, you would have to learn the ordering system and change the Arduino code itself.

To fix the first issue, I have designed a PCB that will be mounted on the the LED board to reduce size. The LEDs are soldered directly onto the PCB, as are the resistors. Because the PCB will have to be flush with the LED board, all resistors and ICs are on the opposite side of the LEDs. Once again, these PCBs are printed using an Othermill Pro, and the vias will have to be soldered manually.

In order to simplify things, I wanted to have one shift register control one PCB. This means 8 LEDs per PCB. With the previous 11x11 setup, this would be very difficult geometrically; thus, I decided to move to a 12x12 grid so that the PCBs are modular. Each PCB will have two rows of 4 LEDs, each spaced according to the maximum size of the LED board. To have 144 LEDs, this will require 18 PCBs, which is a large amount. It is the price you pay for not ordering from a vendor.

For the template creation, one of my friends whipped up a quick script to write an Arduino snippet based on a settings txt file that the user edits. It is very handy-dandy and I will be using and expanding on it soon.
