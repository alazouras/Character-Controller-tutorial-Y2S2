# Character-Controller-tutorial-Y2S2
Tutorial for how my character controller system in '3D Blocks...' was made (Year 2 Semester 2)

# 1) Character Controller Script
First, create the Character Controller script (for me titled CharacterController), attach it to the Character object, and implement the following components before Start:

![image](https://user-images.githubusercontent.com/91538155/180002226-cee0f5c6-7290-499c-81e9-12a7ce5288f8.png)

Then, in Start, all we need is to reference the Rigidbody created above, which should be attached to the Character in-game:

![image](https://user-images.githubusercontent.com/91538155/180002391-8dcadf1f-3fc5-479d-b74e-f055105a9968.png)

Next, we have to get the character to move using the keyboard. To do this, first create a private void (I titled it Move) and implement the following code in order to get the character to respond to WASD commands:

![image](https://user-images.githubusercontent.com/91538155/180002717-580293ee-0c4a-411b-93f2-31d667c8d21a.png)

Below that in the void, implement the following two lines in order to get the character to move along the x and y axis:

![image](https://user-images.githubusercontent.com/91538155/180002888-31248751-22ac-468e-ac6d-dd21459985d8.png)

Then, in order to create more fluid movement, implement these last two lines within the void to blend the movement if pressing more than one key and add a smoothness factor:

![image](https://user-images.githubusercontent.com/91538155/180003064-a282bd19-f6b3-4568-b3cb-82ace358cdf4.png)

Finally, aboe the void in Update, call on the Move void like so:

![image](https://user-images.githubusercontent.com/91538155/180003157-5a4a7530-9ac7-444d-b309-3ef3becc5176.png)


# 2) Camera Controller Script
First, create a script titled CameraController (or anything similar to taste) and implement the following variables:

![image](https://user-images.githubusercontent.com/91538155/180000206-1c0e062d-57f1-448f-8184-c09d997eb2fa.png)

In Start, we will need the following components, making sure the main camera is set to first person and is made a child of the character in question:

![image](https://user-images.githubusercontent.com/91538155/180000421-13c46b9c-09c7-4c81-ae94-fa123938d7d6.png)
![image](https://user-images.githubusercontent.com/91538155/180000953-722540a4-8b37-49c8-a8cf-ada33d8c7021.png)

then, in update, we need to set up the mouse movement in order to look around:

![image](https://user-images.githubusercontent.com/91538155/180001209-ddec0c02-3e2b-4812-84b5-b2a9b8828719.png)

The above components are to got the mouse to move how we want it to, and below is how to then get the above components to work with the camera/character, as well as prevent overturning movement:

![image](https://user-images.githubusercontent.com/91538155/180001495-28e039dc-9d3c-4e28-a5c2-3e0a696e0fcf.png)

Finally (for this script) we need to add the following code to get the character to rotate when moving with the keyboard, and get the camera to rotate with the movement of the mouse:

![image](https://user-images.githubusercontent.com/91538155/180001738-6019d71a-d7c6-4546-93ea-fecc66fdefaf.png)


#The Character Setup
All that's left to be needed for the Character Controller package is to apply the following to the character object; the previously referenced Rigidbody with the following settings, as well as a factor for the speed:

![image](https://user-images.githubusercontent.com/91538155/180003659-fddf043f-2a02-477a-86f6-6a65af71292e.png)

For the camera, after adding the Camera Controller script to it, the following settings for smoothing and sensitivity worked best for my project, namely important to keep them the same value if adjusting to personal preference:

![image](https://user-images.githubusercontent.com/91538155/180003906-4e4ea551-433a-4d9d-a0f2-348735bdf267.png)


# And now, you have a working First Person Character/Camera controller!
