Nigel Edits: v1.0.0

/* Assuming you have STM32CubeIDE or STM32CubeMX? or some other ST Software*/
check this path 
C:\Program Files (x86)\STMicroelectronics
should include:
STM32 ST-LINK Utility 'if not' go to link on step (1)
Software 'if not' go to the link on step (3)

In order to update the Inventek ISM43362 Wifi module firmware, there are several steps:
This update will fully erase the chip.

Prior to running this, 
/* STSW-LINK004 In folder: C:\Users\Kings\Desktop\B-L475E-IOT01A Wi-Fi Upgrade */
1.	You must have the ST-LINK Utility installed in so that the ST-LINK_CLI.exe path is "C:\Program Files (x86)\STMicroelectronics\STM32 ST-LINK Utility\ST-LINK Utility\ST-LINK_CLI.exe" (default install directory).
http://www.st.com/content/st_com/en/products/embedded-software/development-tool-software/stsw-link004.html

/* Install STM32CubeProgrammer or skip to 3 to complete */
2.	Update the ST-LINK firmware on the discovery board with STM32Cube Programmer
	2.0 In the 'ST-LINK' tab, select 'Refresh device list' -> 'Firmware update'
		V2J39M27 stm32 Debug+Mass Storage+VCP
	2.1 Click on 'upgrade'
	2.2 Unplug and re-plug the Discovery Kit IoT Node or press the reset button (Black) 
	2.3 Select the DIS_L4IOT Drive and under 'DETAILS.TXT' you will find the ST-Link version

/* Ignore? */
/* Already had it on my system, */
3.	You must have the STMFlashLoader demonstration tool installed so that the STMFlashLoader.exe path is  "C:\Program Files (x86)\STMicroelectronics\Software\Flash Loader Demo\STMFlashLoader.exe" (default install directory).
http://www.st.com/content/st_com/en/products/development-tools/software-development-tools/stm32-software-development-tools/stm32-programmers/flasher-stm32.html

4.	You must make sure you have no other ST-LINKs connected to the PC other than the Discovery Kit. 

/* Download ISM43362_M3G_L44_SPI_C3.5.2.5.STM SPI Firmware link bellow (no need to unzip and rename) */
https://www.inventeksys.com/iwin/firmware/

/* C:\Users\Kings\Desktop\B-L475E-IOT01A Wi-Fi Upgrade\en.inventek_fw_updater\bin */
6. Copy the ISM43362_M3G_L44_SPI_C3.5.2.5.STM.bin you just downloaded to ..\Inventek FW Updater\bin folder

7. From the \bin directory, run update_Wifi_FW_C3.5.2.5.STM.bat and it will go through 2 steps:
	a.	Update the Discovery Kit firmware to InventekBootloaderPassthrough.bin using the ST-LINK command line interface.
	b.	Update the Inventek WiFi firmware to ISM43362_M3G_L44_SPI_C3.5.2.5.STM.bin using the STMFlashLoader command line interface.
	c.	Once Complete a Blue LED4 should be lit.