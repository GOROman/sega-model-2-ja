# Sega Model 2 — English source reference

Original author: Sega Retro contributors.

Source: [Sega Model 2](https://segaretro.org/Sega_Model_2). [Revision 1149915](https://segaretro.org/index.php?title=Sega_Model_2&oldid=1149915). [Contributor history](https://segaretro.org/index.php?title=Sega_Model_2&action=history).

License: [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). Extracted 2026-10-14.

Editorial notice: Original English wording and technical values are preserved; headings, lists, and references are reformatted as Markdown. Navigation, an empty release-information table, photographs, logos, and scans are omitted. Photo captions are retained. This is an attributed reproduction, not an independently verified specification. Possible errors must be discussed separately rather than silently changing this reference. Linked third-party materials retain their own rights.

## Basic information

- Sega Model 2
- Manufacturer: Sega Enterprises, Ltd.
- Variants: Model 2A-CRX, Model 2B-CRX, Model 2C-CRX
- Add-ons: DSB1/DSB2 (Model 2C-CRX)

The Sega Model 2 (モデル2) is an arcade system board originally debuted by Sega in 1993 as a successor to the Sega Model 1 board. It is an extension of the Model 1 hardware, most notably introducing the concept of texture-mapped polygons, allowing for more realistic 3D graphics for its time.

The Model 2 board was an important milestone for the arcade industry, and helped launch several key arcade franchises of the 1990s, including Daytona USA, Virtua Cop, Sega Rally Championship, Dead or Alive, Virtua Striker, Cyber Troopers Virtual-On and The House of the Dead. It was succeeded by the Sega Model 3 in 1996.


## Hardware


The Model 2 was designed as the direct successor to the Model 1, and like its predecessor was released as a set of printed circuit boards to arcade operators, or packaged in bespoke cabinets created by Sega. It came into existence when General Electric approached Sega with some real-time texture mapping ASICs, which led to a commercial partnership in August 1992[[3]](#ref-3). The board took about a year to produce[[3]](#ref-3).

The most noticeable improvement of the Model 2 over the Model 1 is texture mapping, which enables polygons to be painted with bitmap images, as opposed to the limited monotone flat shading that the previous board supported. The Model 2 also introduced the use of texture filtering and texture anti-aliasing,[[4]](#ref-4) as well as trilinear filtering.[[2]](#ref-2) It can handle 500,000 textured polygons per second,[[5]](#ref-5) or 300,000 polygons per second[[3]](#ref-3) with all hardware effects[[6]](#ref-6) including trilinear filtering.[[2]](#ref-2) It was the most powerful game system in its time, equivalent to the power of a PC graphics card in 1998, five years after the Model 2's release.[[2]](#ref-2)

There are, in fact, four versions of the system: the original Model 2, and the Model 2A-CRX, Model 2B-CRX and Model 2C-CRX variants. The Model 2 and 2A-CRX use a custom DSP with internal code for the geometrizer, while 2B-CRX and 2C-CRX use well documented DSPs and upload the geometrizer code at startup to the DSP.

According to Yu Suzuki, the Sega Model 2B-CRX arcade system board developed for Fighting Vipers "has a slightly faster processing speed" and "a higher response to displaying more polygons".[[7]](#ref-7)


## Technical specifications


### Model 2

- Board composition: CPU Board, Video Board, Communication Board, ROM Board, Sound Board, Feedback Driver Board[[8]](#ref-8)
- Revisions: CPU Board 837-10071 (50 MHz), Video Board 837-10072 (50 MHz), Communication Board 837-10537, ROM Board 834-10798, Sound Board 837-8679 (20 MHz), Drive Board 838-10646[[9]](#ref-9)
- Main CPU: Intel i960-KB @ 25 MHz[[10]](#ref-10)[[11]](#ref-11)
- Fixed-point arithmetic: 32‑bit RISC instructions @ 25 MIPS[[12]](#ref-12)
- Floating-point unit: 32/64/80‑bit operations @ 13.6 MFLOPS[[11]](#ref-11)
- Bus width: 32‑bit
- Additional CPU: 2x Zilog Z80 (8/16‑bit instructions @ 1.74 MIPS)
- Communication Board: 8 MHz[[9]](#ref-9)[[13]](#ref-13) (1.16 MIPS)
- Feedback Driver: 4 MHz[[8]](#ref-8) (0.58 MIPS)

#### Sound

- Sound CPU: Motorola 68000 @ 10 MHz (16/32‑bit instructions @ 1.75 MIPS)
- Sound chip: 2x Sega 315‑5560 MultiPCM
- PCM channels: 56
- PCM sample ROM: Up to 16 MB (8 MB per PCM chip)
- PCM quality: 16‑bit depth, 44.1 kHz sampling rate (CD quality)[[14]](#ref-14)
- Sound timer: Yamaha YM3438 @ 8 MHz (Model 2 only)

#### Graphics


- Graphical specifications of the Sega Model 2:[[15]](#ref-15)[[8]](#ref-8)[[16]](#ref-16)

- GPU:
- 6x Fujitsu TGP MB86234
- Sega Video Board 837-10072
- GPU Geometry Engine DSP coprocessors: 6x Fujitsu TGP MB86234 @ 16 MHz[[17]](#ref-17)[[18]](#ref-18)[[9]](#ref-9)
- Revisions: 315‑5673, 315‑5677, 2x 315‑5678, 2x 315‑5679 (later updated with 2x 315‑5679B in 1994)
- Coprocessor abilities: Floating decimal point operation function, axis rotation operation function, 3D matrix operation function, ALU, DMA controllers, T&L (transform, clipping, lighting)[[19]](#ref-19)
- Instruction set: 32‑bit instructions, 480 MIPS (80 MIPS each)[[n 1]](#note-1)
- Fixed-point arithmetic: 192 MIPS (32 MIPS each)[[n 2]](#note-2)
- Floating-point units: 96 MFLOPS (16 MFLOPS each)[[n 3]](#note-3)
- Bus width: 192‑bit (32‑bit each)
- Notes: Located on CPU Board. DSP are modified by Sega with custom microcode for coprocessor and T&L capabilities.[[19]](#ref-19)
- GPU graphics card: Sega Video Board 837-10072 @ 50 MHz[[9]](#ref-9)[[21]](#ref-21)
- Sega Z-sorting & clipping chipset: 315‑5644 (32 MHz), 315‑5645 (32 MHz), 315‑5712 (40 MHz), 2x 315‑5725 (50 MHz)
- Lockheed Martin rasterization & texture mapping processors: 315‑5646 (50 MHz), 315‑5647 (50 MHz)
- Sega System 24 tilemap engine: 315‑5292 tilemap generator (32 MHz)[[22]](#ref-22)[[23]](#ref-23)
- Display: Up to 50-inch display[[24]](#ref-24)
- Display resolution: 496×384 pixels, 24 Hz HSync, progressive scan (non-interlaced), double-buffering[[15]](#ref-15)
- Overscan resolution: 656×496
- Pixel clock rate: 19.523 MHz
- Refresh rate: 60 Hz, 57.52416 Hz, 30 Hz[[15]](#ref-15)
- Frame rate: 60 FPS,[[25]](#ref-25) 57.52416 FPS, 30 FPS
- Color depth: 65,536 (16bpp), 16,777,216 (24bpp),[[5]](#ref-5) 256 (8bpp)
- Graphical hardware features: Flat shading, texture mapping, perspective correction, texture filtering, texture anti-aliasing, microtexture, diffuse reflection, specular reflection, specular lighting, alpha blending, transparency, rasterization, mipmapping, LOD,[[15]](#ref-15) Z-buffering, point sampling, bilinear filtering, trilinear filtering[[2]](#ref-2)
- Texture map resolution: Up to 1024×2048 pixels
- Microtexture size: Up to 128×128 pixels
- Arithmetic: 110 MFLOPS (floating-point), 210 MIPS (fixed-point)[[n 4]](#note-4)
- Additions: 61 million adds/sec (floating-point), 110 million adds/sec (fixed-point)[[n 5]](#note-5)
- Multiplications: 61 million multiplies/sec (floating-point), 110 million multiplies/sec (fixed-point)[[n 6]](#note-6)
- Divisions: 30 million divides/sec[[n 7]](#note-7)
- Geometry transformations: 6 million vertices/sec,[[n 8]](#note-8) 2 million polygons/sec[[n 9]](#note-9)
- Flat lighting: 1.2 million polygons/sec (floating-point),[[n 10]](#note-10) 2 million polygons/sec (fixed-point)[[n 11]](#note-11)
- Specular lighting: 900,000 polygons/sec[[n 12]](#note-12)
- Gouraud lighting: 880,000 polygons/sec (floating-point),[[n 13]](#note-13) 1.5 million polygons/sec (fixed-point)[[n 14]](#note-14)
- Rendering fillrate: 110 MPixels/s (16bpp), 230 MPixels/s (8bpp), 260 MPixels/s (4bpp)
- Polygons: 100 MPixels/s (16bpp), 200 MPixels/s (8bpp)[[n 15]](#note-15)
- Tilemaps: 15 MPixels/s (16bpp), 30 MPixels/s (8bpp), 61 MPixels/s (4bpp)[[n 16]](#note-16)
- Polygon rendering performance: 100 MPixels/s, 900,000 vectors/sec
- Texture mapping performance: 100 MTexels/s, lighting
- 900,000 polygons/sec: Specular, 100-texel polygons
- 500,000 polygons/sec:[[5]](#ref-5) Specular, 200-texel polygons
- 300,000 polygons/sec: All hardware effects,[[6]](#ref-6) trilinear filtering,[[2]](#ref-2) specular, 300-texel polygons
- 300,000 polygons/sec: Gouraud shading (software), 32-texel polygons[[n 17]](#note-17)
- Hardware support: Motion capture

#### Memory

- Memory: Up to 62 MB (10,881 KB main, 35,460 KB video, 16,960 KB audio, 18 KB other)
- System RAM: 9776 KB (9.546875 MB)[[15]](#ref-15)
- Main RAM: 1152 KB (1.125 MB)
- VRAM: 5984 KB (1 MB framebuffer VRAM, 64 KB coprocessor buffer SRAM/SDRAM, 4 MB texture SRAM/SDRAM, 128 KB luma, 32 KB geometry, 576 KB tiles, 64 KB colors)
- Audio RAM: 576 KB
- Other RAM: 2064 KB (16 KB backup SRAM/NVRAM, 2 MB extra RAM)
- Internal processor cache: 36.75 KB
- CPU cache: 768 bytes[[10]](#ref-10)
- TGP internal RAM cache: 36 KB (6 KB per TGP)[[18]](#ref-18)
- Game ROM: Up to 54.25 MB
- Main ROM: 9.5 MB (EPROM, MROM)
- Video ROM: 28.75 MB (MROM)
- Audio ROM: 16 MB (MROM)

#### Bandwidth

- System RAM bandwidth: 982 MB/s
- Main RAM bandwidth: 78.7 MB/s
- i960: 66.7 MB/s[[30]](#ref-30)
- Z80: 12 MB/s[[n 18]](#note-18)
- VRAM bandwidth: 883.34066 MB/s[[9]](#ref-9)[[21]](#ref-21)
- TGP: 384 MB/s[[n 19]](#note-19)
- Video Board: 499.34066 MB/s
- 315‑5292 & 315‑5644: 30.769232 MB/s[[n 20]](#note-20)
- 315‑5645: 28.571428 MB/s[[n 21]](#note-21)
- 315‑5646 & 315‑5647: 400 MB/s[[n 22]](#note-22)
- 315‑5712: 40 MB/s[[n 23]](#note-23)
- Audio RAM bandwidth: 20 MB/s[[n 24]](#note-24)
- Internal processor cache bandwidth: 484 MB/s
- CPU cache: 100 MB/s[[n 25]](#note-25)
- TGP internal RAM cache: 384 MB/s[[n 26]](#note-26)
- Game ROM bandwidth: 933–1000 MB/s[[n 27]](#note-27)[[9]](#ref-9)[[8]](#ref-8)
- EPROM: 133–200 MB/s[[n 28]](#note-28)
- MROM: 800 MB/s[[n 29]](#note-29)

### Model 2A-CRX


- Model 2A-CRX, released in 1994, featured upgraded sound capabilities and increased ROM capacity:

- Sound CPU: Motorola 68000 @ 12 MHz (16/32‑bit instructions @ 2.1 MIPS)
- Sound chip: Yamaha SCSP
- PCM channels: 32
- PCM sample ROM: Up to 16 MB
- PCM quality: 16‑bit depth, 44.1 kHz sampling rate (CD quality)
- SCSP features: 128-step DSP, 32 PCM/FM/MIDI/LFO channels
- Memory: Up to 142 MB (35,969 KB main, 90,244 KB video, 16,960 KB audio, 2064 KB other)
- System RAM: 9776 KB (9.546875 MB)
- Main RAM: 1152 KB (1.125 MB)
- VRAM: 5984 KB (5.84375 MB)
- Audio RAM: 576 KB
- Other RAM: 2064 KB (2.015625 MB)
- Internal processor cache: 36.75 KB
- CPU cache: 768 bytes
- TGP internal RAM cache: 36 KB
- Game ROM: Up to 132.25 MB (34 MB main, 82.25 MB video,[[37]](#ref-37) 16 MB audio)

### Model 2B-CRX


- Model 2B-CRX, released in 1995, featured upgraded geometry engine DSP coprocessors and increased VRAM:[[15]](#ref-15)

- GPU Geometry Engine DSP coprocessors: 2x ADSP-21062 SHARC @ 40 MHz[[38]](#ref-38)
- Coprocessor abilities: Floating decimal point operation function, axis rotation operation function, 3D matrix operation function, SOC, ALU, T&L
- Fixed-point instructions: 32‑bit instructions, 80 MIPS (40 MIPS each)
- Floating-point units: 32/40‑bit operations, 240 MFLOPS (120 MFLOPS each), 80 MAC operations/sec (40 MACs/sec each)
- Data bus width: 96‑bit (48‑bit each)
- DMA controllers: 20 DMA channels (10 channels each), 80 MHz memory access (dual memory access) per SHARC, 480 MB/s transfer rate (240 MB/s each)
- Lighting calculations: 240 MFLOPS
- Flat lighting: 1.8 million polygons/sec (floating-point)[[n 30]](#note-30)
- Specular lighting: 1.5 million polygons/sec[[n 31]](#note-31)
- Gouraud lighting: 1.3 million polygons/sec (floating-point)[[n 32]](#note-32)
- Rendering fillrate: 130 MPixels/s (16bpp), 270 MPixels/s (8bpp), 300 MPixels/s (4bpp)
- Polygons: 120 MPixels/s (16bpp),[[n 33]](#note-33) 240 MPixels/s (8bpp)
- Tilemaps: 15 MPixels/s (16bpp), 30 MPixels/s (8bpp), 61 MPixels/s (4bpp)
- Texture mapping performance: 120 MTexels/s, lighting
- 900,000 polygons/sec: Specular, 130-texel polygons
- 600,000 polygons/sec: Specular, 200-texel polygons
- 300,000 polygons/sec: Gouraud shading (software), 32-texel polygons[[n 34]](#note-34)
- Memory: Up to 150.21 MB (35.125 MB main, 99,332 KB video, 16,960 KB audio, 18 KB other)
- System RAM: 18,388 KB (17.957031 MB)[[8]](#ref-8)
- Main RAM: 1152 KB (1.125 MB)
- VRAM: 14,596 KB (1.5 MB framebuffer VRAM, 8228 KB coprocessor buffer SRAM/SDRAM, 4 MB texture SRAM/SDRAM, 64 KB luma, 32 KB geometry, 576 KB tiles, 64 KB colors)
- Audio RAM: 576 KB
- Other RAM: 2064 KB (2.015625 MB)
- Internal processor cache: 512.75 KB
- CPU cache: 768 bytes
- DSP internal RAM cache: 512 KB SRAM (256 KB per DSP)[[38]](#ref-38)
- Game ROM: Up to 132.25 MB (34 MB main, 82.25 MB video, 16 MB audio)
- System RAM bandwidth: 1.1 GB/s
- Main RAM bandwidth: 112 MB/s
- VRAM bandwidth: 979.34066 MB/s
- SHARC: 480 MB/s (2x 240 MB/s)[[39]](#ref-39)
- Video Board: 499.34066 MB/s
- Audio RAM bandwidth: 20 MB/s

### Model 2C-CRX


- Model 2C-CRX, released in 1996, featured an upgraded GPU chipset and optional MPEG sound boards:

- GPU geometry coprocessors: 2x Fujitsu TGPx4 MB86235 @ 40 MHz[[15]](#ref-15)[[40]](#ref-40)
- Coprocessor capabilities: Geometry Engine DSP, floating decimal point operation function, axis rotation operation function, 3D matrix operation function, ALU, DMA, T&L
- Bus width: 192‑bit (96‑bit each; 64‑bit SDRAM, 32‑bit SRAM)
- GPU rendering processors: 2x Fujitsu MB86271 AGP (Advanced Graphics Processor) @ 60 MHz[[41]](#ref-41)
- Capabilities: Hardware rendering, DMA
- Fixed-point arithmetic: 32/64‑bit instructions, 240 MIPS (120 MIPS each)
- GPU Z-sorters: 2x Fujitsu MB86272[[41]](#ref-41)
- Capabilities: Z-sorting, clipping
- Graphical hardware features: Gouraud shading, hidden surface, Z-buffering, point sampling, bilinear filtering, trilinear filtering[[42]](#ref-42)
- Rendering fillrate: 200 MPixels/s (16bpp), 400 MPixels/s (8bpp), 430 MPixels/s (4bpp)
- Polygons: 188 MPixels/s (16bpp),[[n 35]](#note-35) 376 MPixels/s (8bpp)
- Tilemaps: 15 MPixels/s (16bpp), 30 MPixels/s (8bpp), 61 MPixels/s (4bpp)
- Texture mapping performance: 188 MTexels/s, lighting, specular,[[15]](#ref-15) alpha blending[[40]](#ref-40)
- 900,000 polygons/sec: 150-texel polygons[[n 36]](#note-36)
- 600,000 polygons/sec: Z-sorting,[[n 37]](#note-37) 400-texel polygons
- 520,000 polygons/sec: Gouraud shading,[[n 38]](#note-38) 150-texel polygons[[n 39]](#note-39)
- 360,000 polygons/sec: Gouraud shading, Z-sorting,[[n 40]](#note-40) 300-texel polygons
- Optional MPEG sound board: DSB1
- Sound CPU: Zilog Z80 (8/16‑bit instructions)
- Sound chip: NEC µD65654GF102
- Optional MPEG sound board: DSB2
- Sound CPU: Motorola 68000 (16/32‑bit instructions)
- Sound chip: NEC µD65654GF102

## List of games


### Model 2

- Daytona USA (1993)
- Daytona USA Deluxe '93 (1993)
- Desert Tank (1994)
- Virtua Cop (1994)

### Model 2A-CRX

- Virtua Fighter 2 (1994)
- Manx TT Superbike (1995)
- Sega Rally Championship (1995)
- Sky Target (1995)
- Virtua Cop 2 (1995)
- Dead or Alive (1996)
- Dynamite Cop (1996)
- Virtua Fighter 2.1 (1996)
- Motor Raid (1997)
- Zero Gunner (1997)
- Hanguk Pro Yagu 98 (1998)
- Pilot Kids (1999)
- Air Walkers (unreleased)

### Model 2B-CRX

- Fighting Vipers (1995)
- Gunblade NY (1995)
- Indy 500 (1995)
- Rail Chase 2 (1995)
- Virtua Striker (1995)
- Dead or Alive (1996)
- Dynamite Baseball (1996)
- Dynamite Cop (1996)
- Last Bronx (1996)
- Pilot Kids (1999)
- Sonic the Fighters (1996)
- Super GT 24H (1996)
- Cyber Troopers Virtual-On (1996)
- Dynamite Baseball 97 (1997)
- Zero Gunner (1997)

### Model 2C-CRX

- Dynamite Cop (1996)
- Over Rev (1997)
- Power Sled (1996)
- Sega Ski Super G (1996)
- Sega Touring Car Championship (1996)
- Sega Water Ski (1996)
- Wave Runner (1996)
- The House of the Dead (1997)
- Top Skater (1997)
- Behind Enemy Lines (1998)

### Other

- Ultimate Domain (unreleased) - Developed by Atlus. Previewed in Mean Machines Sega #51.

## History


The Model 2's development was led by famed game designer Yu Suzuki and his team at Sega AM2[[46]](#ref-46) as part of a joint project between Sega, Fujitsu and GE Aerospace (acquired by Martin Marietta in 1993, now part of Lockheed Martin). Sega developed the polygon geometry engine in-house[[16]](#ref-16), using Fujitsu coprocessors DSP coprocessors that were modified with Sega's custom microcode for hardware T&L capabilities[[19]](#ref-19) (it would be years before hardware T&L would appear on consumer home systems). This was then combined with GE Aerospace's expensive texture-mapping technology,[[16]](#ref-16) which Suzuki's team condensed into a more affordable chipset.

Suzuki stated that the Model 2's texture mapping chip originated "from military equipment from Lockheed Martin, which was formerly General Electric Aerial & Space's textural mapping technology. It cost $2 million USD to use the chip. It was part of flight-simulation equipment that cost $32 million. I asked how much it would cost to buy just the chip and they came back with $2 million. And I had to take that chip and convert it for video game use, and make the technology available for the consumer at 5,000 yen ($50)" per machine. He said "it was tough but we were able to make it for 5,000 yen. Nobody at Sega believed me when I said I wanted to purchase this technology for our games."[[46]](#ref-46) Suzuki stated that, in "the end," it "was a hit and the industry gained mass-produced texture-mapping as a result." For Virtua Fighter 2, he also utilized motion capture technology, introducing it to the game industry.[[47]](#ref-47)

There were also issues working on the new CPU,[[46]](#ref-46) the Intel i960-KB, which had just released in 1993[[11]](#ref-11). Suzuki stated that when working "on a brand new CPU, the debugger doesn't exist yet. The latest hardware doesn't work because it's full of bugs. And even if a debugger exists, the debugger itself is full of bugs. So, I had to debug the debugger. And of course with new hardware there's no library or system, so I had to create all of that, as well. It was a brutal cycle."[[46]](#ref-46)

In a late 1998 interview, Read3D's Jon Lenyo, a former employee of GE Aerospace (later Lockheed Martin), stated that Sega's development for the Model 2 can be traced back as early as November 1990, when he and other GE Aerospace employees visited Sega and demonstrated the trilinear texture filtering and shading capabilities of their technology. As Sega was already working on the Sega Model 1 internally, they eventually incorporated GE Aerospace's technology into the Model 2.[[2]](#ref-2)

The arcade board debuted along with Daytona USA, a game which was finished and copyrighted in 1993, and debuted at the Amusement Machine Show 1993[[48]](#ref-48).

Despite its high price tag of around $15,000 (equivalent to $25,000 in 2014), the Model 2 platform was very successful. It featured some of the highest grossing arcade games of all time, including Daytona USA, Virtua Fighter 2, Cyber Troopers Virtual-On, The House of the Dead, and Dead or Alive, to name a few. Sega sold over 33,000 units of the Model 2 in its first year,[[49]](#ref-49) followed by 65,000 units annually,[[2]](#ref-2) and eventually sold over 130,000 units by 1996, amounting to $2 billion revenue from hardware cabinet sales[[n 41]](#note-41) (over $3 billion with inflation), making it one of the best-selling arcade systems of all time.

The Model 2 was succeeded in 1996 by the Sega Model 3, which in turn was succeeded by the Sega NAOMI, Sega Hikaru and Sega NAOMI 2.


## Production credits

Hiroshi Yagi[[52]](#ref-52)
3D Previewing Software: Kenneth Ibrahim[[53]](#ref-53)
Source:
Developer mentions





## Magazine articles

Main article: Sega Model 2/Magazine articles.

## Photo gallery


CPU



Video PCB



A typical ROM (Virtua Cop)



Model 2A CPU



Model 2A video PCB



Model 2A ROM (Dead or Alive)



Model 2B CPU/Video PCB



Model 2B filter PCB



Model 2B communications PCB



A Model 2B ROM



Model 2C PCB



Official Sega of Japan photograph of the Model 2B CRX

## Notes

<a id="note-1"></a>

[n 1] 5 instructions per cycle[[20]](#ref-20)


<a id="note-2"></a>

[n 2] MAC (multiply–accumulate) operation (multiply and add) per cycle[[20]](#ref-20)


<a id="note-3"></a>

[n 3] 1 operation per cycle (2 cycles per MAC operation)[[20]](#ref-20)


<a id="note-4"></a>

[n 4] TGP: 96 MFLOPS, 192 MIPS[[18]](#ref-18)
i960: 13.6 MFLOPS, 25 MIPS[[11]](#ref-11)


<a id="note-5"></a>

[n 5] TGP: 48 million adds/sec (floating-point), 96 million adds/sec (fixed-point)[[26]](#ref-26)
i960: 13.6 million adds/sec (floating-point), 25 million adds/sec (fixed-point)


<a id="note-6"></a>

[n 6] TGP: 48 million multiplies/sec (floating-point), 96 million multiplies/sec (fixed-point)[[26]](#ref-26)
i960: 13.6 million multiplies/sec (floating-point), 25 million multiplies/sec (fixed-point)


<a id="note-7"></a>

[n 7] Z-sorting & clipping chipset, 32 MHz


<a id="note-8"></a>

[n 8] TGP: 5,333,333 vertices/sec, 18 cycles (9 MAC operations) per vertex[[15]](#ref-15)
i960: 755,555 vertices/sec, 18 floating-point operations (9 MAC operations) per vertex


<a id="note-9"></a>

[n 9] 3 vertices per triangle polygon


<a id="note-10"></a>

[n 10] TGP: 1,043,478 polygons/sec, 92 cycles (46 MAC operations) per polygon[[15]](#ref-15)
i960: 147,826 polygons/sec, 92 floating-point operations (46 MAC operations) per polygon


<a id="note-11"></a>

[n 11] 46 cycles (46 MAC operations) per polygon[[15]](#ref-15)


<a id="note-12"></a>

[n 12] 102 cycles (51 MAC operations) per polygon[[15]](#ref-15)


<a id="note-13"></a>

[n 13] TGP: 774,193 polygons/sec, 124 cycles (62 MAC operations) per polygon[[15]](#ref-15)[[27]](#ref-27)
i960: 109,677 polygons/sec, 124 floating-point operations (62 MAC operations) per polygon


<a id="note-14"></a>

[n 14] 62 cycles (62 MAC operations) per polygon[[15]](#ref-15)[[27]](#ref-27)


<a id="note-15"></a>

[n 15] 400 MB/s polygon rendering bandwidth (2x 32‑bit, 50 MHz)


<a id="note-16"></a>

[n 16] 30.769232 MB/s tilemap generator bandwidth (2x 16‑bit, 7.692308 MHz)


<a id="note-17"></a>

[n 17] 163 cycles (124 cycles geometry, 39 raster operations) per polygon, 175 cycles per 4-scanline polygon (3 operations/scanline per polygon),[[28]](#ref-28)[[29]](#ref-29) 271 cycles per 32-pixel polygon (3 cycles per pixel)


<a id="note-18"></a>

[n 18] 2x 8‑bit, 8/4 MHz


<a id="note-19"></a>

[n 19] 6x 32‑bit, 16 MHz[[31]](#ref-31)


<a id="note-20"></a>

[n 20] 2x 16‑bit, 7.692308 MHz[[32]](#ref-32)


<a id="note-21"></a>

[n 21] 16‑bit, 14.285714 MHz[[33]](#ref-33)


<a id="note-22"></a>

[n 22] 2x 32‑bit, 50 MHz


<a id="note-23"></a>

[n 23] 8‑bit, 40 MHz[[34]](#ref-34)


<a id="note-24"></a>

[n 24] 16‑bit, 10 MHz


<a id="note-25"></a>

[n 25] 32‑bit, 25 MHz


<a id="note-26"></a>

[n 26] 6x 32‑bit, 16 MHz


<a id="note-27"></a>

[n 27] 5x 32‑bit


<a id="note-28"></a>

[n 28] 32‑bit, 33–50 MHz, 20–30 ns[[35]](#ref-35)[[36]](#ref-36)


<a id="note-29"></a>

[n 29] 4x 32‑bit, 50 MHz


<a id="note-30"></a>

[n 30] 46 MAC operations per polygon:[[15]](#ref-15) 1,739,130 polygons/sec (SHARC), 147,826 polygons/sec (i960)


<a id="note-31"></a>

[n 31] 51 MAC operations per polygon[[15]](#ref-15)


<a id="note-32"></a>

[n 32] 62 MAC operations per polygon:[[15]](#ref-15)[[27]](#ref-27) 1,290,322 polygons/sec (SHARC), 109,677 polygons/sec (i960)


<a id="note-33"></a>

[n 33] 2 megapixels per frame


<a id="note-34"></a>

[n 34] 101 cycles (62 cycles geometry, 39 raster operations) per polygon, 113 cycles per 4-scanline polygon (3 operations/scanline per polygon),[[28]](#ref-28)[[29]](#ref-29) 209 cycles per 32-pixel polygon (3 cycles per pixel)


<a id="note-35"></a>

[n 35] 94 megapixels/sec per GPU[[43]](#ref-43)


<a id="note-36"></a>

[n 36] 88 cycles per polygon,[[44]](#ref-44) 266 fixed-point instructions per polygon, 450,000 150-pixel polygons/sec per GPU[[45]](#ref-45)


<a id="note-37"></a>

[n 37] 272 floating-point operations per polygon


<a id="note-38"></a>

[n 38] 151 cycles per polygon[[44]](#ref-44)


<a id="note-39"></a>

[n 39] 250,000 150-pixel polygons/sec per GPU[[45]](#ref-45)


<a id="note-40"></a>

[n 40] 438 floating-point operations per polygon


<a id="note-41"></a>

[n 41] 130,000 units[[50]](#ref-50) at $15,000 each[[2]](#ref-2)[[51]](#ref-51)



## References

<a id="ref-1"></a>

[1] Mean Machines Sega, "August 1994" (UK; 1994-06-30), page 93
Sources: [Mean Machines Sega](https://segaretro.org/Mean_Machines_Sega) · ["August 1994" (UK; 1994-06-30), page 93](https://segaretro.org/index.php?title=File:MeanMachinesSega22UK.pdf&page=93)

<a id="ref-2"></a>

[2] Second Hand Smoke: One up, two down (October 22, 1999)
Sources: [Second Hand Smoke: One up, two down (October 22, 1999)](http://www.thg.ru/smoke/19991022/print.html)

<a id="ref-3"></a>

[3] Edge, "June 1994" (UK; 1994-04-28), page 49
Sources: [Edge](https://segaretro.org/Edge) · ["June 1994" (UK; 1994-04-28), page 49](https://segaretro.org/index.php?title=File:Edge_UK_009.pdf&page=49)

<a id="ref-4"></a>

[4] IGN PRESENTS THE HISTORY OF SEGA (page 8)
Sources: [IGN PRESENTS THE HISTORY OF SEGA (page 8)](http://ign.com/articles/2009/04/21/ign-presents-the-history-of-sega?page=8)

<a id="ref-5"></a>

[5] Saturn maybe not so stellar (Game Zero Magazine)
Sources: [Saturn maybe not so stellar (Game Zero Magazine)](http://www.gamezero.com/team-0/whats_new/past/news9504.html)

<a id="ref-6"></a>

[6] File:DaytonaUSA Model2 Flyer.pdf, page 2
Sources: [File:DaytonaUSA Model2 Flyer.pdf, page 2](https://segaretro.org/index.php?title=File:DaytonaUSA_Model2_Flyer.pdf&page=2)

<a id="ref-7"></a>

[7] File:SSM_UK_02.pdf, page 21
Sources: [File:SSM_UK_02.pdf, page 21](https://segaretro.org/index.php?title=File:SSM_UK_02.pdf&page=21)

<a id="ref-8"></a>

[8] Sega Model 2 (MAME)
Sources: [Sega Model 2 (MAME)](https://github.com/mamedev/mame/blob/master/src/mame/drivers/model2.cpp)

<a id="ref-9"></a>

[9] Sega PCB
Sources: [Sega PCB](http://www.tvspels-nostalgi.com/pcb_sega.htm)

<a id="ref-10"></a>

[10] File:I960 datasheet.pdf
Sources: [File:I960 datasheet.pdf](https://segaretro.org/File:I960_datasheet.pdf)

<a id="ref-11"></a>

[11] File:80960KB datasheet.pdf
Sources: [File:80960KB datasheet.pdf](https://segaretro.org/File:80960KB_datasheet.pdf)

<a id="ref-12"></a>

[12] File:I960 datasheet.pdf, page 2
Sources: [File:I960 datasheet.pdf, page 2](https://segaretro.org/index.php?title=File:I960_datasheet.pdf&page=2)

<a id="ref-13"></a>

[13] http://pdf.datasheetarchive.com/indexerfiles/Scans-068/DSA2IH00225160.pdf
Sources: [http://pdf.datasheetarchive.com/indexerfiles/Scans-068/DSA2IH00225160.pdf](http://pdf.datasheetarchive.com/indexerfiles/Scans-068/DSA2IH00225160.pdf)

<a id="ref-14"></a>

[14] File:ST-077-R2-052594.pdf
Sources: [File:ST-077-R2-052594.pdf](https://segaretro.org/File:ST-077-R2-052594.pdf)

<a id="ref-15"></a>

[15] Sega Model 2 Geometry Engine and 3D Rasterizer (MAME)
Sources: [Sega Model 2 Geometry Engine and 3D Rasterizer (MAME)](https://github.com/mamedev/mame/blob/master/src/mame/video/model2.cpp)

<a id="ref-16"></a>

[16] Next Generation, "November 1995" (US; 1995-10-24), page 16
Sources: [Next Generation](https://segaretro.org/Next_Generation) · ["November 1995" (US; 1995-10-24), page 16](https://segaretro.org/index.php?title=File:NextGeneration_US_11.pdf&page=16)

<a id="ref-17"></a>

[17] Sega Model 2 ROM Dump
Sources: [Sega Model 2 ROM Dump](http://members.iinet.net.au/~lantra9jp1_nbn/gurudumps/m2status/index.html)

<a id="ref-18"></a>

[18] File:MB86232 datasheet.pdf
Sources: [File:MB86232 datasheet.pdf](https://segaretro.org/File:MB86232_datasheet.pdf)

<a id="ref-19"></a>

[19] TGP (MAME)
Sources: [TGP (MAME)](http://wiki.mamedev.org/index.php/TGP:Index)

<a id="ref-20"></a>

[20] File:MB86232 datasheet.pdf, page 32
Sources: [File:MB86232 datasheet.pdf, page 32](https://segaretro.org/index.php?title=File:MB86232_datasheet.pdf&page=32)

<a id="ref-21"></a>

[21] Sega Model 2 Video Board
Sources: [Sega Model 2 Video Board](http://hico-srv004.pixhotel.fr/sites/default/files/gamoovernet/20110520120039-lapin252-IMG-0112.JPG)

<a id="ref-22"></a>

[22] Sega 16‑Bit Common Hardware, MAME
Sources: [Sega 16‑Bit Common Hardware](https://github.com/bji/libmame/blob/master/old/src/mame/video/segaic16.c) · [MAME](https://segaretro.org/MAME)

<a id="ref-23"></a>

[23] Sega System 24 Hardware Notes (2013-06-16)
Sources: [Sega System 24 Hardware Notes (2013-06-16)](https://segaretro.org/Sega_System_24_Hardware_Notes_(2013-06-16))

<a id="ref-24"></a>

[24] Electronic Gaming Monthly, "June 1994" (US; 1994-xx-xx), page 68
Sources: [Electronic Gaming Monthly](https://segaretro.org/Electronic_Gaming_Monthly) · ["June 1994" (US; 1994-xx-xx), page 68](https://segaretro.org/index.php?title=File:EGM_US_059.pdf&page=68)

<a id="ref-25"></a>

[25] File:VirtuaFighter2 Model2 Flyer.pdf, page 2
Sources: [File:VirtuaFighter2 Model2 Flyer.pdf, page 2](https://segaretro.org/index.php?title=File:VirtuaFighter2_Model2_Flyer.pdf&page=2)

<a id="ref-26"></a>

[26] File:MB86232 datasheet.pdf, page 33
Sources: [File:MB86232 datasheet.pdf, page 33](https://segaretro.org/index.php?title=File:MB86232_datasheet.pdf&page=33)

<a id="ref-27"></a>

[27] Design of Digital Systems and Devices (pages 95-97)
Sources: [Design of Digital Systems and Devices (pages 95-97)](https://books.google.co.uk/books?id=iAvHt5RCHbMC&pg=PA95)

<a id="ref-28"></a>

[28] Transformation Of Rendering Algorithms For Hardware Implementation (page 53)
Sources: [Transformation Of Rendering Algorithms For Hardware Implementation (page 53)](http://sirkan.iit.bme.hu/~szirmay/abbas.pdf#page=53)

<a id="ref-29"></a>

[29] File:32XUSHardwareManual.pdf, page 76
Sources: [File:32XUSHardwareManual.pdf, page 76](https://segaretro.org/index.php?title=File:32XUSHardwareManual.pdf&page=76)

<a id="ref-30"></a>

[30] File:80960KB datasheet.pdf, page 7
Sources: [File:80960KB datasheet.pdf, page 7](https://segaretro.org/index.php?title=File:80960KB_datasheet.pdf&page=7)

<a id="ref-31"></a>

[31] File:TC5588P datasheet.pdf
Sources: [File:TC5588P datasheet.pdf](https://segaretro.org/File:TC5588P_datasheet.pdf)

<a id="ref-32"></a>

[32] File:TC518128CPL datasheet.pdf
Sources: [File:TC518128CPL datasheet.pdf](https://segaretro.org/File:TC518128CPL_datasheet.pdf)

<a id="ref-33"></a>

[33] File:MB84256A datasheet.pdf
Sources: [File:MB84256A datasheet.pdf](https://segaretro.org/File:MB84256A_datasheet.pdf)

<a id="ref-34"></a>

[34] http://pdf.datasheetarchive.com/datasheetsmain/Datasheets-39/DSA-764435.pdf
Sources: [http://pdf.datasheetarchive.com/datasheetsmain/Datasheets-39/DSA-764435.pdf](http://pdf.datasheetarchive.com/datasheetsmain/Datasheets-39/DSA-764435.pdf)

<a id="ref-35"></a>

[35] File:AM27C1024 datasheet.pdf
Sources: [File:AM27C1024 datasheet.pdf](https://segaretro.org/File:AM27C1024_datasheet.pdf)

<a id="ref-36"></a>

[36] File:MX27C1024 datasheet.pdf
Sources: [File:MX27C1024 datasheet.pdf](https://segaretro.org/File:MX27C1024_datasheet.pdf)

<a id="ref-37"></a>

[37] Dynamite Cop (MAME)
Sources: [Dynamite Cop (MAME)](http://mamedb.blu-ferret.co.uk/game/dynamcop)

<a id="ref-38"></a>

[38] File:ADSP-2106 datasheet.pdf
Sources: [File:ADSP-2106 datasheet.pdf](https://segaretro.org/File:ADSP-2106_datasheet.pdf)

<a id="ref-39"></a>

[39] File:ADSP-2106 datasheet.pdf, page 4
Sources: [File:ADSP-2106 datasheet.pdf, page 4](https://segaretro.org/index.php?title=File:ADSP-2106_datasheet.pdf&page=4)

<a id="ref-40"></a>

[40] File:3DGraphicsProcessorChipSet.pdf
Sources: [File:3DGraphicsProcessorChipSet.pdf](https://segaretro.org/File:3DGraphicsProcessorChipSet.pdf)

<a id="ref-41"></a>

[41] File:3DGraphicsProcessorChipSet.pdf, page 4
Sources: [File:3DGraphicsProcessorChipSet.pdf, page 4](https://segaretro.org/index.php?title=File:3DGraphicsProcessorChipSet.pdf&page=4)

<a id="ref-42"></a>

[42] File:3D-CG System with Video Texturing.pdf
Sources: [File:3D-CG System with Video Texturing.pdf](https://segaretro.org/File:3D-CG_System_with_Video_Texturing.pdf)

<a id="ref-43"></a>

[43] File:3DGraphicsProcessorChipSet.pdf, page 12
Sources: [File:3DGraphicsProcessorChipSet.pdf, page 12](https://segaretro.org/index.php?title=File:3DGraphicsProcessorChipSet.pdf&page=12)

<a id="ref-44"></a>

[44] File:3DGraphicsProcessorChipSet.pdf, page 8
Sources: [File:3DGraphicsProcessorChipSet.pdf, page 8](https://segaretro.org/index.php?title=File:3DGraphicsProcessorChipSet.pdf&page=8)

<a id="ref-45"></a>

[45] File:3DGraphicsProcessorChipSet.pdf, page 11
Sources: [File:3DGraphicsProcessorChipSet.pdf, page 11](https://segaretro.org/index.php?title=File:3DGraphicsProcessorChipSet.pdf&page=11)

<a id="ref-46"></a>

[46] http://www.1up.com/features/disappearance-suzuki-part-1 (archive.today)
Sources: [http://www.1up.com/features/disappearance-suzuki-part-1](http://archive.is/35o4a)

<a id="ref-47"></a>

[47] Yu Suzuki recalls using military tech to make Virtua Fighter 2
Sources: [Yu Suzuki recalls using military tech to make Virtua Fighter 2](http://www.gamasutra.com/view/news/228512/Yu_Suzuki_recalls_using_military_tech_to_make_Virtua_Fighter_2.php)

<a id="ref-48"></a>

[48] Electronic Gaming Monthly, "October 1993" (US; 1993-xx-xx), page 222
Sources: [Electronic Gaming Monthly](https://segaretro.org/Electronic_Gaming_Monthly) · ["October 1993" (US; 1993-xx-xx), page 222](https://segaretro.org/index.php?title=File:EGM_US_051.pdf&page=222)

<a id="ref-49"></a>

[49] Press release: 1995-03-20: Lockheed Martin 3D Graphics Accelerator offers real-time PC visual system performance
Sources: [Press release: 1995-03-20: Lockheed Martin 3D Graphics Accelerator offers real-time PC visual system performance](https://segaretro.org/Press_release:_1995-03-20:_Lockheed_Martin_3D_Graphics_Accelerator_offers_real-time_PC_visual_system_performance)

<a id="ref-50"></a>

[50] http://www.real3d.com/sega.html (Wayback Machine: 1997-12-10 08:32)
Sources: [http://www.real3d.com/sega.html](http://web.archive.org/web/19971210083243/http://www.real3d.com/sega.html)

<a id="ref-51"></a>

[51] http://assemblergames.com/forums/showthread.php?47028-Early-concept-of-Daytona-USA-at-Summer-CES-1993-Not-on-Model-2-but-Compu-Scene (Wayback Machine: 2014-11-04 19:07)
Sources: [http://assemblergames.com/forums/showthread.php?47028-Early-concept-of-Daytona-USA-at-Summer-CES-1993-Not-on-Model-2-but-Compu-Scene](https://web.archive.org/web/20141104190719/http://assemblergames.com/forums/showthread.php?47028-Early-concept-of-Daytona-USA-at-Summer-CES-1993-Not-on-Model-2-but-Compu-Scene)

<a id="ref-52"></a>

[52] https://www.4gamer.net/games/999/G999905/20210126043/ (Wayback Machine: 2021-02-05 15:00)
Sources: [https://www.4gamer.net/games/999/G999905/20210126043/](https://web.archive.org/web/20210205150032/https://www.4gamer.net/games/999/G999905/20210126043/)

<a id="ref-53"></a>

[53] https://www.youtube.com/watch?v=1CEdmZ5P0jA
Sources: [https://www.youtube.com/watch?v=1CEdmZ5P0jA](https://www.youtube.com/watch?v=1CEdmZ5P0jA)
