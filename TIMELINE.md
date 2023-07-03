# **🕒 Timeline**

> Timeline of changes in coding, cad, and electronics. Documented with photos and appropriate commits

<br>

## Begin (July 1, 2023)

* Started initial drafting of model
    * Based model off 2 part system, Top and Bottom chassis. All electronics would be hosted on the bottom, and payload and other top chassis could be switched out on top.
        
        * Potential top chassis include: carrier box, flat platform for ROV carrying, tools     
    <img src="https://github.com/charlesdengs/Deli_Bot/blob/main/Progress%20Photos%20of%20CAD%20and%20Robot/TopChassisV1.png" width="300" />
    <img src="https://github.com/charlesdengs/Deli_Bot/blob/main/Progress%20Photos%20of%20CAD%20and%20Robot/BottomChassisV1.png" width="300" />
    <img src="https://github.com/charlesdengs/Deli_Bot/blob/main/Progress%20Photos%20of%20CAD%20and%20Robot/WholeAssemblyV1.png" width="300" />
    
    * Spent a lot of time working on the wheels, wanted to be able to have a logo in the center of the wheel while hiding the nut connecting the shaft to the wheel.
    
    * Calculated how much torque and rpm I needed.
        > Used Robotshop motor sizing tool: https://community.robotshop.com/blog/show/drive-motor-sizing-tool
        
        * My results: https://github.com/charlesdengs/Deli_Bot/blob/main/Progress%20Photos%20of%20CAD%20and%20Robot/MotorSizing.png
        * Picked out a motor: Traxxas 21t 550 motor, seems to have enough rpm and I plan on gearing down to 400 rpm to be able to reach 5mph.

        

## Day 2 (July 2, 20203)
* Did research on how ESCs communicate with arduino and how to pick one out. This was helpful: (https://maker.pro/custom/tutorial/how-to-select-motor-controllers-for-big-motors) It came with a spreadsheet of different ESCs, current ratings, and motor style.
* Picked the Hobbywing 1060 ESC, since it was cheap, met my amp requirements, and could fit a 3S lipo.
* Printed out version 1 of the wheel, it was incredibiliy heavy, so I'm going to go back and try and work that out. I still want to use a rigid wheel, unlike some of the softer wheels on some rovers.
* Researched different gearboxes, chose double geartrain because it is compact and not complicated.
* Worked on gearbox, created variables for shaft diameter, in case I can't find a proper shaft. Chose herringbone gears, so it meshes better and it prints better than double helical. The motor I chose didn't have rpm or kv rating, but had turns instead. I believe based off some of the other motors I saw that were 550, a 30:1 gear reduction would work well.
    * Created a spreadsheet with inner-outer diameter pattern to create sketch for where each gear needs to sit on gearbox.
        * https://github.com/charlesdengs/Deli_Bot/blob/main/GearSizingForGearBox.txt
