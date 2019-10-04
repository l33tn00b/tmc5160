# TMC5160
Stepper Motor Control with TMC5160

Ok, Here we go. So you've got one of these stepper motors. And you're tired of cheap chinese control board knockoffs with HUUUUGE capacitors and diodes that just don't do any good. Well, there is a solution. Get one of these TMC5160-based control boards, like the TMC5160 stepstick or a TMC5160-BOB right from Trinamic. 

Now, you're ready to go. 

For a silly start, I tried to just hook up my TMC5160-BOB to an Arduino and a stepper motor (also from Trinamic, I like German quality). My plan was to start with the easy stuff: Just Step/Dir, without the integrated motion controller of the TMC5160. Should be easy, shouldn't it? Well, no.

First I needed to resolder a 0805 SMD resistor. Ready? Not quite. Turns out, the TMC5160-BOB's SPI_MODE pin is hard-wired to VCC. YOU HAVE TO USE SPI to initialize the chip. That one cost me two days until I decided to check the board's schematic. Can't you just spell it out in the documentation?
