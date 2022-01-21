# DISCO-L475VG-IOT01A--WIFI-firmware-update
This is not a replacement for the instructions found in STM, Mbed, ASW web pages or the instruction card.\
Additional intructions can be found in the readme.txt for each Programm
- https://docs.aws.amazon.com/freertos/latest/userguide/getting_started_st.html
- https://os.mbed.com/teams/ST/wiki/How-to-make-wifi-tests#wifi-firmware-update

## Required Downloads
1) ST-Link 004 (attached) \
http://www.st.com/content/st_com/en/products/embedded-software/development-tool-software/stsw-link004.html 

2) Program Flasher (attached) \
http://www.st.com/content/st_com/en/products/development-tools/software-development-tools/stm32-software-development-tools/stm32-programmers/flasher-stm32.html 

3) ISM43362_M3G_L44_SPI_C3.5.2.5.STM (attached) \
https://www.inventeksys.com/iwin/firmware/ 

## Steps 

*1)*
Upgrade the ST-Link using STM32CubeProgrammer 
- In the 'ST-LINK' tab, select 'Refresh device list' -> 'Firmware update'
- V2J39M27 stm32 Debug+Mass Storage+VCP
- Click on 'upgrade'
- Unplug and re-plug the Discovery Kit IoT Node or press the reset button (Black) 
- Select the DIS_L4IOT Drive and under 'DETAILS.TXT' you will find the ST-Link version should read *V2J39M27*\

Upgrade the ST-Link using STM32CubeIDE
- Help 
- ST-Link Upgrade

*2)* 
Run the Bat file on found in the folder en.inventek_fw_updater, this will 
- Update the Discovery Kit firmware to InventekBootloaderPassthrough.bin using the ST-LINK command line interface. \
- Update the Inventek WiFi firmware to ISM43362_M3G_L44_SPI_C3.5.2.5.STM.bin using the STMFlashLoader command line interface.\

*3)* Complete
- Blue LED4 on 


