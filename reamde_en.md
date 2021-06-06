This file is translated from `reamde.md` by translation software. It is only used to provide index for search engines. I do not guarantee that it expresses accurate meaning.

# Ryzen Hackintosh

## My configuration is as follows

Motherboard: Asus-Rog-B550I-Gaming

CPU: AMD Ryzen 5800X

Graphics card: AMD Radeon RX 6900XT

Memory: Chi magic light halberd 8G*2

Case: Patriot S1

Power supply: Great Wall TF850

Heat dissipation: Kyushu Fengshen Fortress 240ex

**Note: This configuration is not a recommendation for purchase, it is only assembled by me using existing existing hardware**

------

This EFI is built according to https://dortania.github.io/OpenCore-Install-Guide/AMD/zen.html, and some modifications have been made, see `tips.md`, I also tried to build according to the Chinese world Some tutorials were built (mainly because they were outdated), but they all failed without exception.
In the end, I bit the bullet and finished the official AMD build tutorial of OpenCore. The final result did not disappoint me, and the installation and startup were successful.

I don't recommend that you use my EFI directly, but build it yourself through the official opencore tutorial. If you have similar configurations to me, I recommend you to look at the `tips.md` file, which lists some of the problems I encountered.

## Available

* WIFI and Bluetooth are available

## Known issues

[] Booting is slow, it only takes several seconds to start opencore, which is suspected to be due to the debug version of opencore

[] No boot sound

[] Unable to use network cable

## update record

### 2021/06/06
Finished installation and startup, currently opencore is still a debug version
