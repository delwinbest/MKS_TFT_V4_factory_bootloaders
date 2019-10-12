# MKS TFT Boot ROM FW and Guide

The MKS TFT Display boards relay on Makerbase's proprietry Bootloader to install their Firmware and initialise the board. For those who have erased their device it's been impossible to reresore these baords to their original....'glory'. 

Special thanks to @darkspr1te for retrieving the original bootrom from the MKS boards which made this guide possible. 

### Requirements
1. Basic understanding of how to program microcontrollers (Arduino, etc).
2. STM32 ST-Link Programmer and cables, [Something Link This](https://www.amazon.com/WINGONEER®-Cortex-M0-Cortex-M3-Interface-Programmer/dp/B012VR3PVA/ref=cm_cr_arp_d_product_top?ie=UTF8).
3. STM32CubeProgrammer Software, downleded from [ST's Site](https://www.st.com/en/development-tools/stm32cubeprog.html).
4. A means to power the MKS board. (DC12V supply, USB-to-Serial cable, etc).
5. The firmware files wihtin this repo. 

## Connecting ST-LINK v2 to the MKS TFT: 
Connect up your ST-Link Programmer, In my case, the JTAG header is the closest STM32 chip and it's pin assignments are listed below. 

    ST-LINK    MKS-TFT32: 
    5v         AUX-1 5v 
    GND        AUX-1 GND 
    SWDIO      JTAG pin 4 
    SWCLK      JTAG pin 5 

I'm using the UART header to power my board using a USB-to-Serial Cable. This is not needed, you can use a DC power source. Do not power the board form the ST-Link Programmer.