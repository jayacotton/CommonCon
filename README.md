# CommonCon
CP/M 3 common console support for s100computers z80 master z80 fpga sbc and camelion 8/16

So, what is the problem that we are trying to solve here.
The console should stay on the selected device from power up to power down without changing to 
a different console or changing speed.  In addition the CP/M 3 code should be able to link into 
the boot prom drivers and use that code for i/o, this will releave the bios writer from creating
yet another copy of the console driver.

What is to be supported ?  Well the SIO port 0 as console using the DUAL SIO board also the USB
device (on the dual sio) and other devices that do USB.  The propellor I/O board as a console,
and support for VGA device on the z80 fpga sbc and camelion 8/16.  VGA support may be available
for other cards TBD.

Adding build tools for this repo.  Note: these will only run on linux x86.  For Windows you will
need an altairz80.exe windows version file.

The plan is morphed a bit.  My plan now is to make a support rom that has the drivers onboard
and a boot loader to start up cp/m.  All the other MASTER.Z80 test code is left out for now.
Once the boot loader is working on more than 1 machine I will start pulling in support code
from MASTER.Z80
