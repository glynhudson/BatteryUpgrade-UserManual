# BatteryUpgrade-UserManual
A guide for the BatteryUpgrade software. This software achieves the impossible, providing backwardscompability for installing newer batteries into older LEAFs. Since not 100% of the communication is known, some bugs still exists, please see the issues page for more info. The latest version of the BatteryUpgrade software is v2.41

## Changelog
- v2.36 - Initial release for this repository and all known issues. Lots of bugs have been fixed in the 50+ versions before this :) 
- v2.38 - SOH is no longer at constant 99% for 2011-2013 battery upgraded vehicles
- v2.40 - The instrumentation cluster now shows correct minutes remaining for time to charge to 100/80% ( Issue #10 )
- v2.41 - Adds a new charge power selection to RapidgateDodger, 25kW@FAN7

## Installation guide
CAN-bridge step-by-step installation video (ZE0) https://www.youtube.com/watch?v=-gLMUeE2mXo

AZE0 battery into ZE0 example video https://www.youtube.com/watch?v=1Dwsk9lnr6I

 - The CAN-bridge needs a constant +12V supply, it is always on and ready to translate the communication between battery and vehicle. If you connect it to switched 12V, it will not wake up fast enough, and miss important messages causing vehicle to not start

## Firmware update guide
See this video for detailed steps https://www.youtube.com/watch?v=eLcNSo2Vn6U

# Frequently asked questions
 - The BatteryUpgrade software contains some extra features (BatterySaver,RapidgateDodger etc.), see this page for description of these features: https://github.com/dalathegreat/LeafEnhancer-UserManual
 - Leafspy should not be used while vehicle is charging, since the CAN-bridge needs to do extra battery-polling while vehicle is charging. Also Leafspy will show wrong data while charging, see Issue #8
 - AZE0 , The instrumentation state of charge % will show the true battery % after vehicle is upgraded (same as Leafspy shows). This is useful since it is more precise on lower SOC values, and helps you stay confident when taking the vehicle close to empty. Due to this reason, the vehicle will also show somewhere between 94-98% when fully charged, instead of 100%. This is completely normal.
 - Q: Help, my new battery is throwing isolation error codes at fastchargers! A: Most likely moisture has gotten inside the battery, this is typical on salvage batteries that have been left outside/pressure washed. Solution is to open up the battery and do a visual inspection.
