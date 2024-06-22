# Making-a-self-balancing-robot-with-stepper-motor-arduino-nano-and-bluetooth-control
I made a model of self balancing robot on stepper motor, arduino nano, cnc shield, bluetooth control.
First of all, I did not write this code, I borrowed from this channel: https://www.youtube.com/@PhamThanhKhuyen (thanks a lot to this man). I have redesigned the model and change the controller values to fit on my robot.
Things to prepare: 1 arduino nano, 2 drv8825 or A4988 (this 2 things have to be tuned Vref later), 1 arduino cnc shield V4, 3 cells battery 18650 (I choosed the pink one with 2600 mAh) ,DC cable 5.5 mm type ,1 switch, 1 mpu6050, 1 bluetooth module HM10 4.0, 2 stepper motor 42x42x35 (800mA per phase),2 wheels; wires and screws.
3D files I have redesigned and maybe post it later on thingsverse.
On the back side of cnc shield (Y and Z axis) , weld MS1 and MS2 pin together, then connect to VMOT pin. This means setting to 1/8 microstepping control with drv8825. To do the same with A4988, please find the control microstepping mode for it.
Indicate the phase A B of your stepper motors then connect them to driver. Becareful this step, wrong wiring can cause operation noisy, heat, and strong vibration. Use multimeter to tune VREF on your driver until the motors works smoothly, no heating or just warm. (I recommend warm is ok, this means the electromagnetic force is strong enough; in case you need a formula: VREF=(2*Imaxperphase)*0.8 *0.5=0.68 for this motor)
Wrap everything together. Finally tune your PID controller for the best performing.
![result](https://github.com/Triplehittrick/Making-a-self-balancing-robot-with-stepper-motor-arduino-nano-and-bluetooth-control/assets/172620782/ee6f5c46-28d9-49dc-b044-18642b2d99c0)
