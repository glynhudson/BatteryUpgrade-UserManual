# BatteryUpgrade-UserManual
A guide for the BatteryUpgrade software. This software achieves the impossible, providing backwardscompability for installing newer batteries into older LEAFs. Since not 100% of the communication is known, some bugs still exists, please see the issues page for more info. The latest version of the BatteryUpgrade software is v2.38

## Changelog
v2.36 - Initial release for this repository and all known issues
v2.38 - SOH is no longer at constant 99% for 2011-2013 battery upgraded vehicles

## Installation guide
CAN-bridge installation video (ZE0) https://www.youtube.com/watch?v=-gLMUeE2mXo

AZE0 battery into ZE0 example video https://www.youtube.com/watch?v=1Dwsk9lnr6I

## Firmware update guide
See this video for detailed steps https://www.youtube.com/watch?v=eLcNSo2Vn6U

# Frequently asked questions
 - The BatteryUpgrade software contains some extra features, see this page for description of these features: https://github.com/dalathegreat/LeafEnhancer-UserManual
 - Leafspy should not be used while vehicle is charging, since the CAN-bridge needs to do extra battery-polling while vehicle is charging. Also Leafspy will show wrong data while charging, see Issue #8
 - Q: Help, my new battery is throwing isolation error codes at fastchargers! A: Most likely moisture has gotten inside the battery, this is typical on salvage batteries that have been left outside/pressure washed. Solution is to open up the battery and do a visual inspection.
