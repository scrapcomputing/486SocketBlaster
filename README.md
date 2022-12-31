# 486SocketBlaster

486SocketBlaster is a simple voltage adapter for 486 processors. It allows you
to use a 3-volt 486 CPU on an older 5-volt-only motherboard. For example you
can use a DX4 or an Am5x86 on an old 486 motherboard that would normally only
work with 5-volt CPUs. This basically converts any 3-volt CPU to an "Overdrive".

<img src='img/486SocketBlaster_rev0.1.jpg' alt='486SocketBlaster Rev0.1 on a purple PCB' height=240>

<img src='img/486SocketBlaster_pcb.png' alt='486SocketBlaster PCB' height=240>

# How does it work ?

It is really simple: All CPU pins are passed through to the motherboard socket,
except the Vcc ones. Those are connected to the output of a mini buck converter
that can be soldered to the 486SocketBlaster board.

# Soldering/Assembly Instructions

This board is tricky to solder, but can be done with a standard soldering iron.
The best way to solder the headers is to start with the innermost one and work
outwards in a spiral manner alternating between the top and bottom side as
needed (see image below). This way you only work on the outside.

<img src='img/AssemblyInstructions.png' alt='Assembly Instructions' height=240>

A desoldering gun may be useful when you accidentally clog up other holes.
Also using flux makes it easier.

Please make sure you check for continuity before you add another row of headers
on the same side, because the new row will permanently block your access to the
solder joints! Desoldering a header is *extremely* difficult even with a
desoldering gun due to the tight hole tolerances.

# Voltage regulator

The 486SocketBlaster can be powered by a cheap of-the-shelf buck converter, or
by an external one. The circuit board accepts two common types of small voltage
buck converters, usually found using keywords like "mini buck converter".
These are commonly rated at up to 3A of current. Given that 3-volt 486 CPUs are
usually very efficient (the DX4-100 is rated at max 3.55/5.22W typical/max) such
a regulator should be adequate in most cases.

If you are planning to overclock or to use a more power hungry CPU, please use
an external regulation circuit.

# WARNING!!!

Please make sure you know what you are doing!
Improper assembly/settings/use can damage both your precious motherboard and your precious CPU!

# Bonus Features

- Header for an external voltage regulator, or for monitoring the voltages.
- Header for selecting/overriding the CPU multiplier. This may be useful for
reducing the multiplier of a DX4 or Am5x86 CPU.

# Bill of materials

Item                            | ##  | Description
--------------------------------|-----|--------------------------------------------------------
mini buck converter             | 1   | We support two common sizes: 22x17mm and 18x12mm. These usually have chips like MP1584, MP2307 and others
40pin SIP pin header (male)     | 5   | Single-row round pin 2.54mm pitch (male). Socket pin diameter: 0.5mm, PCB pin diameter: 0.6mm. (see photo below)
40pin SIP socket header (female)| 5   | Single-row round pin sockets, 2.54mm pitch. PCB pin diameter: 0.5mm. (see photo below) 
SMD Capacitors                  | 4   | 0.1uF SMD 1206
Throughole Capacitor            | 1   | 1uF ceramic through-hole capacitor
3-pin header 2.54mm             | 1   | Header used for selecting the CPU Multiplier
Jumper 2.54mm                   | 1   | A jumper to for the 3-pin header

Please note that the headers are a very tight fit. So please make sure that you get headers of the correct pin diameter.

The capacitors seem to be optional, at least with the limited testing that I
have done so far. Depending on they quality of the buck converter they may
or may not improve stability.

![headers](img/headers.jpg)

