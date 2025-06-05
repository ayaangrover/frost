# Frost: Journal
Total time: ~34 hrs

### May 31: 5 hrs 43 min
During this session, I did a bunch of research, made my schematic, and began my pcb!

#### My Research:
1. Switches - MMD Princess Tactile, 48g. Thocky but tactile, budget friendly
2. MCU - Nice!Nano v2 for easy bluetooth and battery support. Has a lot of cheap knockoff versions on aliexpress
3. Keyboard Size - 75%, 81 keys - nice!nano only has 18 exposed pins so i removed 3 switches and put the mcu there. Less space needed as well since i can tuck the tiny battery under the mcu!
4. Case and fastening - screw the pcb to the case. simple and inexpensive
5. Plate - Nope, direct pcb mount. Looks cool, and i can do it all in white(matches my sister's desk color scheme)
6. Stabilizers - Cherry Stabs (Clip in, PCB Mount, from KBDFans)
7. Battery - 110mah, aliexpress - fits under MCU
8. Hotswap Sockets - kailh hotswap sockets from aliexpress
9. Diodes - THT, easier to solder
10. Keycaps - cheap $17 set from amazon

| Item               | Cost   |
|--------------------|--------|
| MCU (nice!nano v2) | $25.00 |
| Battery (110mAh)   | $3.00  |
| Switches           | $19.30 |
| PCB                | $59.00 |
| Stabilizers        | $9.50  |
| Hotswap Sockets    | $0.99  |
| Fasteners          | $3.48  |
| Diodes             | $2.34  |
| Keycaps            | $16.99 |
| **Total**          | **$139.60** |

#### Links:

MCU: https://bit.ly/43MxEzh (Free shipping, $25+)
Battery: https://bit.ly/4mHn5pD (Free shipping with mcu)
Switches: https://bit.ly/4dSzwen
Stabilizers: https://bit.ly/3FuRC9E
Hotswap Sockets: https://bit.ly/4dIZlgY
Fasteners(3.2mm diameter on the heatset inserts, m2 heatsets and screws): https://bit.ly/43L1Xq4 and https://bit.ly/3Zae3aP
Diodes: random aliexpress brand, doesnt matter which one
Keycaps: Any

Since the n!n has only 18 exposed pins, I'm going to do a 9x9 matrix in the schematic and drop 3 switches from a regular 75% layout and put my MCU and logo/name there.

Update - I just finished for today. Schematic is done, and pcb started but barely. Had to go back because I forgot the diodes though.

Here's what the schematic looks like(after I added the diodes):

![Schematic](https://hc-cdn.hel1.your-objectstorage.com/s/v3/b4f662f5a937066d842f1df2b81d933781cc0f1c_cleanshot_2025-06-01_at_14.40.17.png)

### Jun 1: 9 hrs 38 min
Did all the organizing, layouts, and wiring today! PCB is now fully finished, and it looks good. I added a snowflake icon since it's called Frost. It's looking amazing! Took a long time and looks a bit messy though because the schematic and pcb wiring diagram differ a bit - 9x9 vs 6x15. Also added stab holes and case attatchment holes. I used over 200 vias and over 1100 track segments!

Here are some images of the process and final renders:

![PCB](https://hc-cdn.hel1.your-objectstorage.com/s/v3/e52fe4e04f64aef6a7810594c349aeeb419c2bca_cleanshot_2025-06-01_at_14.43.55.png)
![PCB](https://hc-cdn.hel1.your-objectstorage.com/s/v3/8e2605a99a3ffef96b647e3e74ac65c6e4645698_cleanshot_2025-06-01_at_14.49.07.png)
![PCB 3D View](https://hc-cdn.hel1.your-objectstorage.com/s/v3/7472dd4400217b645455c171a07442d5b0f28683_cleanshot_2025-06-01_at_14.50.39.png)
![PCB JLCPCB Render](https://hc-cdn.hel1.your-objectstorage.com/s/v3/d1286d84882b28505fd7c4d1f33979fc95306325_cleanshot_2025-06-01_at_14.53.43.png)

### Jun 2: 7 hrs 19 min

Made my ZMK code but stuck on an issue in GH Actions where it says it can't find my shield. Made a new repo for my zmk code though - frost-module as per the zmk docs.

Took a LONG time to learn ZMK. There are very few tutorials and explanations online, and the docs are somewhat unclear and they contradict themselves a bit too.

### Jun 3: 2 hrs 4 min

Worked on that error. Asked online but the people's suggestions didn't work very well. Also asked Gemini but it hallucinated a LOT.

### Jun 4: 8 hrs 9 min

Someone else responded to my discord post in scottokeebs server, and pointed out an error in my module.yml where I put ```board_root: ..``` instead of ```board_root: .```

Then I worked on other errors, since there were lots of issues with my overlay and keymap.

Eventually, and with a bit of help from Claude Sonnet 4, I managed to produce a working copy of the firmware! It's available in /firmware - both the .uf2 and the full uncompiled version.

Also started the case in Fusion 360 - it's going to be a very simple design since I want the pcb fully exposed. That way the signal strength from the nice!nano isn't impacted at all.