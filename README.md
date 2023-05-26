# Diy-Arduino

![Screenshot (1087)](https://github.com/Arush-om/Diy-Arduino/assets/134673721/8c59b616-e889-4c26-ae08-162853a66cab)

If you have hard-time 3d printing stuff and other materials which i have provided in this project please refer the professionals for the help, [JLCPCB](https://jlcpcb.com?from=ayu ) is one of the best company from shenzhen china they provide, PCB manufacturing, PCBA and 3D printing services to people in need, they provide good quality products in all sectors

[JLCPCB](https://jlcpcb.com?from=ayu)

Please use the following link to register an account in [JLCPCB](https://jlcpcb.com?from=ayu )

https://jlcpcb.com?from=ayu 


Pcb Manufacturing

----------

2 layers

4 layers

6 layers

jlcpcb.com/RNA


PCBA Services

[JLCPCB](https://jlcpcb.com?from=ayu ) have 350k+ Components In-stock. You don’t have to worry about parts sourcing, this helps you to save time and hassle, also keeps your costs down.

Moreover, you can pre-order parts and hold the inventory at [JLCPCB](https://jlcpcb.com?from=ayu ), giving you peace-of-mind that you won't run into any last minute part shortages. jlcpcb.com?from=ayu 


3d printing

-------------------

SLA -- MJF --SLM -- FDM -- & SLS. easy order and fast shipping makes [JLCPCB](https://jlcpcb.com?from=ayu ) better companion among other manufactures try out [JLCPCB](https://jlcpcb.com?from=ayu ) 3D Printing servies

[JLCPCB](https://jlcpcb.com?from=ayu ) 3D Printing starts at $1 &Get $54 Coupons for new users
![Screenshot (1088)](https://github.com/Arush-om/Diy-Arduino/assets/134673721/642184b1-1683-43ce-bdc7-d20d09dbd85b)
![Screenshot (1089)](https://github.com/Arush-om/Diy-Arduino/assets/134673721/3d4e0d02-77e1-43b9-be29-6361a919f59f)
![Screenshot (1090)](https://github.com/Arush-om/Diy-Arduino/assets/134673721/7e562813-a1a0-44b2-b3de-abcac90b9d40)
![Screenshot (1091)](https://github.com/Arush-om/Diy-Arduino/assets/134673721/6717da92-62d8-42bf-9e75-17351a38b0ea)

In order to make our Arduino board, we will need a microcontroller, which will be the one doing all the mathematical calculations and doing all the logical decisions. So which microcontroller do we use in our Arduino Board? Here, will be using an ATMega328. The microcontroller can’t operate without the bare essentials. In order to function, it just needs a minimal amount of setup. Let’s look at the bare minimum configuration.

![Screenshot (1094)](https://github.com/Arush-om/Diy-Arduino/assets/134673721/28313561-3fe5-40dd-986e-12dcc9ac889c)
![Screenshot (1092)](https://github.com/Arush-om/Diy-Arduino/assets/134673721/71e36e2d-ec2a-49e7-88dd-9daa17e3c7ce)
![Screenshot (1093)](https://github.com/Arush-om/Diy-Arduino/assets/134673721/abf72666-6214-46a0-af59-98d89caff830)


I used an Altium designer to draw the circuit and design the PCB. It is a powerful tool that can be used to design and create your own PCBs for your project as well as complex and multiplayer PCBs for industrial use. I will leave the link to the free trial version in the description. I have been using it for the past 3 years. If you are an electronic engineer, it’s gonna be really useful for you. Also, if you are a student, you will get 6 months license completely free of charge! So do make use of it!

To get started with the bare minimum configuration, we will need the ATMega328 chip, 16 MHz crystal oscillator, and two capacitors. Crystal Oscillator will be connected between pins 9 and 10 and the two ends are connected to the ground. Why do we need a crystal oscillator? Every microcontroller needs a clock signal and every action inside the chip is based on the clock. For the Arduino, clock signals are provided by a Crystal oscillator.

The first step is after finding a good sized perfboard is to find a good place for the chip, and place the IC socket where you want it paying attention to the notch witch will be matched with the notch on the chip. also find where you want your power jack. You should place it on the edge of the board probably in the corner. I widened the holes on the board with a 1/16 inch drill bit, but still had to fold the leads on the jack using needle nosed pliers to get it to fit through. On the jack, the pin on the back connecting to the post on the inside is positive, and the one on the bottom connected to the metal on the inside is ground (the pin on the side is not needed. You could solder it for extra support, but I just broke it off). Remember this when connecting the regulators.

![Screenshot (1097)](https://github.com/Arush-om/Diy-Arduino/assets/134673721/48ae2ae5-2ceb-4e63-94de-deee1253b2c7)
![Screenshot (1095)](https://github.com/Arush-om/Diy-Arduino/assets/134673721/22fcea18-5795-4649-a279-6635d02d7703)
![Screenshot (1096)](https://github.com/Arush-om/Diy-Arduino/assets/134673721/2b5b6fa4-16b6-4d5c-a334-c8d66cb1de00)


So in order to program the Atmega328 using USB, UART data from the chip is sent to another module that can convert UART to USB and vice versa, which will bridge the two technologies together. In our case, we will be using an FTDI module that will handle the communication between ATMega328 and our computer. This is where we will be connecting the FTDI module. The Tx pin of the FTDI module is connected to the Rx pin of ATMega328 and the Rx pin of the FTDI module is connected to the Tx pin of ATmega328.
Once you power up the ATMega328, it will work. But that is not enough, is it? We will be making it more stable, versatile, and more USEFUL. Let’s make it closer to the real Arduino Board.

Making a Custom Arduino Board
This is the point where we will be connecting the input voltage. Input power will be connected to a 7805 voltage regulator which will convert a voltage between 7-32 volt to a steady 5V DC Supply, which will be fed to Arduino and other components.

![Screenshot (1099)](https://github.com/Arush-om/Diy-Arduino/assets/134673721/6c7c0d02-d6e9-4202-82b2-d38648af72b5)

![Screenshot (1101)](https://github.com/Arush-om/Diy-Arduino/assets/134673721/bdcf7e2a-e73a-4cf3-b492-9fbfb7c0d895)

This 5V is also fed to a voltage divider circuit which will reduce the voltage to a 3.3V DC voltage. This will be really helpful when we are connecting modern sensors and modules as most of them work on 3.3V.

PWM pins are connected to these 3 pin headers, where the first pin is connected to corresponding PWM pins, the second pin is connected to 5V and the third pin is connected to GND. This is the pin configuration of most of the servo motors and sensor modules; which means, you can connect your Servo motor directly to this Arduino Board.

Then here are the Analog pin headers, which are connected to the Analog Pins, and here are the digital pin headers that are connected to the remaining digital pins.

And we have some indicator LEDs that will help us to troubleshoot if anything goes wrong. This LED is connected to Pin 13 of the ATMega328.

Now the real question is how do we program this Arduino Board? The ATMega328P chip can’t communicate with USB directly. Their way of communication is UART.

![Screenshot (1100)](https://github.com/Arush-om/Diy-Arduino/assets/134673721/10ff13b1-1717-42c7-b993-c237238613fd)

![Screenshot (1103)](https://github.com/Arush-om/Diy-Arduino/assets/134673721/dd6f8890-cd5d-46e6-9675-375ca9753a1c)

![Screenshot (1104)](https://github.com/Arush-om/Diy-Arduino/assets/134673721/89c237ae-c880-4c37-aea1-9caa5a4b0c0d)

Now it is time to add the five volt regulator. This is technically the only regulator you need to power the chip, but if you want a 3.3v pin (some breakout boards or sensors require 3.3v so the pin is nice to have), you will need to add the 3.3v regulator. These regulators require two decoupling capacitors each. Holding the 7805 printed side facing you, and the pins pointing down, the one furthest left is the input, the center is ground and the furthest right is the output. connect one 10 uf electrolytic capacitor to between the output and ground and the input and ground, being sure to connect the smaller leg to ground. connect the positive from the power jack to the furthest input pin, and ground from the power jack to the center pin.

To draw the final schematic I used Easyeda, a web-based EDA tool suite. Drawing big circuits like this can be very easy in this portal. Also it's a online service. So by usability it gets nothing better. I will also recommend you to use it in your design. The circuit that I designed can be found in the link below. That is a PDF doc. Download and take a look if you want.

Once you have received the PCBs, it's time to solder the components on it to make the final product. There is nothing complicated in it. Just keep a printout of the schematic in front of you and start putting the components one by one in the PCB. Make sure there is no short in power and ground after the completion of this step.

One thing I just want to clear here is that the caps values are don't need to be perfect. Something close to those values will do the job. Same goes for the resistors. But keep the R1 and R2 values of LM317 as it is told.

One thing you may find odd that the arduino that I made has two reset buttons on it. Actually what happened is that when I designed the layout, I used a four pin push button as a reference. But at the time of soldering I realized that I don't have that. So I soldered 2 two pin reset switches on place. Nothing is special in there.

Connect the breakout board to the arduino and connect that to the computer. Open device manager and observe the com port of the usb to ttl converter. In arduino IDE select the com port and board correctly. Now here comes a tricky part. If your ftdi board das a DTR pin and it is connected to reset then just save the program and upload that to the arduino as usual. There will be no error. But if you don’t have the DTR pin like me, then before clicking on upload, hold down the reset button on the board, and then press upload. Hold the button till the program is compiling, when the ide says ‘uploading’ , then release the reset switch. Then the code will be uploaded.

![Screenshot (1106)](https://github.com/Arush-om/Diy-Arduino/assets/134673721/fd93482b-0898-4043-8dc8-fe643f5d5bf0)

![Screenshot (1104)](https://github.com/Arush-om/Diy-Arduino/assets/134673721/c20938bd-9f4c-4360-af41-1a37cf4ed848)

It is very important to remember that 3.3v regulator does not have the same pinout as the 7805. With the printed side towards you and the pins down the one furthest to the left is ground, the center is the output, and the furthest right is the input. Again you will need two decoupling capacitors. connect one of the 10 uf tantalum caps between output and ground and the other between input and ground paying attention to polarity. the positive lead should be labeled on the front of the cap, the other is negative, and be sure negative leads on these caps get connected to the furthest left pin on the regulator.

For starters you should probably label each pin on your female headers to avoid confusion later. then solder the headers to the board and connect them to the respective pin on the chip, according to the pin diagram above.

This process is very tedious, so just have some patience and you should be fine. Also planning out how you are going to connect everything before hand will go a long way. You will probably have a lot of wires intersecting. after a while I was forced to start connecting pins on the bottom of the board to prevent this.
