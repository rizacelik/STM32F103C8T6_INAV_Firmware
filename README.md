# INAV 1.7.3 Flight Controller

### Getting Started with STM32F103C8T6
https://www.electronicshub.org/how-to-upload-stm32f103c8t6-usb-bootloader/

![image](https://user-images.githubusercontent.com/19993109/140780448-febede84-03c3-4273-a66f-178484e75ccb.png)


## Download inav_1.7.3_STM32F103C8T6.hex


* Cables for connecting modules
![image](https://user-images.githubusercontent.com/19993109/140774268-1bb3cb9c-603a-4fba-bbcb-0cc5cba95517.png)

* Receicer and Motor, Servo Pin Out

![image](https://user-images.githubusercontent.com/19993109/140774450-e447498e-a044-462c-a7f2-99cccc2b6729.png)

![image](https://user-images.githubusercontent.com/19993109/140774510-0e2ab9ea-3e26-4dfb-a0b3-44394f702c3b.png)

## Frame 

![image](https://user-images.githubusercontent.com/19993109/140774593-b2654240-cabf-4b55-9abf-6fa653c3c14b.png)

# Download INAV configurator

https://github.com/iNavFlight/inav-configurator/releases/tag/2.1.0

### NOTE: It will not work in versions higher than 2.1.0.

## Upload Firmware
* Step 1 and Step 2
![image](https://user-images.githubusercontent.com/19993109/141267643-f8971246-7724-4021-9e5d-1998848587ae.png)

* Step 3 Open Load Firmware file.

![image](https://user-images.githubusercontent.com/19993109/141267858-dd03625d-053d-4b0a-a45d-38c334ea5253.png)

* Step 4, Flash Firmware

![image](https://user-images.githubusercontent.com/19993109/141267945-9cba0dc3-a6b1-4832-b9b9-d05921df7dd7.png)

* Step 5 Bring the BOOT pin back to its original position.

![image](https://user-images.githubusercontent.com/19993109/141268997-cdf3e8ef-b9f4-4aab-9d6f-25ddc8efb2b9.png)

* Step 6 INAV configurator Connect to the development board by clicking the Connect button..

Confirm by clicking the 5” GPS option for GPS support. Save by clicking the blue Save and Rebot button at the bottom right of the window.

![image](https://user-images.githubusercontent.com/19993109/140774708-dd2d429e-9432-4b27-a8c0-24981b8448eb.png)

See or select PPM RX input selected from the Configuration menu. Click the slider button that will activate the GPS. The settings should be as follows. Save by clicking the blue Save and Rebot button at the bottom right of the window.

![image](https://user-images.githubusercontent.com/19993109/140774785-318273c0-2694-4c33-ab01-4be2fbab1ecc.png)

Adjust the GPS setting from the Ports menu. Save by clicking the blue Save and Rebot button at the bottom right of the window.

![image](https://user-images.githubusercontent.com/19993109/140774942-dd042458-c081-41f7-8cc7-373e865bc656.png)

The following options are available in the Configuration menu. Select the model of Quad X or any other vehicle, the setting is as follows. Save by clicking the blue Save and Rebot button at the bottom right of the window.

![image](https://user-images.githubusercontent.com/19993109/140775071-c71d88ec-a4f4-4b77-b577-439d15de7818.png)

Select the accelerometer, gyroscope, compass and barometer of the GY-87 Module from the Configuration menu.

![image](https://user-images.githubusercontent.com/19993109/140775165-6dd3cf4c-7300-4cba-a110-25c946e97eac.png)

After the settings, the sensors will appear as active on the top panel as follows.

![image](https://user-images.githubusercontent.com/19993109/140775286-ecab39b4-f45c-4919-9416-5005c9483d71.png)

Open your ESC and Engine settings in the Configuration menu, it should be as follows.

![image](https://user-images.githubusercontent.com/19993109/140775378-ed299652-a2e0-4636-ada8-d6dd4b41ca3c.png)

Test your remote receiver from the Receiver menu. See incoming signals by playing with channels.

![image](https://user-images.githubusercontent.com/19993109/140775474-36d57210-fe51-4dd5-a172-9ac738bb04ca.png)

Click on the GPS menu to see the map where the GPS gives your location. If the GPS module is started for the first time, it will try to acquire satellites for a long time, about 15 to 20 minutes, so this window may open late. It should also be tested outdoors if possible, or on a window or balcony if not. If no satellite is found indoors, this window will not open again.

![image](https://user-images.githubusercontent.com/19993109/140775570-96ce04d6-c67d-4419-b5c6-3f37a0212855.png)

You can make autonomous flight by marking the coordinates you want on the map with Mission Control from the Mission Control menu. After determining the coordinates, click the blue Save and Rebot button at the bottom right of the last window to save.

![image](https://user-images.githubusercontent.com/19993109/140775651-e7d6c730-d28f-4935-8a1f-19d8def50bec.png)

The task definitions for autonomous flight are made in the Modes Menu.
* NAV ALTHOLD - Altitude hold
* NAV POSHOLD - Hold horizontal position
* NAV KURS HOLD - Fixed Wing Steering
* NAV CRUISE - Fixed Wing Direction + Altitude Hold
* NAV RTH - Back home
* NAV WP - Autonomous waypoint mission
* GCS NAV - Ground control station

Channel CH5 is assigned for ARM and HORIZON. You can assign the channel of the switch buttons on the remote here.

![image](https://user-images.githubusercontent.com/19993109/140775877-b15e975d-7f9e-430e-bec4-666c8d310530.png)

NAV POSHOLD position hold. Always check that POSHOLD is working properly before using RTH or starting a WP task. You can assign the channel of the switch buttons on the remote here. CH6 is used in the example.

![image](https://user-images.githubusercontent.com/19993109/140775955-f6bf9b32-327a-4ac2-9fe8-5e825a9f7a69.png)

It allows us to use automatic navigation features such as NAV RTH and NAV WP Tasks. If the signal from CH7 is at the top, let it return home (NAV RTH), and if it is in the middle, let it fulfill the task that we have determined with the coordinates you want with Mission Control (NAV WP).

![image](https://user-images.githubusercontent.com/19993109/140776018-bfea642e-a234-483e-b52c-453ff45e17a6.png)

We can set the flight route according to the coordinates in the Mission Control Menu. Select the first location by clicking on a desired location on the map, the blue icon will appear, click on it and the location information will appear as shown on the side. In the meantime, we enter the height in cm where it says Alt (cm). You should also enter the speed in cm in the area written (cm/s) at the bottom. For example, 100 cm means that it will gain speed of 1 meter per second. Then we save the first position by clicking the Save button, then you can select the second, third, etc. targets in a similar way and enter their heights and speeds in different ways. These set coordinates will be realized with the NAV WP task above. This task occurs when you bring the switch of the CH7 channel on the remote to the middle.

![image](https://user-images.githubusercontent.com/19993109/140776106-90a1d7d4-4e91-4075-9def-c4ddd1239c86.png)

In the Failsafe menu, we set what to do when there is a problem or the drone is out of range, out of range. DROP drop, Land auto land, RTH return home are options.

![image](https://user-images.githubusercontent.com/19993109/140776208-7252c0d7-4803-47c3-ab3b-5e6bc279723b.png)



You can read about navigation mods
https://github.com/iNavFlight/inav/wiki/Navigation-modes





