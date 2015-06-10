ChiMS
=====

ChiMS is an open-source data acquisition and control software program written within LabVIEW for high speed imaging and depth profiling mass spectrometers. ChiMS can also transfer large datasets from a digitizer to computer memory at high repetition rate, saves data to hard disk at high throughput, and performs high speed data processing. The data acquisition mode generally simulates a digital oscilloscope, but with peripheral devices integrated for control as well as advanced data sorting and processing capabilities. Customized user-designed experiments can be easily written based via several included templates. ChiMS is additionally well suited to non-laser based MS imaging and various other experiments in laser physics, physical chemistry, and surface science. 

More details description refers to: Review of Scientific Instrument paper. 

Code Quality
=============
Master branch is LabVIEW 2013 compatible. 
Multirec-nightly branch can only be opened by LabVIEW 2014. 
Multirec-nightly branch is only functional to demonstrate 5 kHz high speed image, but not stable enough for real experiment. 
You will not be able to run the code right away just by clone the code.
You will need to clone instr.lib folder into your LabVIEW installation folder so that the first LabVIEW loads the code, the dependency can be found
You will need to get all the non-properiety dependencies by your own.
You might need Visual Studio runtime to have certain dll libray functional.
Master branch is most functioning well, although bugs exist in minor functionalities.

Known Issues in multirec-nightly branch
=============
Imaging pixel number is hard coded to be 5 in multirec-nightly branch for multirecord mode.
To run more than one imaging, the software has to be restarted, due to certain device were not closed properly. 
Encoder position readout is not properly designed. Deadlock could easily happen if trigger line signal quality is bad(hardware issue mostly). 
Each line scan has an uncertan length, couple pixel might be lost at the end of each line.

Dependencies
=============
This software does not come with all the dependencies due to coyright issues. However, you can download all the dependencies from their offcial website for free, except LabVIEW enviroment or hardware. Dependecies includes:

1. LabVIEW
2. NI-VISA
3. NI-Vision (if you need camera)
4. OpenG (lava.org, or VIPM)
5. MGI (VIPM)
6. JSON for LabVIEW (lava.org)
7. Gage SDK (Gage Applied)
8. NI-DAQmx (if you use NI DAQ products)

