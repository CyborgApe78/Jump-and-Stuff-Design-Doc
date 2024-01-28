---
tags:
  - ability
  - state
  - "#jumps"
aliases:
  - jump
  - jumps
---
# _Jump_

Type: [[Abilities and States]], [[Jumps]]

----


Add force to [[Player]] to [[Jump]] off surfaces. [[Gravity]] is added to player's velocity

[[Jump Consecutive]] 

Code to determine jump force
```gdscript
func calculate_jump_velocity(height: float = jumpHeight, time: float = _jumpTimeToPeak):
	return -sqrt(2 * gravityJump * height)
```

## State Transitions

### Input based

* [[Bash]]
* [[Dash Air]]
* [[Dash Down]]
* [[Dash Up]]
* [[Dive]]
* [[Fall]]
* [[Glide]]
* [[Grapple Hook]]
* [[Ground Pound]]
* [[Wall Grab]]

### Update based

* [[Abilities & States/Bonk]]
* [[Fall]]
* [[Idle]]
* [[Jump Apex]]
* [[Walk]]