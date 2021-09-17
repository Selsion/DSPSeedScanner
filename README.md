
# DSPSeedScanner
This github repo contains seed lists for the game [Dyson Sphere Program](https://store.steampowered.com/app/1366540/Dyson_Sphere_Program/) produced from my standalone seed scanner. The different lists are provided as files in this repo, and are described below.

The code for the seed scanner is currently not included in this repo, since it uses decompiled code from the game. No executable is available for public use yet, since configuration is currently done by modifying the code. The scanner may in the far future be changed to not rely on using decompiled code, if such a scanner proves to not be too difficult to make. If the scanner ever reaches that stage, then its code will be shared on this repo, and proper user configuration will be added.

## Seed lists
- [3bg.csv](https://github.com/Selsion/DSPSeedScanner/blob/main/seed_lists/3bg.csv): All 435383 64-star seeds with 3 blue giants (3 is the max). Each line contains the seed, followed by the 3 blue giants' luminosities sorted from greatest to smallest. Formatted as a csv to allow importing into spreadsheet software
- [starter_3_moons.txt](https://github.com/Selsion/DSPSeedScanner/blob/main/seed_lists/starter_3_moons.txt): All 588008 seeds where the starter system has 3 moons orbiting the gas/ice giant
- [starter_2_moons_1_TL.txt](https://github.com/Selsion/DSPSeedScanner/blob/main/seed_lists/starter_2_moons_1_TL.txt): All 436735 seeds where the starter system has 2 moons orbiting the gas/ice giant and 1 tidally locked planet
- [26_um_patches.csv](https://github.com/Selsion/DSPSeedScanner/blob/main/seed_lists/26_um_patches.csv): All 862 64-star seeds containing 26 [unipolar magnet vein](https://dsp-wiki.com/Unipolar_Magnet_Vein) patches (26 is the max). Each line contains the seed, total number of UM veins, and total UM amount

## Requests
You can request specific scans by contacting me on discord at Selsion#0769. The scanner does not yet support vein or terrain generation, because that slows down scanning immensely. Here are time estimates for different types of scans over all 100 million 64-star seeds when run with 24 threads with my AMD Ryzen 9 5900X:

- Scanning only starter system properties (star and/or planet properties): ~70 seconds
- Scanning only star properties (no planet properties): ~18 minutes
- Scanning star and planet properties for all stars and planets: ~70 minutes IIRC

Here is a non-exhaustive list of properties you might want:

- Some number of moons around an ice/gas giant
- Some number of O-type systems in the cluster ([Related seed list](https://dsp-wiki.com/Starting_Seeds#Maximum_O-Type_Stars))
- A specific [planet or star type](https://dsp-wiki.com/Stars_and_planets)
- Special planet properties like high solar energy ratio, tidal locking, horizontal rotation, etc.
- A custom function to maximize or filter by, such as sum of all luminosities
- A large max dyson sphere radius, such as 1.35 times as big as the innermost planet, to allow 100% [ray receiver](https://dsp-wiki.com/Ray_Receiver) effectiveness everywhere on the planet without using [graviton lenses](https://dsp-wiki.com/Graviton_Lens)

When making a request, please be specific with your requirements. For example, "good resource spread" or "close to the starter system" are too vague, while "x star with a luminosity of at least 2.0,"  "5 satellites around some gas/ice giant," or "x star within 5 light-years of the starter system" are more specific. If your scan would take over an hour to finish and your request is too specific to post on this repo, then I may give you the executable to scan the seeds yourself. In that case, scans may take a long time if you use a low number of threads. There are cases where I can first filter by a computationally cheap property (e.g. TL planet in the starter system), then scan for more computationally expensive properties (e.g. a blue giant with a luminosity of at least 2.5 in the cluster) on those filtered seeds. In those cases, you can get away with requesting more computationally expensive properties.

## Issues
If you have any bugs or issues to report (such as incorrect data in a seed list), then either contact me on discord at Selsion#0769, or raise an issue on this github repo.

## Todo
Add the other seed lists
