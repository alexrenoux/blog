---
title: The EEPROM Memory in 2025
summary: Read about the EEPROM memory market in 2025 from a Technical Marketing Engineer.
date: 2026-01-04
series:
weight: 1
aliases:
  - /eeprom-memory-2025
tags:
  - semiconductor
  - eeprom
author:
  - Alexandre Renoux
cover:
  image: images/papermod-cover.png
  hiddenInList: true
---
Since 2025 and I don't know for how long, I have been in charge of the EEPROM Japanese market for STMicroelectronics a semiconductor manufacturer. This product despite being quite old was very new to me since I came from a microcontroller background where embedded memories were usually Flash and RAM.

With my new discoveries, I wanted to write this article to share a bit about this potentially unknown semiconductor device being used in billions of devices.
# A bit of history

EEPROM memories were being manufactured more than 40 years ago and are still present in many BOM's applications. 
Why ?
Because the reliability and longevity of these products is unmatched.
In the memory market, you can go cheap, you go high density, you can go fast and you can go high reliability but you can't have everything all at once.
One other element is the data retention aspect. Depending on the application, in some cases you want the memory to retain the information even when power is off. And in other cases you don't.

# The EEPROM position in the memory market

In the below table, I summarize the benefit of each main memory type used nowadays.

Flash memories 
- Cheap
- Data retention based on floating gate
- Reliability: low to medium (with ECC), 10K to 100K write cycles, low temperature resistance, need to be changed at least every 10 years.
- Medium power consumption
- Hight densities up to 8TB
- 2 main types : NOR and NAND (3D NAND is the biggest market)
- Usage : SSDs, flash drive, microcontroller internal memory
RAM
- Relatively cheap
- No data retention based on capacitors
- Reliability: low but not very important since we refresh constantly the memory cells
- Medium to high power consumption
- High densities up to 64GB per die
- Computer (cache, GPU), Servers, Embedded (MCU, MPU)
- Need is constantly increasing
- RAM is becoming more important than Flash
- The need to go 3D is important
HBM
- Very expensive
- Extremely high performance and high bandwidth 
- Wafer stacking necessary 
- Very high densities up to 512GB per die
- Reliability: same as RAM but yield is not yet optimal, lots of wafers used for HBM
- High power consumption
- Mainly for AI servers
EEPROM
- Relatively expensive for the size but around 10 cents on average
- Low densities up to 4Mbits (512KB)
- Reliability: very high (high write cycles up to 4 millions, high temperature support up to 150°C, 200 years data retention), Can run constantly for 20 years.
- Very low power consumption
- Used mainly in Embedded (high write cycling), BIOS storage for computers, config for camera sensors and RAM sticks

Based on the above table, we can clearly see that EEPROM is targeting a market that no other memory type can cover perfectly and this is why EEPROMs are still being commonly used even after 40 years.
Of course, EEPROM have not been the same for the past 40 years, the technology has matured with time and numerous companies have worked on increasing efficiency through better designs and the use of more advanced technology nodes. One node that will be used soon is the 80nm but due to transistors getting smaller, 5V is not sustainable anymore so new EEPROMs are gradually moving towards 3.3V support instead of 5V

Various companies are making and selling EEPROMs these days but the most prominent ones are ST from France, Microchip from US and several Chinese competitors like Fudan, Giga Device or Giantec.

The market is stagnating or retracting at a slow pace but despite this, innovation is still ongoing due to market size still significant.

# How EEPROM store data

Data is stored using a MOSFET structure with a floating gate surrounded by Silicon Oxide (SiO2) to trap charges inside the gate and induce a bias in the functioning of the MOSFET.

Now for a certain applied voltage, the resulting current will be zero or a higher value than usual.
- When the gate is charged negatively (electrons were transferred to the floating gate), holes will be accumulating on the source-drain path, due to electricity forces, making it harder to move electrons from the source to the drain. This means a 0.
- When the gate is charged positively (excess in holes, electrons left the floating gate), electrons will be accumulating on the source-drain path, leading to more electrons flowing with a certain applied voltage. This means a 1.

In order to write a value to the memory cells, a high voltage of more than +-12V needs to be applied to the gate-source junction to force electrons in or out of the floating gate by jumping through the thin SiO2 insulator.

This method is quite violent for the material which leads to cell aging through parasite in the thin SiO2 layer.
Also because of the high voltage, the MOSFET size cannot be reduced under 180nm due to material properties limitations. With some patented tricks and solutions known to memory makers, this can be partly overcome to still reduce the die size for the same densities.

# What's next ?

EEPROM memories are still being improved for ever smaller dies and cheap manufacturing while maintaining current reliability standards.

To go above the 4Mbit density threshold, ST has launched a memory called the Page EEPROM. This memory uses their in-house 40nm eSTM flash memory technology and has been designed to sustain 500K write cycles all the way to 105 degrees.
This makes the Page EEPROM an alternative to EEPROM duplication when the write cycling specs are not in the million of cycles.
It can also replace Flash memories in certain applications where data logging is crucial and battery/environmental requirements are strict.

In the future, more techniques will be found to go smaller while maintaining low price and high reliability.
