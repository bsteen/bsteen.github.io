# General Information
- Last updated: 2024-02-22
- Mazda Mazda3
- 2010 - 2013, 2nd Generation (BL)
- <https://en.wikipedia.org/wiki/Mazda3#Second_generation_(BL;_2008)>
- Example used: 2010 Mazda Mazda3s Sport (2.5L engine), 5 door (hatch back), 5 speed automatic transmission

# Mazda Original Equipment Parts
- When looking for Mazda original equipment (OE) parts, there are 3 main store types to choose from: Mazda Dealerships, "Various OE" part sellers (places that sell OE parts for many different brands), and the usual independent party seller platforms (Amazon, eBay, etc.)
- In general, but especially with the various OE websites, send them a message before ordering parts to make sure all the parts are actually in stock
- It seems random whether an online seller will ship fluids or not
  - For example: automatic transmission fluid (ATF) and engine coolant
- I've had both Mazda dealerships and various OE sites say they don't ship engine coolant: "We do not ship hazardous material"
    - Specifically for coolant, some sites explicitly state it is not available for shipping, while other don't mention it until after they refund your order
- For fluids like ATF, it is a mixed bag
    - I've had one dealer say they don't ship liquids period, while 2 others shipped ATF without question
    - I've also had a general OE website say they would ship ATF, but they never have the Mazda M5 in stock
    - Dealers will pretty much always have ATF and other common fluids in stock, but you again have to make sure they will actually ship
    - You can usually select pick up for dealerships if you live nearby

## Mazda Dealership Websites
- <https://getmazdaparts.com>
    - Lunenburg, MA; address is the same for North End Mazda
    - Order payments are made to Colonial Imports West Inc.
    - Shipped items the afternoon I ordered them, took a week to arrive
    - Prices are generally one of the lowest out of other Mazda dealer sites
    - Does ship ATF
- <https://mazdacarpartsonline>
    - Cincinnati, OH; part of the Jake Sweeney Automotive dealership network
    - Order payments are made to Jake Sweeney Chevrolet Imports
    - They do not ship fluids, including ATF
- <https://mazdaswag.com>
    - Peoria, IL; part of the Scherer Automotive dealership network
    - Order payments are made to Scherer Automotive Inc.
    - Time from purchase to shipping was pretty quick
    - Order arrived in 4 days of shipping, even with the cheapest shipping option
    - They usually have a 10% of shipping coupon; check the website header or coupon sites for it
    - Does ship ATF

## Various OE Websites
Various OE parts websites (places that sell OE parts for many different brands) will usually have cheaper prices than Mazda dealership websites. The issue is that they are likely to not have the part in stock even when they claim it is. They also take a longer time to ship out the parts versus dealer websites.
- <https://getoemparts.com>
    - Cranston, RI; part of the Tasca Automotive dealership network (Tasca Parts)
    - Order payments are made to NewAutoParts.com (New Auto Parts, LLC), another OE parts seller presumably also part of Tasca Parts
    - Generally has the lowest prices for OE Mazda parts anywhere else on the internet
    - The issue is that they've told me several times that common Mazda parts are either not actually in stock or need to be special ordered
    - They take their time between receiving the order and actually shipping the parts
    - If the item is actually in stock and you don't mind waiting for shipping, this place is usually the cheapest by a few dollars
    - They do ship ATF, but M5 ATF always seem to be out of stock

# OBD2 Readers and Software
- For Bluetooth OBD2 readers, I've had good experiences with the [BAFX Products Wireless Bluetooth Diagnostic OBD2 Scanner](https://www.amazon.com/dp/B005NLQAHS)
- Once you get passed the usual annoyances of Bluetooth pairing, it seems very consistent
- The reader you use isn't that important, as long as it allows you to connect to a phone, tablet, or laptop (or a desktop PC if you really want)
- The software to interpret the reader's data is the most important aspect of reading the BL's OBD2 and CAN bus
- Because of that, I do not recommend any of the cheap wire connection readers you can get at Walmart or Harbor Freight
  - They usually only read and clear basic Diagnostic Test Codes (DTCs)

## Torque Lite / Torque Pro (Not Recommended)
- <https://torque-bhp.com>
- Torque Lite, Android, free demo: <https://play.google.com/store/apps/details?id=org.prowl.torquefree>
- Torque Pro, Android, paid: <https://play.google.com/store/apps/details?id=org.prowl.torque&hl=en_US&gl=US>
- This app is recommended by a lot of people online, but it is not optimized for Mazda's PIDs (Parameter IDs) that are outside the OBD2 standard
- **For example, it can't read the automatic transmission fluid temperature (TFT / transmission fluid temperature) by default**
- The UI has cheesy graphics, several layer deep submenus, and annoying dial selectors
- It can read the BL's active DTCs, but not pending ones
- You do have the ability to add custom defined PIDs, but good luck finding a set online that works with the BL
- Trying to read the TFT, for example: the default transmission temperature PID, the multiple "[FORD]" specific PIDs, and a custom PID formula I found online all do not work
  - There was a Mazdaspeed 3/6 plugin for Torque, but the link to it is dead
- There are plenty of other PIDs available in Torque that will not work because the BL is not equipped with the nessary sensors
  - This is not Torque's fault, but don't be surprised when you can't read oil temperature or pressure
  - The BL does not have sensors for these beside an oil pressure warning light (a pass/fail light)

## FORScan / FORScan Lite (Recommend)
- <https://forscan.org>
- FORScan Lite, Android and iOS, free demo or full paid
  - The demo version only allows reading of one PID at a time, and you can read but not clear DTCs
  - The Android version was removed from the Google Play store, so you have to download the APK directly from the developer website
- FORScan for Windows, free but very advanced features requiring a paid license
  - These advanced features include enabling/disabling the "smart" turn signal or changing the way automatic door locking/unlocking works
- **This is basically the best OBD2 companion software available for Mazda vehicles besides the actual [Mazda M-MDS Software](https://www.mazdaserviceinfo.com/mdars-software)**
- FORScan is made specifically for Ford, Mazda, Lincoln and Mercury vehicles, and it has all the Mazda-specific PIDs for the BL, **including transmission fluid temperature!**
  - It seems to be smart enough to only displays PIDs it can actually read from the BL, unlike Torque which shows all generic PIDs, regardless if they work
- FORScan can read individual modules on the BL, like the PCM, TCM, and BCM, and it shows pending and active DTCs on each (with the ability to clear them)
- **When connecting to the BAFX OBD2 reader, FORScan warns that the device is potentially not compatible, but I've had no issues**
- The Windows version is very powerful when it comes to reading and controlling the BL's modules
  - The Android version has reduced features, but it allows convenient reading/recording of PIDs from your mobile device

# Car Ramps
- RhinoGear RhinoRamps (11914MI, 12K lbs.) **DOES NOT** work with this car. The BL's front bumper is too long and low for the angle of these ramps. The bumper will scrape and push the ramps. This is with the stock ride height and wheel size. See the picture below. 
    - I know the ramp is on an uneven surface in this picture, but even on a flat surface, the ramp height is still 2+ inches over the top of the front bumper. They will not work with this car without a modification/extension to the ramps.

![image](https://user-images.githubusercontent.com/13274734/166124445-a9cb549e-c624-44e2-8fad-4026e3ecf831.png)

# DTC U0101 Transmission Control Module (TCM) Failure
TODO

# Mazda ATF M-V (Type M5)
## Idemitsu M vs. Mazda M5 ATFs
On the label for Mazda M5 ATF (part number [0000-77-112E-01](https://smile.amazon.com/dp/B00GKGCP5G)), it states it is manufactured by Idemitsu Lubricants America Corporation. Idemitsu also makes their own M5 compatible ATF, [Idemitsu Type M ATF](https://smile.amazon.com/dp/B071X4DRXN). I was hoping I could get the identical ATF from the OEM because it is cheaper than the Mazda branded ATF. After emailing ILAC, it turns out **Idemitsu branded and Mazda branded ATF formulations are NOT the same**. Below in a transcript of my initial email and the official response from ILAC:

```
Hello,
I was hoping any differences between Mazda branded Type M5 ATF (Mazda part # 0000-77-112E-01) and Idemitsu branded Type M ATF could be explained.
On the label for Mazda branded M-V (Type M5) ATF, it states it is manufactured by Idemitsu Lubricants America Corporation. Are there any differences between the Mazda M5 ATF made by Idemitsu and Idemitsu M ATF? Are they identical formulations?
Thank you.
---

From: Wolff, Alec <awolff[dot]1478[at]idemitsu[dot]com>
Date: Fri, Jun 24, 2022 at 10:24 AM
Subject: RE: **** Idemitsu Type M vs. Mazda M5 ATF
To: [me]

Hello,
And thank you for contacting Idemitsu Lubricants America.
Our aftermarket branded product was formulated based on the proper research and development done to create OE branded product. So, the formulations are not exactly the same.
Please, let us know if you have any questions.

Best Regards,

Alec Wolff | アレック　ウォルフ
Technical Sales Manager
Aftermarket

Idemitsu Lubricants America Corp.
3000 Town Center, Suite 2820
Southfield, MI 48075
```

I interpret this response as meaning Idemitsu created their Type M ATF formula to meet the specifications of Mazda's M5, but they probably aren't allowed to use the exact proprietary formula from Mazda's M5 (even though Idemitsu has to know the exact formula, since they make it). On one hand, the Mazda M5 is only about $2/quart more versus Idemitsu M, so if you really care about the exact formula, buy the Mazda M5. If price is really an issue, the Idemitsu M ATF is probably very close to Mazda's formula, but possibly not as good in some way. This is based on the assumption that Mazda's M5 is the most ideal formulation for Mazda transmissions and anything else is less than ideal. I have no proof of this, so I suppose the two could be identical for the vast majority of operating conditions. You would need to do a lot of testing and chemical analysis on both brands to prove this, including sending samples to a place like [Blackstone Laboratories](https://www.blackstone-labs.com/).

In terms of other aftermarket ATFs, I'm currently aware of only one other brand besides Idemitsu that claims to be solely compatible with Mazda M5 (not a multi-vehicle formula). That is [Beck/Arnley Premium Automatic Transmission Fluid for Type M5](https://www.beckarnley.com/parts/fluids/transmission-dual-clutch/atf-m5.html). I have not used this ATF and haven't done any research on it. I also haven't seen many people online recommending this over Mazda M5 or Idemitsu M. I have used Beck/Arnley FL-22 compatible coolant in the past, and it seems to be working well. I have no experience with this ATF, but the company seems to make decent aftermarket products that meet OE specifications.

**My final opinion on the issue is buy Mazda M5 for the most ideal product, then Idemitsu M if you can't find Mazda M5 for a good price.** Whatever you do, don't use the "multi-vehicle" ATFs. You need an ATF the meets the exact friction characteristics defined in the Mazda M5 specification. Idemitsu M ATF claims to do this and is recommended by others many times online. Multi-vehicle ATFs, while even cheaper, will have a very broad range to accommodate many transmissions, so I don't trust them to protect and maintain performance in my Mazda transmission in the long term.
