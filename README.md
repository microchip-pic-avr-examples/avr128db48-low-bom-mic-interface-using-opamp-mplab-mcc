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

* [MPLAB® X IDE](http://www.microchip.com/mplab/mplab-x-ide) 5.40 or newer
* [MPLAB® XC8](http://www.microchip.com/mplab/compilers) 2.31 or a newer compiler
* [MPLAB® Code Configurator (MCC)](https://www.microchip.com/mplab/mplab-code-configurator) 4.0.0 or newer
* MPLAB® AVR-Dx_DFP version 1.6.88 or newer

## Hardware Used

* [AVR128DB48 Curiosity Nano](https://www.microchip.com/DevelopmentTools/ProductDetails/PartNO/EV35L43A)
* Electret microphone
* One 2.2kΩ resistor
* One 1µF capacitor

## Setup

* Connect the hardware together as seen in the schematic of the application note

## Operation

* Connect the AVR128DB48 Curiosity Nano to a computer using a USB cable
* Clone the repository or download the zip to get the source code
* Open the .X project with MPLAB
* Press Make and Program Device to run the example 

## Conclusion
After going through this example, you should have a better understanding of how to set up the OPAMP peripheral to amplify weak signals from sensors into detectable signals for the MCU.  


