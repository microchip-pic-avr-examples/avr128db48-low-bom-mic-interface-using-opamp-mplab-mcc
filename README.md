<!-- Please do not change this logo with link -->
[![MCHP](images/microchip.png)](https://www.microchip.com)

# Low-BOM Microphone Interface Using the Analog Signal Conditioning (OPAMP) Peripheral
<p align="left">
  <img width=800px height=auto src="images/setup.png">
</p>

A new feature introduced in the AVR® DB family of microcontrollers (MCUs) is the Analog Signal Conditioning (OPAMP) peripheral. In this example, the OPAMP peripheral is used to amplify a weak signal up to the 100-millivolt range so that it can be detected by an analog comparator in the MCU or converted to a digital signal by the MCU’s analog-to-digital converter (ADC). 
Up to three internal op amps are available for configuration in the AVR DB. The configuration for this example can be seen in the figure above. Including the MCU the setup uses an external electret microphone, a resistor, and a capacitor. For more information about setup and code, see the [application note](https://microchip.com/DS00003631).

## Related Documentation

* [AN3631 - Low-BOM Microphone Interface Using the Analog Signal Conditioning (OPAMP) Peripheral](https://microchip.com/DS00003631)
* [AVR128DB48 Curiosity Nano User Guide](https://www.microchip.com/DS50003037)
* [AVR128DB48 Device Page](https://www.microchip.com/wwwproducts/en/AVR128DB48)

## Software Used

* MPLAB® X IDE 5.50 or newer [(http://www.microchip.com/mplab/mplab-x-ide)](http://www.microchip.com/mplab/mplab-x-ide)
* MPLAB® XC8 2.32 or a newer compiler [(http://www.microchip.com/mplab/compilers)](http://www.microchip.com/mplab/compilers)
* MPLAB® Code Configurator (MCC) 4.1.0 or newer [(https://www.microchip.com/mplab/mplab-code-configurator)](https://www.microchip.com/mplab/mplab-code-configurator)
* MPLAB® Melody Library 1.84.2 or newer [(https://www.microchip.com/mplab/mplab-code-configurator)](https://www.microchip.com/mplab/mplab-code-configurator)
* MPLAB® Code Configurator (MCC) Device Libraries AVR® MCUs 2.70 or newer [(https://www.microchip.com/mplab/mplab-code-configurator)](https://www.microchip.com/mplab/mplab-code-configurator)
* Microchip AVR-Dx Series Device Support (1.8.112) or newer [(https://packs.download.microchip.com/)](https://packs.download.microchip.com/)

## Hardware Used

* [AVR128DB48 Curiosity Nano](https://www.microchip.com/DevelopmentTools/ProductDetails/PartNO/EV35L43A)
* Electret microphone
* One 2.2 kΩ resistor, R5
* One 1 µF capacitor, C1

## Peripherals Configuration using MCC
This section describes how this example was configured in MCC.

### Added Peripherals
* The *OPAMP* driver was found under *Device Resources*, and added

![OPAMP_driver](images/MCC_Melody_adding_OPAMP_driver.png)

* The *Builder* tab showed the system, with the added *OPAMP* peripheral

![Builder](images/MCC_Melody_builder.png)

* Clicked on the *OPAMP* block, to enable the OPAMP driver *Easy View* and configured as shown below

![OPAMP System](images/MCC_Melody_OPAMP_System.png)

![OP0](images/MCC_Melody_OPAMP_OP0.png)

**Note:** *System Gain* is calculated based on settings from both *OP0* and *OP1*, and the screenshot shows the calculated value once *OP1* was setup, as shown below. 

![OP1](images/MCC_Melody_OPAMP_OP1.png)

* Clicked on *Generate* in the *Resource Management* tab to generate the source code

![Builder](images/MCC_Melody_generate.png)


## Setup
* Connect the hardware together as shown in the schematic above:
  * Electret microphone
  * Resistor, R5
  * Capacitor, C1

## Operation

* Connect the AVR128DB48 Curiosity Nano to a computer using a USB cable
* Clone this repository or download the *.zip to get the source code
* Open the `avr128db48-low-bom-mic-interface-using-opamp-mplab-mcc.X` project in MPLAB X
* Click *Clean and Build* to build the example

![Build](images/clean_and_build.png)

* Click *Make and Program Device* to run the example

![Program](images/make_and_prog.png)

* If no tool has been chosen, a window will open, select the *AVR128DB48 Curiosity Nano* evaluation kit. The tool can also be chosen in the project settings.

## Summary
After going through this example, you should have a better understanding of how to set up the OPAMP peripheral to amplify weak signals from sensors into detectable signals for the MCU.  


