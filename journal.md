### Journal
This project was created from a culmination of short logins and a variation of extended, and brief efforts, Some simple parts may take near months, 
and some complexx parts have been done in a matter of minutes due to fluctuations in concentration and work enviroment. There is no hour-to-dollar ratio, 
so it's not like there's any point in frauding hours anyhow. 
<img width="1318" height="752" alt="image" src="https://github.com/user-attachments/assets/733f8ba0-487a-4d51-88ff-0e059a437c9e" />
please dont overfeed your 3d printer.
## Part 1: The body (5/9/26-5/15/26)
<img width="988" height="1099" alt="image" src="https://github.com/user-attachments/assets/82b6e08e-a01f-4408-82a0-7eea392606cb" />

To begin, this printer is based off an ender 5 plus frame. the extrusions on top were replaced and rotated, along with the front extrusion. 
3MM hot roll steel structural panels were added to increase rigidty, sound insulation, and thermal counterbalancing for the linear rails. 
Extrusions were added on the bottom to serve as mounting points for DIN components, and other components that may need rigid mounting. 
An ACM skidplate was added because of it's durability, affordability, and fire retardance in the event of any mishaps, and to protect  it 
better than plywood or plastic in the event the bottom encounters any damage or impact. Blue spacers with completely locking casters were added to raise the machine, 
and make it easier to transport a heavy machine like this one, without letting it roll away. Handles were added to enable the lifting of the machine (into trucks, or onto tables)
Large vents were added to allow the electronics to breathe, they are flat on one side to enable the cooling of electronics. While they might not have cool geometric patterns like voron vents,
I think they look okay and reinforce the "Form over function" soul of this machine. 
## Part 1.1: Door (5/19/26)
<img width="976" height="1044" alt="image" src="https://github.com/user-attachments/assets/fac31f15-c918-4ec4-af56-e561adb9289a" />
I added a nice robust, and sealed door made with 1515 extrusions as the frame, and handle that pushes the flange seal to trap heat. 

## Part 2: Z-axis (5/19/26-5/25/26)
<img width="803" height="829" alt="Image" src="https://github.com/user-attachments/assets/12f82d21-7cbe-49cb-8c90-e882d33d8822" />
The Z axis is pretty simple. It reuses a large amount of components from the original ender 5 z axis, however it's been modified to fit the new frame, and has a 1kw heating pad to improve heating times, a thermal fuse mounted for safety in the event of an SSR failing (which oftentimes happens in the closed state), and an edge thermistor to compare temperature deltas to monitor the heatsoaking process. Unfortunately, the bed remains the stock steel sheet, as graphite or a cast bed would cost an astronomical amount and the extreme warpage can be compensated with the high-resolution eddy current scanner in this machine. 

## Part 3: CoreXY gantry (5/25/26-6/10/26)
<img width="1358" height="822" alt="Image" src="https://github.com/user-attachments/assets/5b2449ef-d9a3-4a06-82e1-f583193ea62a" />
The corexy gantry was one of the more difficult parts of the design. While based on the monolith gantry, the XY joints, and motor mounts had to be completely redesigned in order to support the new motion system and fit the needs of this machine. The XY joints have modified bump stops to change the endstop position to avoid toolhead collision with Z-axis components, and the motor mounts are redesigned to support a new, relatively unexplored method of control in 3dp. Because this remains relatively uncharted territory, I developed semi-custom servos for this application. I started off with the falcon 500 motor body, as it's incredibly powerful (6000rpm, 4.7nm) at only 12 volts. with an increased voltage, at 24, or even 48 these motors have great response and torque. The controller will be an odrive an an mt6835, and the servo is given a 3:1 reduction before driving the main drive pulley. because of the encoder's 2.1 million positions, this gives the main pulley 6.3 million positions per rotation, or a theoretical (not practical!) gantry resolution of 6.5nm, which is comparable to modern photolithography nodes for cpu/gpu manufacturing. While this number obviously isnt being used, it provides an incredibly high-resolution, low noise value for the PID loop to use, giving it incredible smoothness and response (The shaft will feel as if it's welded in place), benefiting total stiffness within the system (Steppers act like springs in their gantries due to laws of magnetism) and quality. The reduction is tensioned by a sliding, and locking plate that moves the motor. The gantry features double shear, and liveshaft idlers because of the extreme belt tensions required by the 9mm GT2 EPDM belting, which is thicker than standard and is required to handle the extra loads. The X axis is also constructed from a high temperature resistant carbon fiber box tube, which has superior stiffness, while weighing a fraction of the extrusion. The gantry uses a MGN12H rail for X, and MGN9H for Y to provide high strength and reduce wear on the gantry, and a supporting extrusion has been aded to the motor mounting system to improve rigidity and strength. 

## Part 4: Toolhead (6/11/26-6/20/26)
<img width="750" height="984" alt="Image" src="https://github.com/user-attachments/assets/1e6b0499-5f89-40a5-aa57-e10c8acaa47d" />
The toolhead was another fun part to deal with. While it appears to simply be an XOl toolhead on the outside, a deeper dive shows that it's nearly unrecognizable from a design standpoint. The ducts, body, and frame of the toolhead have been completely redone to support the hotend, a lancer meltzone long WITH a meltzone extender to support increased flowrates. The ducts are configured to support a CPAP cooling setup, which at this level is the bare minimum to cool the ducts 