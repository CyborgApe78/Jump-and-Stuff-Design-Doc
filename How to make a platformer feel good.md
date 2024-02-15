---
tags:
  - article
---
# _How to make a platformer feel good_

Type: [[Articles]]

----

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