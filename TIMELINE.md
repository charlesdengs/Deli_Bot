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
* Did research on how ESCs communicate with Arduino and how to pick one out. This was helpful: (https://maker.pro/custom/tutorial/how-to-select-motor-controllers-for-big-motors) It came with a spreadsheet of different ESCs, current ratings, and motor styles.
* Picked the Hobbywing 1060 ESC, since it was cheap, met my amp requirements, and could fit a 3S lipo.
* Printed out version 1 of the wheel, it was incredibly heavy, so I'm going to go back and try and work that out. I still want to use a rigid wheel, unlike some of the softer wheels on some rovers.
<img src="https://github.com/charlesdengs/Deli_Bot/blob/main/Progress%20Photos%20of%20CAD%20and%20Robot/NewWheels.png" width="200" />

* Researched different gearboxes, and chose double geartrain because it is compact and not complicated.
* Worked on gearbox, and created variables for shaft diameter, in case I can't find a proper shaft. Chose herringbone gears, so it meshes better and it prints better than double helical. The motor I chose didn't have rpm or kv rating but had turns instead. I believe based on some of the other motors I saw that were 550, a 30:1 gear reduction would work well.
    * Created a spreadsheet with an inner-outer diameter pattern to create a sketch for where each gear needs to sit on the gearbox.
        * https://github.com/charlesdengs/Deli_Bot/blob/main/GearSizingForGearBox.txt
<img src="https://github.com/charlesdengs/Deli_Bot/blob/main/Progress%20Photos%20of%20CAD%20and%20Robot/Progress1ofGearbox.png" width="200" />



## Day 3 (July 3, 2023) - Gearboxes
* I have finished a prototype CAD for the gearbox, with a reduction of 27:1. I used a parallel gearbox, where 2 gears are on the shaft connected, so I could make the gearbox more compact. I used  3, 3:1 gears to make the ratio. The exact teeth count was 3 sets of 16 teeth to 48 teeth. The gearbox uses a 3/16in shaft, that I'm going to buy from lowes and cut down to the appropriate size, and there are also spacers to keep the gears in line. I saw a video where the shaft for the in-between gears didn't rotate, and only the gears did. I liked that idea, so I incorporated it.
    * The gearbox's size makes it so, I can only fit 4 motors inside the bottom chassis, so I will have to stick to 4 wheels instead of 6. This means each motor will need to output more torque, but the torque from the gearbox should be more than enough. Will do testing soon.
    * This video was really helpful: https://www.youtube.com/watch?v=VsX_tIuKYB0

<img src="https://github.com/charlesdengs/Deli_Bot/blob/main/Progress%20Photos%20of%20CAD%20and%20Robot/GearboxFullV1.png" width="200" />  <img src="https://github.com/charlesdengs/Deli_Bot/blob/main/Progress%20Photos%20of%20CAD%20and%20Robot/GearBoxAngledV1.png" width="200" /> 
<img src="https://github.com/charlesdengs/Deli_Bot/blob/main/Progress%20Photos%20of%20CAD%20and%20Robot/GearboxTopV1.png" width="200" />

* I'm leaving for the beach tomorrow, so most likely not much work or updates will be out for a few days.

## Day 4 (July 7, 2023) - Printing and Issues

* Got back from Folly Beach, SC today, that was really cool. Fun place to be, learned how to surf.
* I'm beginning to print out some of the preliminary parts of the gearbox to test tolerances.
* I'm having an issue with Fusion 360 where all the actions in the timeline keep messing up when I change anything. Trying to figure it out, I might just copy the file and paste it and make a new one.
<img src="https://github.com/charlesdengs/Deli_Bot/blob/main/Progress%20Photos%20of%20CAD%20and%20Robot/WeirdTimeLineErrors.png" width="200" />

* I also reorganized the bot chassis to fit the 4 gearboxes, their arrangement, and larger tires so the bottom of the chassis doesn't hit anything.
<img src="https://github.com/charlesdengs/Deli_Bot/blob/main/Progress%20Photos%20of%20CAD%20and%20Robot/BottomChassisV2.png" width="200" />
<img src="https://github.com/charlesdengs/Deli_Bot/blob/main/Progress%20Photos%20of%20CAD%20and%20Robot/Motorspacing.png" width="200" />


## Day 5 (July 13, 2023) - Testing Gearboxes and Reorganizing

* I fixed the issues with the gearbox F360 file by going back in the timeline and readjusting the sketches one by one. It seems like it accidentally projected too many faces, so the extrusion go overwhelmed. I resolved this by removing those extra faces.

* I also designed a sensor/camera tray on the top chassis where I could include ultrasonic sensors and cameras for view. The only issue with the tray is that it takes up space inside the storage unit, but other robots I saw, tend to do the same, so I think for the space underneath the camera tray, I might add trays or pullout tabs for more storage.
<img src="https://github.com/charlesdengs/Deli_Bot/blob/main/Progress%20Photos%20of%20CAD%20and%20Robot/NewCameraHousing.png" width="200" />
<img src="https://github.com/charlesdengs/Deli_Bot/blob/main/Progress%20Photos%20of%20CAD%20and%20Robot/CameraHousingInside.png" width="200" />

* I finished printing out the gearbox, I'm still waiting on a package with the ESCs, and bearings to finish the gearbox. But with just the 1:9 gear ratio, it is working out really well. The gearbox is really loud, however, but lubrication and the top casing should help block out some of the noise.

* My plans now are to get the ESCs set up with the motors once they arrive, and begin testing code, since a lot of the remaining prints will be the rest of the gearboxes, and the larger prints of the chassis'.
