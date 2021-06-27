# BatteryUpgrade-UserManual
A guide for the BatteryUpgrade software. This software achieves the impossible, providing backwardscompability for installing newer batteries into older LEAFs. Since not 100% of the communication is known, some bugs still exists, please see the issues page for more info. The latest version of the BatteryUpgrade software is v2.41

## Changelog
- v2.36 - Initial release for this repository and all known issues. Lots of bugs have been fixed in the 50+ versions before this :) 
- v2.38 - SOH is no longer at constant 99% for 2011-2013 battery upgraded vehicles
- v2.40 - The instrumentation cluster now shows correct minutes remaining for time to charge to 100/80% ( Issue #10 )
- v2.41 - Adds a new charge power selection to RapidgateDodger, 25kW@FAN7
- v2.42 - Internal improvements, rewrite of functions
- v2.43 - AZE0: The instrumentation cluster now shows correct minutes remaining for time to charge to 100/80% ( Issue #10 )
- v2.44 - ZE0: Block sending 0x5BF towards battery (Saves CPU and bus load, newer batteries should not recieve this ZE0 data)
- v2.45 - Rewrite thermal management to be more in line with 2018+ models. When the battery is cold the regen/motor output is more limited compared to previous versions, thus improving the lifetime of the battery by making it harder to overstress it.
- v2.46 - Fix ChargeCurrent feature sometimes gets activated by remote heating request. This would show up as chargespeed max 1kW after using remote heating. Now added so if condition is held for more than 16s it reverts to full power.
- v2.47 - Add new SOC% dash feature for ZE0 users. How to use it: https://www.youtube.com/watch?v=LuiKp4wjlpQ

## Installation guide
CAN-bridge step-by-step installation video:

ZE0 https://www.youtube.com/watch?v=-gLMUeE2mXo

AZE0 https://www.youtube.com/watch?v=Iq4NsAjvCn0 (Thanks Gelisob!)

e-NV200 https://youtu.be/OxF6pKY6dgw (Thanks Glyn Hudson!)


Battery install guide:

ZE0 https://www.youtube.com/watch?v=1Dwsk9lnr6I

e-NV200 https://youtu.be/RmzlNWBnZGQ (Glyn Hudson) 

 - The CAN-bridge needs a constant +12V supply, it is always on and ready to translate the communication between battery and vehicle. If you connect it to switched 12V, it will not wake up fast enough, and miss important messages causing vehicle to not start

## Firmware update guide
See this video for detailed steps https://www.youtube.com/watch?v=eLcNSo2Vn6U

# Frequently asked questions
 - After CAN-bridge is installed, any 2014+ 24/30/40/62kWh battery can be installed
 - The BatteryUpgrade software contains some extra features (BatterySaver,RapidgateDodger etc.), see this page for description of these features: https://github.com/dalathegreat/LeafEnhancer-UserManual
 - Leafspy should not be used while vehicle is charging, since the CAN-bridge needs to do extra battery-polling while vehicle is charging. Also Leafspy will show wrong data while charging, see Issue #8
 - ZE0, The vehicle needs to be fully charged after the battery upgrade is completed, in order for the instrumentation to sync how full 12/12bars should be. If you start to drive it right after the upgrade, it will decrement the bars incorrectly. Simply charging it will resolve the situation, and bars will work like they should.
 - AZE0 , The instrumentation state of charge % will show the true battery % after vehicle is upgraded (same as Leafspy shows). This is useful since it is more precise on lower SOC values, and helps you stay confident when taking the vehicle close to empty. Due to this reason, the vehicle will also show somewhere between 94-98% when fully charged, instead of 100%. This is completely normal.
 - Q: Help, my new battery is throwing isolation error codes at fastchargers! A: Most likely moisture has gotten inside the battery, this is typical on salvage batteries that have been left outside/pressure washed. Solution is to open up the battery and do a visual inspection.
