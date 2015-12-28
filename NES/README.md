
README.md


This is a project for ECE 395 at the University of Illinois.  Our original intent was to take someone else's working NES fpga project and turn it into a portable console system a la the GameBoy.  From the first appearance of the project, it looked like this one was the most complete, so we chose to begin our work with it. The original idea was to have a final product that runs off of cartridges, as using roms has questionable legality at best, so we would have to modify the code.   


Notes
--The blog post in which the original poster documented the project stated the board used was the NEXYS 4, but it appears that the actual board was the NEXYS 3, as the project mentions the Spartan 6 chip, where the NEXYS 4 uses an Artix 7.  

--Our goal of making a portable system means that we need to not use a development board.  This means we need to solder the fpga to the board (schematic generated in EAGLE).  The problem is that the Spartan 6 uses a ball-grid-array packaging, which we are not skilled enough to solder.  At the moment we are looking at spartan 3 chips, which are available in a flat packaging, so we are attempting to make the project work for a digilent spartan 3 development board.  

Contributors
--Nick Moore
--Robert Gazdziak

Origins of code used not generated by Bobby or Nick
--code for the compiler was taken from the cc65 repo on github.  It's a pretty cool compiler in that it includes specific headers for developing projects with specific famous targets in mind, like the NES, the apple 2E, and the Atari 5200
--Original code for the NES emulator was taken from a repo owned by github user Strigeus.  This code is the code described by the report as being insufficient for good development and portability due to its poor code organization and its hardware restrictions.  The original readme for Strigeus's project follows.  If you choose to use his code, you can still find his unchanged repo under his name.  He doesn't mention that you need to download and install the digilent adept 2 libraries from the digilent website and modify the solution files to use the correct include paths in order to successfully build the visual studio solution he provides.  

################################################################################################################################
original README.md as written by Strigeus
################################################################################################################################
fpganes
=======

This is the source code for my FPGA NES.

It's designed to run on the Nexys4 board and built with
Xilinx ISE.

Use "loader" to download ROMS to it over the built-in UART.

"loader" also transmits joypad commands from my USB joypad
to the FPGA across UART.
