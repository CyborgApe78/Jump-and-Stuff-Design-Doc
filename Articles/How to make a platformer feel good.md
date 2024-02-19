---
tags:
  - article
---
# _How to make a platformer feel good_

Type: [[Articles]]

----

### Coyote Time

Jump after leaving ground
also useful for wall jump

### Jump Buffer

### Half Gravity at Apex

### Corner Correction

### Extended wall detection for wall jumps

###  Variable Jump Height

### Faster at apex

### Clamp Fall Speed


Basic feel goods to add
	Sticky feet on land
		Will need accel and decel first
		Quick stop when landing if input is opposite of move direction
	Push up through a semisolid 
		Make a collision box that detects it is in a semisolid (and still holding jump) and put player on top of platform
		Could use for multiple abilities like dash
	If the joystick is slightly pushed, don’t go over edges
	Add platform momentum to character (looks like godot 4 does that)
	Extend wall detection when trying to use abilities
		You can actually wall jump 2 pixels from a wall. (That sounds tiny but this is a 320x180-resolution game :P)
		If you're doing a "super wall jump" (ie: a wall jump while dashing upward), this is a more precise and demanding maneuver so we let you do it from even further away (I think it's 5 pixels, which is more than half a tile!)
	Wall ability control
		different jump if holding up
		jump/dash way from wall

Adjust air control
Be a bit different than ground 
​​What I usually do is treat mid air horizontal velocity change as interpolation from the current velocity to the player's desired velocity. Godot has a built in lerp function that's helpful for this. You would do something like current_hvel.lerp(input_hvel, arbitrary_fraction × delta). Hvel stands for Horizontal velocity. That arbitrary fraction will make the jump feel weightier at lower values. 0 will make it impossible to move in the air.
With this method you will infinitely approach the goal velocity, but technically never actually reach it. To solve that, just clamp it at the end to the desired velocity if the difference between the current and desired is small enough.
SMW actually has a lot of hidden mechanics, while it might look to be a very standart movement it has some neat details
SMW does a neat trick to change the jump height
The height is varied by lowering the "force" that moves you down when you press the nump button
(Which results in an interestingly dynamic way of changing your jump height, as well as allowing to change your fall speed by holding the jump button pressed)
(Barely any game does its jump like that anymore, but I adore it cause of how great it feels when you know it and play some Kaizo)
