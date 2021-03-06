# Alligator-Arduino-variant

*Variant files to add support of Alligator Board in your arduino IDE Software*

Supported Arduino IDE:
- **Arduino 1.6.3**
- **Arduino 1.5.8**

### Install Alligator support on Arduino 1.5.8

1. Install Arduino 1.5.8
2. Navigate on your Arduino install directory and copy Alligator variant files:

  ##### For Windows:
  - Copy *alligator_r2* directory to 
  **C:\Program Files (x86)\Arduino\hardware\arduino\sam\variants\**

  - Replace the file **C:\Program Files (x86)\Arduino\hardware\arduino\sam\boards.txt**
    with the file **variant-Arduino-1.5.8\boards.txt**

  ##### For Mac OSX:
  - Copy **alligator_r2** directory to
  
    **/Arduino.app/Contents/Resources/Java/hardware/arduino/sam/variants/**

  - Replace the file **/Arduino.app/Contents/Resources/Java/hardware/arduino/sam/boards.txt**
    with the file **variant-Arduino-1.5.8/boards.txt**

3. run Arduino software and select : 

  Tools -> Board -> Alligator 3D Printer Board R2 ( USB /UART)

4. ERASE flash memory and upload code

  Uploading code to the SAM3X is different than the AVR microcontrollers found in other boards because the flash memory   needs to be erased before being re-programmed. Upload to the chip is managed by ROM on the SAM3X, which is run only when the chip's flash memory is empty.

  The dip switch near the processor is responsable for the manual flash erase procedure :

    - Dip switch toward drivers engine
    - Press the reset button
    - Waiting for 1 second
    - Dip-switch toward processor
    - Press the reset button
    - upload code

### Install Alligator support on Arduino 1.6.3

1. Install Arduino 1.6.3
2. run Arduino software
  - navigate to Tools -> Board -> Boards Manager 
  - install *Arduino SAM Boards (32-bits ARM Cortex-M3)*
  - close Arduino Software
3. Navigate on your Arduino package directory and copy Alligator variant files:

  ##### For Windows:
  - Copy **alligator_r2** directory to 
  **C:\Users\user_name\AppData\Roaming\Arduino15\packages\arduino\hardware\sam\1.6.3\variants\**

  - Replace the file **C:\Users\user_name\AppData\Roaming\Arduino15\packages\arduino\hardware\sam\1.6.3\boards.txt**
    with the file **variant-Arduino-1.6.3\boards.txt**

  ##### For Mac OSX:
  - Copy *alligator_r2* directory to 
  **/Users/user_name/Library/Arduino15/packages/arduino/hardware/sam/1.6.3/variants/**

  - Replace the file **/Users/user_name/Library/Arduino15/packages/arduino/hardware/sam/1.6.3/boards.txt**
    with the file **variant-Arduino-1.6.3\boards.txt**
  
4. ERASE flash memory and upload code

  Uploading code to the SAM3X is different than the AVR microcontrollers found in other boards because the flash memory   needs to be erased before being re-programmed. Upload to the chip is managed by ROM on the SAM3X, which is run only when the chip's flash memory is empty.

  The dip switch near the processor is responsable for the manual flash erase procedure :

    - Dip switch toward drivers engine
    - Press the reset button
    - Waiting for 1 second
    - Dip-switch toward processor
    - Press the reset button
    - upload code


  
 **WARNING only for Alligator SN less than #77 : Native port are directly connected to 5V power !** <br>
 **Do not connect Native USB port to the PC in presence of 12-24V power input.** <br>
 **Communicate with Alligator and with your printer only from the USB/UART port.** <br>
 **Native port connected directly to the PC can be used only for board testing without 12-24V power input (for expert users only!)**
