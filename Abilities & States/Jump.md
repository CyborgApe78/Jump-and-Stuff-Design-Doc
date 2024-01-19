---
tags:
  - ability
  - state
  - "#jumps"
---
# _Jump_

Type: [[Abilities]], [[Jumps]]

----


Add force to [[player]] to [[Jump]] off surfaces. [[Gravity]] is added to player's velocity

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
* [[Dash Up]]
* [[Dash Down]]
* [[Dive]]
* [[Fall]]
* [[Glide]]
* [[Grapple Hook]]
* [[Ground Pound]]
* [[Wall Grab]]

### Update based

* [[Bonk]]
* [[Fall]]
* [[Idle]]
* [[Jump Apex]]
* [[Walk]]