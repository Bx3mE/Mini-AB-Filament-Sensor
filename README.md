# Filament sensor for Dragon Mini AB
Queria crear un sensor de filamento dentro toolhead para revisar si se acaba el filamento o si hay un clog en el extrusor. Probado en Dragon normal flow, no se ha probado en Dragonfly, pero deberia funcionar.

# BOM
## For both (before and after the extruder's gears)
- [2x digital hall sensor](http://aliexpress.com/item/32312432947.html), it doesn't matter if it's [latching or not latching](https://maker.pro/arduino/tutorial/how-to-use-a-hall-effect-sensor-with-arduino). I'm using U18
- [7x 4mm ball bearings](http://www.aliexpress.com/item/1005002383413769.html)
- [4x 5mm x 3mm Round Neodymium Magnets](https://www.aliexpress.com/item/1005002226737225.html)
- 2x 10k ohm resistor
- [Thin wires, 32 AWG recommended](https://www.aliexpress.com/item/32882386535.html)

## BOM If you only want a sensor before the gears:
- 1x Digital hall sensor
- 1x ball bearing
- 2x Magnets
- 1x resistor
- Thin wires

## BOM If you only want a sensor before the gears:
- 1x Digital hall sensor
- 6x ball bearings
- 2x Magnets
- 1x resistor
- Thin wires

## Tools needed
- Multimeter

# Printed parts
- _Mid_Body.stl_ - Needed
- Recommended to print 2 copies of every hall sensor holder
- _Cowling_Dragon.stl_ - Not needed at all, but print it if you don't want to sand it down (step 12)

# Instructions
![Cut2](https://user-images.githubusercontent.com/67475249/132077526-349f1146-a096-41ef-b85d-1fae97070d25.png)
1. Insert 6 balls in **1**
2. Insert magnet in **1**
3. Make sure that magnet is around 2mm down the tunnel, if not, then push it using filament or something similar
4. Test your clearances by inserthing filament, when there is no filament the magnet should be 2mm down the tunnel and when the filament is loaded the magnet, should raise up about 2mm



![Filament loaded](https://user-images.githubusercontent.com/67475249/132095333-1b69d459-0445-4db0-bcaa-d3d98d68a5bc.PNG)
![Untitled](https://user-images.githubusercontent.com/67475249/132095385-33e1fe7b-fb2e-4527-8164-fc9859a71c98.png)




6. Insert a magnet in **3**, it should repel the magnet in **1**. If you inserted it in the wrong orientation use an 1.5 or 2mm drill bit to remove it out of the hole
7. Prepare hall sensor, solder resistor at least 10 cm from the sensor

 ![u18](https://user-images.githubusercontent.com/67475249/132078144-125efee8-cbf2-4fad-b4a4-a07cc85edf7b.PNG)
 
7. Test your circuit, move the hall sensor towards both magnets and check with a multimeter, it should read 5v or 0v when they are close and 0v or 5v if they aren't 
8. Insert the hall sensor in HallSensorHolder145-145.stl, then insert the holder with the sensor in **2** (small face of sensor pointing towards **3**). **DO NOT** force it yet

10. Load and unload filament and check with a multimeter if there is any variation, if the voltage doesn't change, rotate hall sensor and repeat
   * if everything is working, push the hallsensor holder in place
   * if it's not working, remove it and try with a different sensor holder, then repeat
   
11. Repeat steps 1-9 for sensor before extruder gears, but insert only 1 ball in **4**
12. Bend pins in both hall sensors, nothing can be taller than the highlighted part in the picture. Hot glue could be needed

![Capture](https://user-images.githubusercontent.com/67475249/132079892-3765e3a6-2719-4336-a23c-b147f8357271.PNG)

12. Route the cables. In the black circle in the second picture can be seen what needs to be sanded. If you dont want to sand, print _Cowling_Dragon.stl_


![Cable path](https://user-images.githubusercontent.com/67475249/132078872-913ee597-7d4d-4c8c-8d2f-637c7ced4135.jpeg)
![file](https://user-images.githubusercontent.com/67475249/132079048-aeaa3e7a-c9e1-4481-bddb-add37ee8c292.PNG)

13. Choose any pin available in your board and connect the wires. RX2 and TX2 are recommended because they are next to each other and GND +5V. See _TestCode.txt_
 
 ![skr e3 2 0](https://user-images.githubusercontent.com/67475249/132079748-d0abf244-5354-479a-8e0c-bf18af6764ff.png)

# Photos
![Mid Body](https://user-images.githubusercontent.com/67475249/131930646-4e525b9a-e959-4d66-a8ba-3105bf5979fa.png)
![Final](https://user-images.githubusercontent.com/67475249/131932295-15f4ab81-08fd-4978-9525-03dfe47383a3.jpeg)
![Final 2](https://user-images.githubusercontent.com/67475249/131932313-80a32543-3dc1-4280-85ae-4797c5f7eb73.jpeg)
![Cut](https://user-images.githubusercontent.com/67475249/131930642-4eed7b00-6c50-4ca0-8c28-58445fdcd040.png)
