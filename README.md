# SPI-Master
A TTL implemention of SPI


SPI is almost universal these days, for peripherals, LCDs, sensors, memory, uSD cards, GPIO expanders etc, etc. It's also a really neat way to communicate between 2 systems using a minimum of signals.


The downside is that it is not implemented on the classic cpus - such as 6502, Z80 etc, creating an additional problem to interface these processors to modern peripherals.


Ideally, the solution would be a simple SPI transceiver that could be connected to a traditional 8-bit bus.


A partial solution was suggested on the 6502.org forum nearly a year ago involving bit-banging SPI, and then a faster hardware proposal making use of the 74HC299 universal shift register.


http://forum.6502.org/viewtopic.php?f=12&t=6066&start=60


This repository explores the TTL shift register solution further, with the aim of building a simple TTL design that will interface to a typical microprocessor bus.


Whilst an SPI interface could be implemented using a programmable logic device such as the ATF750 CPLD:

https://ww1.microchip.com/downloads/en/DeviceDoc/doc0776.pdf

the challenge here is to explore the TTL options. This gives a better understanding of the features required and how to implement them in discrete logic.


Initial simulations have been performed using H. Neemans "Digital" simulator - available here on Github https://github.com/hneemann/Digital


A circuit model of the 74HC299 universal shift register was created and added to the Digital library, along with other relevant circuit simulations.
