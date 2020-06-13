# Samaroli
A water-cooled Hackintosh with custom hardline loop, using OpenCore bootloader!

## Main PC Parts

|Component|Make|Part Name|
|---|---|---|
|CPU|Intel|Core i9-9900KS 5GHz Special Edition|
|Motherboard|Gigabyte|Z390 Designare, BIOS version F9G|
|RAM|Corsair|Vengeance RGB Pro 64 KB (4 x 16 GB) DDR4-3200 CL16 ver 5.32|
|GPU|ASUS|ROG Strix RX-5700-XT 8G|
|Internal Storage|Samsung|970 EVO Plus NVMe M.2 SSD 1TB x2|
|WiFi/BT|fenvi|FV-T919 Wireless Network Adapter|
|10G Ethernet|LR-LINK|94T0255 PCIe x4 10G SIngle-Port Server Adapter|
|RAID Card|Highpoint|RocketRAID 2721 (1xInt/1xExt Mini-SAS ports)|
|Fans|ThermalTake|Riing Trio 12 x6|
|Fan Hub|ThermalTake|TT Sync Controller|
|RGB Hub|Gamer Storm|5V DRGB to 12V ARGB Convertor/Hub|
|USB Hub|Generic|PAN8USB-G01 USB3.0/2.0 x2 PCB Internal Hub|
|Case|Lian Li|O11 Dyanmic XL Full Tower Case|
|Power Supply|Seasonic|Focus GX-580 850W|

## Watercooling Parts

|Component|Make|Part Name|
|---|---|---|
|Distro Plate/Pump|EKWB|O11 Dynamic XL Distro Plate G1 D-RGB + DDC 3.1 PWM|
|CPU Waterblock|EKWB|EK-Velocity RGB - Full Nickel|
|GPU Waterblock|EKWB|EK-Quantum Vector Strix RX 5700 +XT D-RGB - Nickel + Plexi with Nickel Blackplate|
|Radiators|EKWB|EK Coolstream Classic PE 360 x2|
|Fittings|EKWB|EK-HTC Classic 16mm – Black Nickel|
|Tubings|Bitpower|16mm Outer Diameter PETG hard tubings|
|Coolant|EKWB|EK Cryofuel Concentrate - Amber Orange|

## External RAID Array Parts (existing)

|Component|Make|Part Name|
|---|---|---|
|Enclosure|Stardom|4 HDD eSata enclosure|
|Storage|Toshiba|Enterprise Series 10T HDD x4|

## Build Notes
- First time getting into watercooling -- planning and bending hardline PETG tubes was hard but a lot of fun!
- Getting all the RGB wired up was unexpectedly challenging. Gigabyte Z390 Designare supports only 12V ARGB (analog) but not 5V DRGB (digital). I ended up with mixed ARGB and DRGB devices connected to the analog motherboard using Gamer Storm's DRGB to ARGB converter hub. I was able to synchronize RGB via Gigabyte's AmbientLED app -- very barebone but servicable. Note that some of the lighting effects are not perfect, but good enough for what I want.
- The Lian Li O11 Dynamic XL case comes with 4x USB 3.0/2.0 ports (plus an USB 3.1 Type C port). I used an internal USB 3.0/2.0 hub PCB connected to F_USB30 (HS05/SS05 and HS06/SS06) to support all 4 physical ports.
- This is also my first OpenCore build. For my own learning and education, I chose not to take a pre-built EFI package as-is. I followed Dortania's very well-written [OpenCore Desktop Guide](https://dortania.github.io/OpenCore-Desktop-Guide/) to customize my own config.plist and SSDT's -- the idea is that I want to understand the exact purpose of every changes to the sample.plist before I add to mine.
- CaseSJ's incredibly detailed [guide](https://www.tonymacx86.com/threads/success-gigabyte-designare-z390-thunderbolt-3-i7-9700k-amd-rx-580.267551/) on this motherboard also provided a wealth of information to explore (the thread is 2,254 pages long as of this writing!)
