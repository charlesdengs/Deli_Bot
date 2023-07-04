# **🕒 Timeline**

> Timeline of changes in coding, cad, and electronics. Documented with photos and appropriate commits

<br>

## Begin (July 1, 2023) - Day 1!!!

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

        

## Day 2 (July 2, 2023) - Research
* Did research on how ESCs communicate with arduino and how to pick one out. This was helpful: (https://maker.pro/custom/tutorial/how-to-select-motor-controllers-for-big-motors) It came with a spreadsheet of different ESCs, current ratings, and motor style.
* Picked the Hobbywing 1060 ESC, since it was cheap, met my amp requirements, and could fit a 3S lipo.
* Printed out version 1 of the wheel, it was incredibiliy heavy, so I'm going to go back and try and work that out. I still want to use a rigid wheel, unlike some of the softer wheels on some rovers.
<img src="https://github.com/charlesdengs/Deli_Bot/blob/main/Progress%20Photos%20of%20CAD%20and%20Robot/NewWheels.png" width="200" />

* Researched different gearboxes, chose double geartrain because it is compact and not complicated.
* Worked on gearbox, created variables for shaft diameter, in case I can't find a proper shaft. Chose herringbone gears, so it meshes better and it prints better than double helical. The motor I chose didn't have rpm or kv rating, but had turns instead. I believe based off some of the other motors I saw that were 550, a 30:1 gear reduction would work well.
    * Created a spreadsheet with inner-outer diameter pattern to create sketch for where each gear needs to sit on gearbox.
        * https://github.com/charlesdengs/Deli_Bot/blob/main/GearSizingForGearBox.txt
<img src="https://github.com/charlesdengs/Deli_Bot/blob/main/Progress%20Photos%20of%20CAD%20and%20Robot/Progress1ofGearbox.png" width="200" />



## Day 3 (July 3, 2023) - Gearboxes
* I have finished a prototype CAD for the gearbox, with a reduction of 27:1. I used a parrallel gearbox, where 2 gears are on the shaft connected, so I could make the gearbox more compact. I used  3, 3:1 gears to make the ratio. The exact teeth count was, 3 sets of 16 teeth to 48 teeth. The gearbox uses a 3/16in shaft, that I'm going to buy from lowes and cut down to the appropiate size, and there are also spacers to keep the gears in line. I saw a video where the shaft for the in between gears didn't rotate, and only the gears did. I liked that idea, so I incorporated it.
    * The gearbox's size makes it so, I can only fit 4 motors inside the bottom chassis, so I will have to stick to 4 wheels instead of 6. This means each motor will need to output more torque, but the toruqe from the gearbox should be more than enough. Will do testing soon.
    * This video was really helpful: https://www.youtube.com/watch?v=VsX_tIuKYB0

<img src="https://github.com/charlesdengs/Deli_Bot/blob/main/Progress%20Photos%20of%20CAD%20and%20Robot/GearboxFullV1.png" width="200" />  <img src="https://github.com/charlesdengs/Deli_Bot/blob/main/Progress%20Photos%20of%20CAD%20and%20Robot/GearBoxAngledV1.png" width="200" /> 
<img src="https://github.com/charlesdengs/Deli_Bot/blob/main/Progress%20Photos%20of%20CAD%20and%20Robot/GearboxTopV1.png" width="200" />
* I'm leaving for the beach tommorrow, so most likely not much work or updates will be out for a few days.