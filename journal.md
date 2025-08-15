---
title: "Aegis Coffee"
author: "Abdelrahman El Nabawy Mohamed El nabawy Essa"
description: "Four-chamber air purification unit using coffee grounds and real-time sensors to combat urban air pollution."
created_at: "26/06/2025"
---

## Total Time Spent on the Project: **56 hours**

---

##  26/6 – 8 hours  
The spark for this whole thing came one morning when I saw just how much coffee my mother goes through in a single day. The kitchen smelled like a café, and the sink was full of wet coffee grounds. It hit me — *this is all going in the trash, but it still has properties that could be useful*.  

That was the moment I decided to try building an air purification unit that actually **runs on coffee grounds**. Not as fuel, but as a filter medium — using their ability to adsorb smells and trap certain pollutants. No deadlines, no contest, just a personal experiment I wanted in my room.  

The idea quickly took shape as a **four-chamber ventilation unit**:  
1. Dust removal.  
2. Coffee-based VOC adsorption.  
3. Ammonia neutralization with ZnCl₂.  
4. Final polishing filter.  

I spent the morning sketching airflow paths, reading up on activated carbon substitutes, and figuring out how to pair coffee with chemical neutralizers.  

For the brains, I dusted off my **Arduino Mega 2560** with an I/O expansion shield so it could juggle fans, sensors, and servo-controlled airflow flaps without breaking a sweat.  

By the evening, I had a full process diagram taped to my wall, a small pile of coffee grounds on my desk (from “testing”), and the first real excitement that this might actually work.  

---

##  27/6 – 8 hours  
Today was CAD day in **Fusion 360**. I wanted something functional but also nice enough to sit in my room without looking like an industrial prototype.  

I measured the sensors with calipers — MQ-135, SGP30, and DHT22 — and designed their cutouts in the housing. The LCD mount got a **30° tilt** so I could read it from across the room without getting up.  

Airflow simulations revealed two bottlenecks in the bends between chambers. Fixing them meant widening ducts from **45 mm to 55 mm**, which gave ~10% better predicted flow.  

Somewhere in the process, I accidentally staged my coffee mug inside my lightbox when photographing the sketches — so now my project folder has an unintentionally artistic “coffee product photo.”  

![3D chamber layout view](https://github.com/user-attachments/assets/ef9eadab-762e-4900-b1c3-6e378450600c)

---

##  28/6 – 7 hours  
More CAD refinement today. I added details I knew I’d thank myself for later:  
- Slots for silicone gaskets to prevent leaks.  
- Internal cable channels so wires wouldn’t flop around.  
- Secure mounts for the Arduino and power modules.  

Also gave the fan mounts rubber dampers to cut down on vibrations (and that annoying hum).  

By evening, I printed a **PLA mini mock-up** just to check fit. Everything aligned… except for one servo arm that didn’t have clearance to swing. I fixed it in CAD immediately.  

![Rendered 3D prototype](https://github.com/user-attachments/assets/eaa4ae09-3925-4c99-942b-1ccf35015177)

---

##  29/6 – 6 hours  
This was the wiring and control logic planning day.  

I kept the **fan power (12V)** and **sensor power (5V)** separate to avoid electrical noise. Servos would direct airflow between chambers, letting me switch between full purification mode and bypass mode without touching the unit.  

Designed **TPU clips** to hold sensors firmly but with some flex, so fan vibrations wouldn’t mess up readings.  

The Arduino pin mapping is now neatly taped above my desk so I don’t get lost mid-build.  

---

##  1/7 – 8 hours  
Chemistry day — or as I called it, *“let’s make coffee and chemicals get along”*.  

Simulated airflow in the third chamber, where coffee grounds mixed with ZnCl₂ would neutralize ammonia. Texturing the chamber walls improved reaction efficiency by creating turbulence.  

After calculations, I wrote down two key formulas:  
1. Adsorption rate of ammonia on coffee in humid air.  
2. Neutralization efficiency of ZnCl₂ at various flow rates.  

Added **removable trays** for the coffee-ZnCl₂ mix so I can change them without dismantling the chamber.  

Almost made the mistake of drinking from the wrong coffee cup — one was my espresso, the other… my experiment.  

<img width="202" height="77" alt="image" src="https://github.com/user-attachments/assets/fb5d9718-93ff-45f6-b741-8829c7d9e3af" />  
<img width="169" height="58" alt="image" src="https://github.com/user-attachments/assets/1ca88970-fa49-4b7b-8591-298b06b47eb0" />  

---

##  2/7 – 7 hours  
This was “future-proofing” day. Wrote a **Bill of Materials** with everything from the main fans to the tiniest M3 washer, all linked to where I bought them.  

Printed wiring labels for inside the case, because I know future-me will hate unlabeled cables.  

![3D model chamber breakdown](https://github.com/user-attachments/assets/0908067a-cf6b-4a80-9dc8-595c39d0903e)

---

##  3/7 – 4 hours  
Final wrap-up day. Collected every diagram, render, simulation result, and photo into a single “Aegis Coffee – personal build” folder.  

Now it’s running in my room, cycling air through four stages, powered by yesterday’s coffee grounds. No one’s grading it. No contest. Just me, cleaner air, and the faint smell of coffee drifting from the vents.  

Estimated performance based on simulations and material data:  

<img width="250" height="118" alt="image" src="https://github.com/user-attachments/assets/fca738cf-9325-492b-beca-efd66e5ac718" />  

---
