---
title: "Aegis Coffee"
author: "Abdelrahman El Nabawy Mohamed El nabawy Essa"
description: "Four-chamber air purification unit using coffee grounds and real-time sensors to combat urban air pollution."
created_at: "26/06/2025"
---

## Total Time Spent on the Project: **56 hours**

---

##  26/6 – 8 hours  
I began the project by locking in the conceptual framework — a four-chamber ventilation system designed to sequentially clean and chemically treat polluted air, using **coffee grounds** as the primary adsorption medium, paired with neutralizing agents like **NH₃** and **ZnCl₂** for targeted removal of specific pollutants.  

My aim was to engineer a continuous airflow path where each chamber had a **distinct role**:  
1. **Particulate filtration** – to catch dust and PM2.5.  
2. **Coffee-based adsorption** – to capture VOCs and certain acidic gases.  
3. **Chemical neutralization** – to handle ammonia and acidic residues.  
4. **Polishing filter** – to ensure clean, breathable output air.  

I spent hours comparing **filtration kinetics** from research papers, identifying optimum particle sizes for the coffee bed, and calculating the required surface area for effective pollutant capture. I also considered **regeneration cycles** for the coffee grounds, as they saturate over time.  

By late afternoon, I had a **full process flow diagram** sketched — showing air movement, fan placements, and control loops — and finalized the decision to use a **Raspberry Pi 5** with a custom HAT for sensor integration and servo control. This would serve as the “brain” for automated monitoring of CO₂, PM2.5, VOC levels, and humidity.  

---

##  27/6 – 8 hours  
With the functional plan in place, I opened **Fusion 360** and began building the **CAD model** for the external housing and internal chamber arrangements.  

The day was a mix of creativity and mechanical precision — I had to design:  
- A compact but **serviceable enclosure** with detachable panels for maintenance.  
- Chamber partitions angled to guide airflow without creating turbulence hotspots.  
- Mounting frames for **high-CFM fans** to maintain constant flow rates.  
- Sliding rails for coffee ground cartridges, allowing easy replacement.  

I also left **pre-engineered mounting holes** for sensors (MQ-135 for air quality, SGP30 for VOCs, DHT22 for temperature/humidity) so that they could sit directly in the air stream without obstructing flow.  

An initial **airflow simulation** in Fusion 360’s CFD workspace revealed **bottlenecks** in chamber transitions — velocities dropped sharply at two corners. I redesigned those transitions by increasing the cross-sectional diameter from **45 mm to 55 mm**, smoothing the bends to reduce pressure drop.  

By the end of the day, the housing had a clean, functional geometry with aligned airflow ducts and space for every mechanical and electronic component.  

![3D chamber layout view](https://github.com/user-attachments/assets/ef9eadab-762e-4900-b1c3-6e378450600c)

---

##  28/6 – 7 hours  
This was the **refinement day**. I added detailed mechanical elements to the CAD model:  
- **Waterproof sealing grooves** for silicone gaskets.  
- Bracket arms for the Raspberry Pi and the 16x2 LCD display.  
- Cutouts for the **external rocker power switch**, USB port, and Ethernet access.  

I ensured **fan backflow prevention** by adding slots for one-way flap valves. To make the unit more intuitive for users, I aligned the LCD display to a **30° tilted panel** for better readability when the purifier is placed on the floor.  

At midday, I ran another CFD simulation with **boundary conditions set to simulate urban street air (average PM2.5 ~60 µg/m³)**. The revised model showed a 12% improvement in uniform air velocity distribution between chambers.  

In the evening, I printed a **small-scale non-functional model** using PLA — just enough to check proportional accuracy and ergonomic feel. While it wasn’t operational, it confirmed that the **filter drawer clearances** and **sensor reach points** were practical.  

![Rendered 3D prototype](https://github.com/user-attachments/assets/eaa4ae09-3925-4c99-942b-1ccf35015177)

---

##  29/6 – 6 hours  
This day was dedicated to **wiring layout planning**. I virtually mapped where each sensor cable, servo wire, and fan connector would travel inside the enclosure.  

I tested **servo motor positioning** in the CAD model to control **air diversion flaps** between chambers. These flaps would allow different operation modes:  
- **Full purification** (all chambers active)  
- **Bypass mode** (direct fresh-air feed when air quality is already good)  

To avoid signal noise and possible power dips, I simulated the **electrical load distribution** in the Raspberry Pi’s GPIO handling. I determined that high-load components like the fans should run from a separate buck converter while sensors remained on the Pi’s 3.3V logic line.  

By late afternoon, I **generated section diagrams** and **exploded views** for documentation. I added **custom sensor clip mounts** that could be 3D printed in flexible TPU to absorb vibration from fan operation.  

The CAD model was now finalized, and I exported both **STL** (for printing) and **DXF** (for laser cutting) files for future fabrication.  

---

##  1/7 – 8 hours  
Focus shifted to the **chemical reaction chamber** — the third stage. This is where coffee grounds and ZnCl₂ would actively neutralize ammonia.  

I used computational fluid dynamics with **reactive flow modeling** to simulate how ammonia molecules would diffuse through a packed bed of coffee grounds under varying humidity. I experimented with **inner wall surface texturing** (micro-ridges vs. smooth coating) to enhance residence time.  

Two **key equations** were derived to model:  
1. **Ammonia adsorption rate** on coffee-activated carbon in mixed humidity streams.  
2. **Neutralization efficiency** of ZnCl₂ under varying air velocities.  

The chamber was redesigned with **bracket slots** for removable filter trays, each hermetically sealed to prevent bypass leakage. A **vapour trap section** was also included to prevent ammonia-laden air from escaping before neutralization.  

<img width="202" height="77" alt="image" src="https://github.com/user-attachments/assets/fb5d9718-93ff-45f6-b741-8829c7d9e3af" />  
<img width="169" height="58" alt="image" src="https://github.com/user-attachments/assets/1ca88970-fa49-4b7b-8591-298b06b47eb0" />  

---

##  2/7 – 7 hours  
This was a **documentation-heavy engineering day**.  

I finalized the **assembly sequence**, ensuring that the manufacturing process could be performed with **minimal tools** and in under two hours. I included detailed notes on:  
- Torque specs for fastening components.  
- Correct routing of sensor wiring to avoid electromagnetic interference.  
- Placement order of filters, coffee grounds, and chemical media.  

I created a **Bill of Materials (BOM)** with exact vendor links, part numbers, and quantities, cross-referencing each against the CAD model to ensure no missing components.  

![3D model chamber breakdown](https://github.com/user-attachments/assets/0908067a-cf6b-4a80-9dc8-595c39d0903e)

---

##  3/7 – 4 hours  
The final stage was **complete project consolidation**.  

I formatted the README with:  
- Project introduction and goals.  
- System architecture diagram.  
- Wiring schematic.  
- Step-by-step assembly instructions.  
- Sensor calibration procedures.  

I embedded **rendered images**, CAD screenshots, and all equations into the GitHub repository. I also proofread every document, checked for **broken file links**, and ensured that diagrams were in **SVG or PNG** for universal compatibility.  

The result was a **fully documented, reproducible open-source air purification unit** design that combines low-cost materials with **environmental reuse** (coffee waste) to combat urban pollution.  

Estimated performance results (based on simulation and material specs):  

<img width="250" height="118" alt="image" src="https://github.com/user-attachments/assets/fca738cf-9325-492b-beca-efd66e5ac718" />  

---
