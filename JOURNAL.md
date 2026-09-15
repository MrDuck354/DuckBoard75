---
title: "DuckBoard 75%"
author: "MrDuck354"
description: "A basic 75% keyboard with 3d printed case and plate and a custom PCB."
created_at: "2026-09-12"
---

# 2026-09-12: changing BOM

**Total time spent: 0.5 hours**

I decided that It would be best for me to just get the funds for the 3d printed case through here, a library close to me has a makerspace with 3d printers, laser cutters etc and they charge 10 cents per gram of filament. I put my bottom case and plate through PrusaSlicer so I can see how much filament it would use. Since the 3D printer bed that the library has is 900x600mm, my parts fit on the bed without having to slice them in half, Prusa Slicer says that my bottom case and plate will use about 336 grams of filament and at 10 cents per gram, that's about $34 NZD which is about $20 USD at the current exchange rate. I then put this into all my BOM's and costs.

![image](https://cdn.hackclub.com/01a016e3-65fa-7ba8-b911-fc8f37e1ec17/Screenshot%202026-08-19%20095602.png)
![image](https://cdn.hackclub.com/01a016e3-896a-7743-b268-e4337dfab801/Screenshot%202026-08-19%20095618.png)

# 2026-09-12: fixing PCB pt 2 + fixing case/plate

**Total time spent: 2.0 hours**

Started off by adding the wires I left from last journal entry, not much to say about that.

![image](https://cdn.hackclub.com/019feb05-dd62-7832-82e1-7a288ad74185/Screenshot%202026-08-10%20195706.png)

Then I started on my plate where I moved the micro controller cut out to the edge to fit the new placement, then I added it to my assembly to see how it fit with my bottom case. When I put my plate in the proper place it turns out that it was a few mm off the screw holes so I increased the size of the plate and moved the switch holes to the right spots

![image](https://cdn.hackclub.com/019feb07-a1cc-7e42-8126-4ea7b29ae60b/Screenshot%202026-08-10%20200756.png)
![image](https://cdn.hackclub.com/019feb07-bb71-716c-907f-6ee6483105c6/Screenshot%202026-08-10%20201700.png)
![image](https://cdn.hackclub.com/019feb08-00a7-7f36-9811-9973e0d0367a/Screenshot%202026-08-10%20202659.png)

After that I checked the fit with the PCB but when I hid the plate the PCB was slightly off center which meant that the switch holes in the plate were in the wrong spot so I fixed that easily.

![image](https://cdn.hackclub.com/019feb09-48ea-748b-b3c6-5a88206f9372/Screenshot%202026-08-10%20204545.png)

Then I realized that I never added a hole for the wire to connect to the micro controller through the case so I spent a bit of time adding that.

![image](https://cdn.hackclub.com/019feb0a-04e9-76a4-93ea-75d472bc7491/Screenshot%202026-08-10%20212657.png)
![image](https://cdn.hackclub.com/019feb0a-21fb-7c6d-a44f-55e7737142c7/Screenshot%202026-08-10%20212706.png)

Now everything is in the right places and fit together properly. Here are some screen shots of the finished product, I also added the plate and case files to GitHub but the assembly.stl file couldn't be added as it's too big due to the amount of parts the PCB has in OnShape so to see that you have to go to the OnShape link in my GitHub repo.

![image](https://cdn.hackclub.com/019feb0b-afdc-7d86-b553-65e978d232f2/Screenshot%202026-08-10%20212719.png)
![image](https://cdn.hackclub.com/019feb0b-d638-7318-9b34-56c9574cf2e0/Screenshot%202026-08-10%20212730.png)

# 2026-09-12: Fixing the PCB

**Total time spent: 0.2 hours**

I did a bit of work at school during lunch. I made the corners of the PCB curved so it's not pointy but to move the micro controller to the edge of the PCB I need to re do a lot of the wiring so I just left it till I get home.
![image](https://cdn.hackclub.com/019fe928-5b1c-7427-816f-269d37bc07d5/image.png)

# 2026-09-12: Completed firmware and fixed PCB

**Total time spent: 1.1 hours**

2 and a half hours of pain fixed in just over an hour...
In the error found in the previous journal entry, it was because I had named the layout as "duckboard75" but qmk wants it in a certain format starting with LAYOUT so I changed it to "LAYOUT_75_ANSI" but that still gave an error because it's supposed to be "LAYOUT_75_ansi" so I fixed all that. Now I thought that that would be the end of the errors but I thought wrong. Once I tried compiling it again, I got a long list of warnings and errors (Shown below)

![image](https://cdn.hackclub.com/019fe5a1-5a50-7c7c-a65c-82bee7270745/Screenshot%202026-08-09%20193306.png)
![image](https://cdn.hackclub.com/019fe5a1-78b3-76d5-aa6f-161f690e0351/Screenshot%202026-08-09%20193317.png)

According to the errors, row 5 was never connected to the micro controller which I thought was an error I would never had made but low and behold I did in fact make that mistake. Row 5 was never connected to the micro controller so I remedied it by connecting row 5 to the D1 (GP1) pin and then adding that to the row thing in my code.

![image](https://cdn.hackclub.com/019fe5a3-9212-7c27-9cd3-40885e115158/Screenshot%202026-08-09%20194657.png)
![image](https://cdn.hackclub.com/019fe5a3-a6a7-7aa6-b8e6-7be787c30445/Screenshot%202026-08-09%20194909.png)
![image](https://cdn.hackclub.com/019fe5a4-24bc-7417-b04b-55716cf32c67/Screenshot%202026-08-09%20195504.png)

After that I encountered my second to last error which was my code had some keys connected to columns 15 and 16 but I only have columns 0-14. This was caused by my bottom row of keys jumping from 6 to 15 and I don't remember doing that but I guess I'm a bit dim. Once fixing that my last error was just having a semi colon in the wrong spot. I compiled the code successfully and uploaded the firmware and the fixed PCB to github. I also put the files into JLCPCB to see if it would cost more but it still costs the same amount.

# 2026-09-12: Progressing through the firmware

**Total time spent: 2.5 hours**

I started working through the previously mentioned tutorial and got all the way through it up until I had to compile it.
![image](https://cdn.hackclub.com/019fe407-65bb-7d90-9556-33f5ebf0f410/Screenshot%202026-08-09%20111829.png)
![image](https://cdn.hackclub.com/019fe407-87cb-7a62-9d61-e4951b99e49d/Screenshot%202026-08-09%20123557.png)

When I tried to compile the code I got some errors and ended up spending so much time trying to fix it that I got frustrated and rage quit so I'll leave it till tomorrow or later today.
![image](https://cdn.hackclub.com/019fe408-78ae-7660-921f-b2d37d021e43/Screenshot%202026-08-09%20124736.png)

# 2026-09-12: Fixing OnShape link and starting firmware

**Total time spent: 0.8 hours**

started off by fixing the OnShape link, instead of copying the url while I was working on it I had to click on the share button and use that url.
I started looking around for tutorials and I settled on iNimbleSloth's tutorial https://www.youtube.com/watch?v=9bjp_LteX_Y
![image](https://cdn.hackclub.com/019fe374-ec93-717d-9da6-e16ea4f78468/image.png)

I watched through it once to make sure that it will actually be useful for me and it was.
Next I will begin working through his tutorial though it seems like a lengthy process

# 2026-09-12: Updated the README on Github

**Total time spent: 0.4 hours**

Updated the read me to include the BOM and changed the formatting to make it more organized by adding the onshape link, adding the steps I took and shortening the project goals
![image](https://cdn.hackclub.com/019fdb63-01d2-7546-9f87-c73b2886e345/Screenshot%202026-08-07%20203940.png)
![image](https://cdn.hackclub.com/019fdb62-b385-722d-a6e2-910ffddcbf74/image.png)

# 2026-09-12: changing description

**Total time spent: 0.1 hours**

i spent a short amount of time changing my description. I also found some diodes on aliexpress which meant I didn't have to pay for the shipping but the total ended up being more somehow ($78 instead of the current $73) so I kept the old diodes.
![image](https://cdn.hackclub.com/019fd8c8-e635-7980-b9c0-a1b647c15fdd/image.png)

# 2026-09-12: Finishing Case + BOM

**Total time spent: 2.3 hours**

Started off by creating the bottom case, I first measured the plate then made the inside of the case slightly larger so that the plate would fit. I then created the walls and put the plate in to see if it would all fit. I then added screw holes to the case and the plate. I did a bit of research and it seems like most 3d printed cases don't use a top case and instead use the plate as the top so that's what I will do. I then realized that I never created a hole in the plate for the microcontroller to sit in so I added that. Here are some photos of the completed case and plate.

![image](https://cdn.hackclub.com/019fbac3-77dd-7a47-a73b-28116ddd9e19/Screenshot%202026-08-01%20114111.png)
![image](https://cdn.hackclub.com/019fbac3-b3e2-7099-8dc7-07cb5f065c87/Screenshot%202026-08-01%20111654.png)

I then added the files to Github and began working on my BOM. For my BOM, all the parts are from aliexpress and 3 are apart of one of their bundle deals. I will fund the 3D printing myself

![image](https://cdn.hackclub.com/019fbad5-3b2d-7538-adcd-781e9c37749e/Screenshot%202026-08-01%20125818.png)
![image](https://cdn.hackclub.com/019fbad5-65e7-7d51-bb58-0f50141e67a6/Screenshot%202026-08-01%20125852.png)
![image](https://cdn.hackclub.com/019fbad5-83ae-739d-8093-cf1666b270d3/Screenshot%202026-08-01%20125900.png)
![image](https://cdn.hackclub.com/019fbad5-a76d-7add-aa2e-bdf8dcc5ca2c/Screenshot%202026-08-01%20125908.png)

Heres my timelapse:
https://lapse.hackclub.com/timelapse/eOVi5fF8ssbe

Next Steps:
Create the firmware to put on the Microcontroller and get funding

# 2026-09-12: Finishing the plate

**Total time spent: 3.6 hours**

Started off by adding squares in the plate for the switches to go into. They're supposed to be 14mm because that's the size holes that standard MX switches clip into but I made them 14.15mm because of any plastic shrinkage that may happen when I 3D print the case. After that I did a bit more research on the case and I wanted to add a line art of a duck to the case to make it more personalized but I had no clue how to re size a .dxf file so i'm just gonna leave that to a later date. The plate is 3mm thick but it needs to be 1.5mm around the switch for it to properly clip in so I added a second square which was extruded to 1.5mm instead of 3mm, I made the plate 3mm thick so that it wouldn't break easily under pressure. Here's some photos of the completed plate, i'll add screw holes later when I finish the bottom case because I don't really know where to put the holes right now.

![image](https://cdn.hackclub.com/019fb77b-2c82-7492-b563-e58f2986ebcb/Screenshot%202026-07-31%20210706.png)
![image](https://cdn.hackclub.com/019fb77b-6276-77b5-b2fe-50d1a766e8e4/Screenshot%202026-07-31%20210730.png)

Here's my timelapse:
https://lapse.hackclub.com/timelapse/d68X6dKh54Kl

Next steps:
Start the bottom and top parts of the case.

# 2026-09-12: Finishing PCB and starting the case

**Total time spent: 2.6 hours**

Started by putting labels on all the connections I need so that I can see what isn't connected yet in the PCB tool. I then put all the switches in the correct spots and wired them up, then I added the diodes and wired them together. This whole process was very time consuming, I also went back to Scotto's tutorial to check if I missed anything or not. I added my PCB files to Github. Here's photos of my finished PCB

![image](https://cdn.hackclub.com/019fb222-3e50-7c30-aeed-3ce1b2e79481/Screenshot%202026-07-30%20175523.png)
![image](https://cdn.hackclub.com/019fb222-7b68-753b-adad-be1db6b25a1d/Screenshot%202026-07-30%20191810.png)
![image](https://cdn.hackclub.com/019fb222-abf5-778d-bfb2-4b6765b10812/Screenshot%202026-07-30%20192246.png)

I then added my PCB into onshape to design my case around this new PCB. I decided to just completely redesign the case and start from scratch which I thought would be easier, I also decided on making a bottom mount case. I started with designing the plate on the PCB but my laptop was really struggling with this and it became really slow to use the software, I got a bit frustrated by this so I decided to just leave it for tomorrow.
Here's my timelapse:
https://lapse.hackclub.com/timelapse/ggHCVTWVpvnO

Next steps:
Continue designing the plate and then the case.

# 2026-09-12: Designing my own PCB

**Total time spent: 2.3 hours**

Since the most expensive part of my keyboard is the PCB, I decided to just create my own on KiCad which would be a more cost effective option. Although I would have to redesign my case but that's fine.
First I watched a tutorial online by Joe Scotto which helped me learn how to use KiCad and what a keyboard matrix is and how it works. Following his tutorial, I designed a 3x3 grid PCB, switches and all, these skills that I learned from Joe Scotto directly helped me build a keyboard PCB. This is a photo of that PCB that I built from his tutorial

![image](https://cdn.hackclub.com/019fad38-3490-76ec-8b0f-a748d8830d4e/image.png)

After that, I went ahead and started designing my own PCB with a 75% keyboard layout. This was very similar to the tutorial except I chose my own micro controller which would be the RP2040 since it's cheap and other people who did a similar project to me recommended it online and I also added stabilizers for my longer keys.

![image](https://cdn.hackclub.com/019fad3a-e9a6-78c5-aebd-112020d27179/Screenshot%202026-07-29%20212414.png)
![image](https://cdn.hackclub.com/019fad3b-1108-767f-8dbf-2b5e3e8cf3c9/Screenshot%202026-07-29%20212425.png)

Next steps:
I will align all the parts of the PCB to make it look like an actual keyboard, then I'll redesign the case around this new PCB.

# 2026-09-12: Finishing the case and deciding on parts

**Total time spent: 1.2 hours**

Today I started off my fixing the standoffs, They were hollow instead of solid because of a setting on the extrude option which I changed from new to add, then I added a second extrude option on the bottom of the standoffs as they were originally sitting on the top of the bottom instead of going all the way down so there were holes about 10mm long in the bottom of the case which I fixed.
After that I thought about changing the height of the case again when I looked at the side profile because i'm so used to this HP membrane office keyboard i'm using right now so I feel like I wouldn't enjoy using a taller keyboard so I ended up reducing the height by 5mm, if it does end up being too low then I can always 3D print a new one.
I added holes in the middle of the standoffs for the screws to go into but I made them slightly smaller because the screws need to thread themselves, when I added the holes though the sides of the standoffs seemed a bit small to me so I increased them to 3.5mm
![image](https://cdn.hackclub.com/019f969b-c077-747b-9bbd-34bb6344a2d5/image.png)
Once I had added the holes and looked at it with the PCB inside, I had a sudden revelation that nothing was supporting the PCB so it would just fall to the bottom of the case. Using this new found knowledge I tried increasing the size of the standoffs so that it would touch the PCB and support it but for some reason that wouldn't work in the software so I added supporting brackets which would hold the PCB up so now the first prototype of the case is fully finished! yippee.
![image](https://cdn.hackclub.com/019f969e-a423-7a9e-a029-57e59a5c0d76/Screenshot%202026-07-25%20113010.png)
After finishing the case I began looking at keycap and switch options for my keyboard. First I started looking at keycaps because I thought they would be cheap but to my dismay they were around $90 USD on cannonkeys! so I looked on the Gateron website as well but they only had two keycap choices, both of which I didn't like. So I looked at switches, first I narrowed my options down to two linear switches, the Gateron Everfree Curry's and the CK x Haimu Pastel lemon's. But after a bit more research I decided to switch up and go for tactile switches as they would be what I am most used to. I looked on cannon keys and Gateron and I decided on the Gateron chocolate jelly switches which I was originally going to purchase off of cannon keys but they had a large shipping cost so I will get them off of amazon including keycaps I found on amazon. The PCB I will get on cannonkeys which is $62 USD including shipping costs and the keycaps, switches and screws I will get on amazon for a combined price of $85.63 USD including shipping for a total price of $147.63 USD
![image](https://cdn.hackclub.com/019f96bf-e117-7d81-ac3f-573a2c2b9746/Screenshot%202026-07-25%20124821.png)
![image](https://cdn.hackclub.com/019f96c0-0bbb-748d-8e37-bf78d64e25fc/Screenshot%202026-07-25%20124801.png)
![image](https://cdn.hackclub.com/019f96c0-8378-7a2d-b99f-d2b9a70f1849/Screenshot%202026-07-25%20123559.png)


need to get funding for these parts then I can build the keyboard when the parts arrive

heres a link to my timelapse
https://lapse.hackclub.com/timelapse/45xeqn5r-VNa

# 2026-09-12: Adding screw holes for the pcb to sit in the case

**Total time spent: 1.7 hours**

I started off today by looking at other peoples 3D printed keyboard case files for inspiration on how to add my screw holes but I didn't end up finding anything useful which I could implement into my project. After that I took measurements of the PCB for the holes which are cut out of the edges of the PCB which I assume are the holes for the screws, this lead me down a long rabbit hole where every time I would add a hole to my case, it wasn't even in the right spot. 
After the 3rd attempt, I found out that I had somehow measured the PCB height wrong yesterday when I started the project which caused the holes to be miss aligned.
When I found out that I had measured the PCB incorrectly, I began double checking other measurements for the case, one of which being the height of it. In the Onshape software I thought the case looked quite tall so I looked around for measurements of switches and keycaps to see if I should change it or not. I decided to lower the height by 10mm because I would rather a case that is too low than too high. This research also lead me towards figuring out how to thread the holes, typically you would use a m2 size screw with a length of 4-6mm so I made the standoffs 8mm long and 2.5mm wide to ensure that there is enough room for error. 
When dealing with plastic, you can either use heat inserts or self tapping screws. Heat inserts are little brass cylinders which you heat up and melt into the plastic standoffs using your soldering iron, these are quite strong and typically used but I wouldn't trust myself to properly do it so I decided on self tapping screws. 
Self tapping screws are screws which borough into the standoffs basically threading it themselves which I think will be much easier for me. I specifically decided on these screws because they were the cheapest on amazon which can be used for plastic
![image](https://cdn.hackclub.com/019f93a5-6784-77bd-b681-3e5c0c263c5c/Screenshot%202026-07-24%20220846.png)

After I did all this research I actually got the holes in the right spots by measuring the distance between the middle of the hole and the middle of the PCB screw holes when they were close to each other which proved to be the best course of action (which I should've done in the first place but oh well). Here is a photo of the case so far and the case with the PCB in.
![image](https://cdn.hackclub.com/019f93a8-2608-754a-b7a8-03852ee9dabb/Screenshot%202026-07-24%20220831.png)
![image](https://cdn.hackclub.com/019f93a8-68aa-7790-9b08-34e009594d11/Screenshot%202026-07-24%20222253.png)

Next steps:
add small holes through the standoffs so that the self tapping screws can borough in properly, decide on a set of keycaps and switches and get funding for the PCB, screws, keycaps and switches

Here's my timelapse: https://lapse.hackclub.com/timelapse/-FbHM5XkMHVH

# 2026-09-12: Start of the project - learning how to use Onshape and designing the case.

**Total time spent: 2.1 hours**

I started this project by learning Onshape using the built in tutorial as I have never used the software, or any 3D modelling software, before so this is all new to me. The tutorial taught me things like how to add screws/screw holes and the layout but it didn't teach me how to create basic shapes or lines which I later learned through trial and error and some tutorials I found online when searching up help for some problems. 

After completing the tutorial I started looking around for a PCB I could build my case around. I looked on alibaba and aliexpress but I only found a bunch of hotswappable PCBs which would not be ideal for me to learn how to solder on. I eventually stumbled upon a website called CannonKeys who sell generic PCBs which are meant to be used as a replacement PCB for other keyboards so they have the most compatibility which would be best for me. I decided upon a 75% keyboard layout as that would be best for my needs (picture below of the PCB, prices in NZD I think its $45 USD?) I will probably end up buying switches and keycaps from the same site because that would be easier and they sell a wide variety of both.
![image](https://cdn.hackclub.com/019f8dea-655e-7ea1-8238-fdbd8a6977dc/image.png)

finally I started designing my case on Onshape. figuring out how to add the PCB into Onshape took a while for me to do but I found a .step file online which is provided by CannonKeys on a different website for some reason so I just imported that file into it. This is when I began my afformentioned trial and error and watching tutorials because I somehow couldn't figure out how to create a basic hollow rectangle with walls...
this is a picture of my case so far, pretty barebones but its most of the work done already.
![image](https://cdn.hackclub.com/019f8dee-a8ce-779d-ac7f-623cbe2dd8f8/image.png)

Next steps:
add screw holes and maybe some customized designs on it to make it look cool and unique, test fit with the PCB and hopefully it all works out. After that I will look at switches and keycaps and hopefully acquire funding to purchase all the parts I need.

https://lapse.hackclub.com/timelapse/uQ7YKJ-IyvPE

