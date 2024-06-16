Controller Mappings:
Refer to [[servo_arm_plan.excalidraw]]

| *Button/Slider Input* | *Function* | 
| ---------- | :--------- | 
| A | +INCREMENT 3y | 
| B | -INCREMENT 3y |
| Y | +INCREMENT 1x |
| X | -INCREMENT 1x |
| LS-X | ADJUST 1x |
| LS-Y | ADJUST 1z |
| RS-X | ADJUST 2z |
| RS-Y | ADJUST 3z |
| LT | CLOSE |
| RT | OPEN |
| DP-U | PRESET Flat |
| DP-D | PRESET Mid |
| DP-L | PRESET Short |
| DP-R | PRESET Tall |

* INCREMENT(Value, Amount):
```
Value += Amount
```

* ADJUST(Value, Stick Dimension)
```
Value+= get(Stick.x)
```

* PRESET(array)
	* Base Array: \[0,0,0,0,0,0\] - Values for each Servo
	* Different Presets will be different 6d vectors
* CLOSE AND OPEN ARE SPECIAL CASES OF PRESET in which the arm is opened and closed
***
### Code for premade functions

**INCREMENT:**
```java
INCREMENT(Servo servo, float amount){
	servo.setPosition()
}
```
