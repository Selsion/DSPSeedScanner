
# DSPSeedScanner
This github repo contains seed lists for the game [Dyson Sphere Program](https://store.steampowered.com/app/1366540/Dyson_Sphere_Program/) produced from my standalone seed scanner. The different lists are provided as files in this repo, and are described below.

The code for the seed scanner is currently not included in this repo, since it uses decompiled code from the game. No executable is available for public use yet, since configuration is currently done by modifying the code. The scanner may in the far future be changed to not rely on using decompiled code, if such a scanner proves to not be too difficult to make. If the scanner ever reaches that stage, then its code will be shared on this repo, and proper user configuration will be added.

## Seed lists
- [3bg.csv](https://github.com/Selsion/DSPSeedScanner/blob/main/seed_lists/3bg.csv): All 435383 64-star seeds with 3 blue giants (3 is the max). Each line contains the seed, followed by the 3 blue giants' luminosities sorted from greatest to smallest. Formatted as a csv to allow importing into spreadsheet software
- [starter_3_moons.txt](https://github.com/Selsion/DSPSeedScanner/blob/main/seed_lists/starter_3_moons.txt): All 588008 seeds where the starter system has 3 moons orbiting the gas/ice giant
- [starter_2_moons_1_TL.txt](https://github.com/Selsion/DSPSeedScanner/blob/main/seed_lists/starter_2_moons_1_TL.txt): All 436735 seeds where the starter system has 2 moons orbiting the gas/ice giant and 1 tidally locked planet
- [26_um_patches.csv](https://github.com/Selsion/DSPSeedScanner/blob/main/seed_lists/26_um_patches.csv): All 862 64-star seeds containing 26 [unipolar magnet vein](https://dsp-wiki.com/Unipolar_Magnet_Vein) patches (26 is the max). Each line contains the seed, total number of UM veins, and total UM amount
- [star_2.5ly_2.3L.csv](https://github.com/Selsion/DSPSeedScanner/blob/main/seed_lists/star_2.5ly_2.3L.csv): All 970542 seeds with a 2.3L+ star within 2.5 light-years of the starting system. The seed must be generated with a specific star count. Each entry in the csv file contains the seed and star count needed for generation, as well as the luminosity and distance for the nearby star.
- [ashen_fire_ice_tl.txt](https://github.com/Selsion/DSPSeedScanner/blob/main/seed_lists/ashen_fire_ice_tl.txt): All 1117 seeds with an ashen gelisol moon with fire ice as well as a tidally locked planet in the starting system. These are ideal for speedrunning.
- [4_ocean_sats.csv](https://github.com/Selsion/DSPSeedScanner/blob/main/seed_lists/4_ocean_sats.csv): All 7 64-star seeds containing a star with 4 ocean-type planets orbiting a gas planet.
- [4_tl_O.csv](https://github.com/Selsion/DSPSeedScanner/blob/main/seed_lists/4_tl_O.csv): All 38 64-star seeds containing an O-type star with 4 tidally locked planet orbiting it. Each seed is accompanied with the corresponding O-type's luminosity. 
- [7_o_types.csv](https://github.com/Selsion/DSPSeedScanner/blob/main/seed_lists/7_o_types.csv): All 38988 64-star seeds with at least 7 O-type stars. Each seed in the csv file is accompanied with the number of O-types in the seed.
- [rainbow_giants.csv](https://github.com/Selsion/DSPSeedScanner/blob/main/seed_lists/rainbow_giants.csv): All 124788 64-star seeds with 3 different giant star types. Each seed in the csv file has the counts for each type listed.

## Requests
You can request specific scans by contacting me on discord at Selsion#0769. The scanner does not yet support exact vein or terrain generation, because that slows down scanning immensely. I can however get the number of vein patches within an error of +-1, and estimate the total vein amounts. Here are time estimates for different types of scans over all 100 million 64-star seeds when run with 24 threads with my AMD Ryzen 9 5900X:

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

## Issues
If you have any bugs or issues to report (such as incorrect data in a seed list), then either contact me on discord at Selsion#0769, or raise an issue on this github repo.

## To do
Add the remaining seed lists
