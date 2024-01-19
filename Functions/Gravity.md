```gdscript
func calculate_gravity(height: float = jumpHeight, time: float = _jumpTimeToPeak):
	return (2.0 * height) / pow(time, 2) 
```