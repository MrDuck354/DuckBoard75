---
Title: DuckBoard75
Author: MrDuck354
Description: A basic 75% keyboard with a 3d printed case, plate and a custom PCB
Created on: 23/07/26
---

# July 29th: Designing my own PCB

Since the most expensive part of my keyboard is the PCB, I decided to just create my own on KiCad which would be a more cost effective option. Although I would have to redesign my case but that's fine. First I watched a tutorial online by Joe Scotto which helped me learn how to use KiCad and what a keyboard matrix is and how it works. Following his tutorial, I designed a 3x3 grid PCB, switches and all, these skills that I learned from Joe Scotto directly helped me build a keyboard PCB. This is a photo of that PCB that I built from his tutorial

<img width="1183" height="813" alt="image" src="https://github.com/user-attachments/assets/d77d22b6-9796-4e16-b213-cf8d9c4fb5a1" />

After that, I went ahead and started designing my own PCB with a 75% keyboard layout. This was very similar to the tutorial except I chose my own micro controller which would be the RP2040 since it's cheap and other people who did a similar project to me recommended it online and I also added stabilizers for my longer keys.

<img width="1073" height="733" alt="image" src="https://github.com/user-attachments/assets/2867d0d7-4569-4edd-b40d-bc6ca7afc4ff" />
<img width="1183" height="813" alt="image" src="https://github.com/user-attachments/assets/2dad2a8c-2b5c-4cf6-9c8a-91aee08d038b" />

Next steps: I will align all the parts of the PCB to make it look like an actual keyboard, then I'll redesign the case around this new PCB.

**Total time spent: 2.3 hours**

#July 30th: Finishing PCB and starting the case

Started by putting labels on all the connections I need so that I can see what isn't connected yet in the PCB tool. I then put all the switches in the correct spots and wired them up, then I added the diodes and wired them together. This whole process was very time consuming, I also went back to Scotto's tutorial to check if I missed anything or not. I added my PCB files to Github. Here's photos of my finished PCB

<img width="1267" height="833" alt="image" src="https://github.com/user-attachments/assets/2ddf78b8-137a-490c-ac7d-36011862dc94" />
<img width="972" height="461" alt="image" src="https://github.com/user-attachments/assets/d4c94b9b-ff3f-4e19-aa9f-eb5dea789fd9" />
<img width="1526" height="724" alt="image" src="https://github.com/user-attachments/assets/ea60e38a-08dc-4dfc-87d4-43d514d7f04b" />

I then added my PCB into onshape to design my case around this new PCB. I decided to just completely redesign the case and start from scratch which I thought would be easier, I also decided on making a bottom mount case. I started with designing the plate on the PCB but my laptop was really struggling with this and it became really slow to use the software, I got a bit frustrated by this so I decided to just leave it for tomorrow. Here's my timelapse: https://lapse.hackclub.com/timelapse/ggHCVTWVpvnO
Next steps: Continue designing the plate and then the case.

**Total time spent: 2.6 hours**

# Finishing the plate

Started off by adding squares in the plate for the switches to go into. They're supposed to be 14mm because that's the size holes that standard MX switches clip into but I made them 14.15mm because of any plastic shrinkage that may happen when I 3D print the case. After that I did a bit more research on the case and I wanted to add a line art of a duck to the case to make it more personalized but I had no clue how to re size a .dxf file so i'm just gonna leave that to a later date. The plate is 3mm thick but it needs to be 1.5mm around the switch for it to properly clip in so I added a second square which was extruded to 1.5mm instead of 3mm, I made the plate 3mm thick so that it wouldn't break easily under pressure. Here's some photos of the completed plate, i'll add screw holes later when I finish the bottom case because I don't really know where to put the holes right now.

<img width="953" height="362" alt="image" src="https://github.com/user-attachments/assets/80f727e1-a1d8-4127-b662-9a4269a148df" />
<img width="1397" height="711" alt="image" src="https://github.com/user-attachments/assets/fa12e8f0-75b0-483a-b097-3a79d4253623" />

Here's my timelapse: https://lapse.hackclub.com/timelapse/d68X6dKh54Kl
Next steps: Start the bottom and top parts of the case.

**Total time spent: 3.6 hours**

# August 1st: Finishing Case + BOM

Started off by creating the bottom case, I first measured the plate then made the inside of the case slightly larger so that the plate would fit. I then created the walls and put the plate in to see if it would all fit. I then added screw holes to the case and the plate. I did a bit of research and it seems like most 3d printed cases don't use a top case and instead use the plate as the top so that's what I will do. I then realized that I never created a hole in the plate for the microcontroller to sit in so I added that. Here are some photos of the completed case and plate.

<img width="1363" height="713" alt="image" src="https://github.com/user-attachments/assets/381a8671-37f3-49d3-a98c-214d80dc20ba" />
<img width="1464" height="799" alt="image" src="https://github.com/user-attachments/assets/bb7d52fd-2914-4213-92cc-71b44090338d" />

I then added the files to Github and began working on my BOM. For my BOM, all the parts are from aliexpress and 3 are apart of one of their bundle deals. I will fund the 3D printing myself

<img width="1243" height="674" alt="image" src="https://github.com/user-attachments/assets/3a0bf0a4-754d-4139-8596-322daeec2e76" />
<img width="1456" height="638" alt="image" src="https://github.com/user-attachments/assets/3fce0db4-2920-47cf-9743-a073af435fbe" />
<img width="1278" height="858" alt="image" src="https://github.com/user-attachments/assets/1f4edcfd-fbd7-483b-9cbb-1f71972f4476" />
<img width="849" height="566" alt="image" src="https://github.com/user-attachments/assets/58d6e91a-4b11-454e-a8da-6cdb6b3608fa" />

Heres my timelapse: https://lapse.hackclub.com/timelapse/eOVi5fF8ssbe
Next Steps: Create the firmware to put on the Microcontroller and get funding

**Total time spent: 2.3 hours**

# August 7th: Updated the README on Github

Updated the read me to include the BOM and changed the formatting to make it more organized by adding the onshape link, adding the steps I took and shortening the project goals

<img width="1345" height="841" alt="image" src="https://github.com/user-attachments/assets/0c7a2547-db81-4dfe-9df0-6137f35c75a2" />
<img width="1037" height="805" alt="image" src="https://github.com/user-attachments/assets/ee1c64cb-1f3f-4235-bba0-7e3ec28e33d5" />

**Total time spent: 0.4 hours**

# August 9th: Fixing Onshape link and starting firmware

started off by fixing the OnShape link, instead of copying the url while I was working on it I had to click on the share button and use that url. I started looking around for tutorials and I settled on iNimbleSloth's tutorial https://www.youtube.com/watch?v=9bjp_LteX_Y

<img width="1344" height="851" alt="image" src="https://github.com/user-attachments/assets/bc538cd6-a858-4bc0-a789-370cd08396be" />

I watched through it once to make sure that it will actually be useful for me and it was. Next I will begin working through his tutorial though it seems like a lengthy process

**Total time spent: 0.8 hours**

# August 9th: Progressing through the firmware

I started working through the previously mentioned tutorial and got all the way through it up until I had to compile it.

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/a25f8149-2bcb-479b-85f0-0aec08aca732" />
<img width="1399" height="695" alt="image" src="https://github.com/user-attachments/assets/548e7686-a89d-4809-8452-ee925ac81ddd" />

When I tried to compile the code I got some errors and ended up spending so much time trying to fix it that I got frustrated and rage quit so I'll leave it till tomorrow or later today.

<img width="1916" height="601" alt="image" src="https://github.com/user-attachments/assets/50eaef66-195d-44ea-9d7e-e15662eb0d29" />

**Total time spent: 2.5 hours**

# August 9th: Completed firmware and fixed PCB

2 and a half hours of pain fixed in just over an hour... In the error found in the previous journal entry, it was because I had named the layout as "duckboard75" but qmk wants it in a certain format starting with LAYOUT so I changed it to "LAYOUT_75_ANSI" but that still gave an error because it's supposed to be "LAYOUT_75_ansi" so I fixed all that. Now I thought that that would be the end of the errors but I thought wrong. Once I tried compiling it again, I got a long list of warnings and errors (Shown below)

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/e1f4c0ce-c6a6-44b7-ac34-5538c0302bdd" />
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/0e537e43-01a9-494d-bdfc-1827b9cdda80" />

According to the errors, row 5 was never connected to the micro controller which I thought was an error I would never had made but low and behold I did in fact make that mistake. Row 5 was never connected to the micro controller so I remedied it by connecting row 5 to the D1 (GP1) pin and then adding that to the row thing in my code.

<img width="696" height="627" alt="image" src="https://github.com/user-attachments/assets/d9a6344f-16c1-4cae-a899-746219783cba" />
<img width="499" height="497" alt="image" src="https://github.com/user-attachments/assets/2fbd4d7d-3daa-49da-a1f0-4fdcb57845cb" />
<img width="1016" height="112" alt="image" src="https://github.com/user-attachments/assets/e825f1a0-4057-4ea3-9d87-a1bde8570008" />

After that I encountered my second to last error which was my code had some keys connected to columns 15 and 16 but I only have columns 0-14. This was caused by my bottom row of keys jumping from 6 to 15 and I don't remember doing that but I guess I'm a bit dim. Once fixing that my last error was just having a semi colon in the wrong spot. I compiled the code successfully and uploaded the firmware and the fixed PCB to github. I also put the files into JLCPCB to see if it would cost more but it still costs the same amount.

**Total time spent: 1.2 hours**

# August 10th: Fixing the PCB

I did a bit of work at school during lunch. I made the corners of the PCB curved so it's not pointy but to move the micro controller to the edge of the PCB I need to re do a lot of the wiring so I just left it till I get home.

<img width="803" height="796" alt="image" src="https://github.com/user-attachments/assets/eccf3cba-1a69-4f75-b4f2-d9426fe1c58b" />

**Total time spent: 0.3 hours**

# August 10th: Fixing PCB pt 2 + fixing case/plate

Started off by adding the wires I left from last journal entry, not much to say about that.

<img width="1108" height="742" alt="image" src="https://github.com/user-attachments/assets/b88cb90e-7fbc-4722-8545-2fd14ddd6515" />

Then I started on my plate where I moved the micro controller cut out to the edge to fit the new placement, then I added it to my assembly to see how it fit with my bottom case. When I put my plate in the proper place it turns out that it was a few mm off the screw holes so I increased the size of the plate and moved the switch holes to the right spots

<img width="434" height="397" alt="image" src="https://github.com/user-attachments/assets/bf8a9c75-7303-4cca-9a63-da8def425264" />
<img width="978" height="780" alt="image" src="https://github.com/user-attachments/assets/7c368c5a-df56-4feb-b425-b49c3b4eca88" />
<img width="1435" height="615" alt="image" src="https://github.com/user-attachments/assets/b179576b-f1b2-4ec2-b3a4-7d43b1d6ca1e" />

After that I checked the fit with the PCB but when I hid the plate the PCB was slightly off center which meant that the switch holes in the plate were in the wrong spot so I fixed that easily.

<img width="1212" height="513" alt="image" src="https://github.com/user-attachments/assets/78f6396b-6257-4c2c-ab50-f61bda84d7aa" />

Then I realized that I never added a hole for the wire to connect to the micro controller through the case so I spent a bit of time adding that.

<img width="623" height="459" alt="image" src="https://github.com/user-attachments/assets/1e07f319-1917-49c6-b09d-2d036e0e6a4b" />
<img width="648" height="549" alt="image" src="https://github.com/user-attachments/assets/adda6f6d-d500-47ef-8dc4-2a6c3b52df74" />

Now everything is in the right places and fit together properly. Here are some screen shots of the finished product, I also added the plate and case files to GitHub but the assembly.stl file couldn't be added as it's too big due to the amount of parts the PCB has in OnShape so to see that you have to go to the OnShape link in my GitHub repo.

<img width="1138" height="458" alt="image" src="https://github.com/user-attachments/assets/1fa6ef3d-a5fc-4bf7-8128-2225b1595e50" />
<img width="1406" height="604" alt="image" src="https://github.com/user-attachments/assets/443e74d0-f563-4c2d-a2e0-a2c8add7fec3" />

**Total time spent: 2 hours**

# August 19th: Changing BOM

I decided that It would be best for me to just get the funds for the 3d printed case through here, a library close to me has a makerspace with 3d printers, laser cutters etc and they charge 10 cents per gram of filament. I put my bottom case and plate through PrusaSlicer so I can see how much filament it would use. Since the 3D printer bed that the library has is 900x600mm, my parts fit on the bed without having to slice them in half, Prusa Slicer says that my bottom case and plate will use about 336 grams of filament and at 10 cents per gram, that's about $34 NZD which is about $20 USD at the current exchange rate. I then put this into all my BOM's and costs.

<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/88fbfca9-c39b-44c0-889d-230d47dc484a" />
<img width="315" height="196" alt="image" src="https://github.com/user-attachments/assets/6cb7ab23-e846-452b-9b50-2ea124ac40d3" />

**Total time spent: 0.5 hours**


# September 18th: Fixing BOM

I added the proper names for both BOMs (the read me one and the .csv one) and fixed some of the links because they brought you to the shopping cart instead of the actual products. The keycaps were unavailable so I had to change them with different ones, these new keycaps were on sale for very cheap but the sale ends on the 21st of september so I put the normal price instead. This does raise the total price to $113.

<img width="888" height="772" alt="image" src="https://github.com/user-attachments/assets/2ddc3492-a2d1-49f6-885e-565c8e335f65" />

**Total time spent: 0.5 hours**
