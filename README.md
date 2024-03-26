This is going to be a small PCB with a microcontroller, IMU and a form of wirelessly transmitting that information though wifi/bluetooh.
It will serve as a central piece for a lot of future IoT projects.

![Microll_3D_PCB](https://github.com/RubenTrov/Microll/assets/104866446/adbaad53-3648-441e-a02c-f3fd26bebdd2)
![Microll_V1_Layout](https://github.com/RubenTrov/Microll/assets/104866446/88a206c8-d2b8-48e0-aa99-db1a78bdd943)

#How to program the PCB
This board has two microcontrollers that share the Same USB Port through a switch.
##Programming the STM32
1. The USB selector switch should be flipped to the SM32 position.
2. Open STM32CubeIDE and load the file that you wish to flash to the microcontroller.
3. Set the Boot pin High by setting the Boot on the DIP switch to position 2 and then from the ON side of the switch connect a jumper to the 3.3V GPIO header.
4. Connect the USB to the PCB to power on the board. This should make the STM32 be detected by the programmer.
5. Erase the memory and upload the file.
6. Disconnect the PCB from the USB and switch the position of Boot on the DIP switch.
7. Plug the USB back in the PCB and it will begin executing the program that was uploaded!

##Programming the ESP32
1. You may need to connect the GPIO0 pin to GND using a jumper cable before powering on the board
2. Flip the USB switch to the ESP32 position
3. Flip the EN on the DIP switch to the on position to connect it to 3.3V
4. Power on the board by plugging in the USB
5. Disconnect the GPIO0 pin from GND
6. The board should now be ready to program. Use the editor of your choice for this.
