# SO-101 parts list (leader + follower)

Source: official BOM in github.com/TheRobotStudio/SO-ARM100 (checked 18 Sep 2026).
Prices below are the US reference prices from that README. Fill INR prices in orders.md after you find Indian sellers.

## A. Parts to buy

### Servos (12 total, all Feetech STS3215, 7.4 V version)
| Gear ratio | Feetech code | Qty | Goes where |
| --- | --- | --- | --- |
| 1/345 | C001 | 7 | Follower: all 6 joints. Leader: shoulder lift (joint 2) |
| 1/191 | C044 | 2 | Leader: base pan (joint 1) and elbow flex (joint 3) |
| 1/147 | C046 | 3 | Leader: wrist flex (4), wrist roll (5), gripper (6) |

Why different gears on the leader: lower ratio = easier to move by hand, so the leader feels light when you puppet it.
Buy the 7.4 V version, not 12 V. The 12 V version is stronger but the repo says 7.4 V is enough and it matches the 5 V supply below.
Check that the servo listing includes the servo cables and screw bags (they normally do).

### Electronics
| Item | Qty | Note |
| --- | --- | --- |
| Waveshare bus servo driver board (motor control board) | 2 | One per arm. Has a jumper for USB mode on channel B |
| USB-C cable | 2 | Mac to each control board |
| Power supply 5 V (barrel plug for the board) | 2 | One per arm. Check plug size matches the Waveshare board |

### Hardware and tools
| Item | Qty | Note |
| --- | --- | --- |
| Table clamp set (4 pcs) | 1 | Holds both arm bases to the desk |
| Small screwdriver set | 1 | Phillips for M2 and M3 |

### Not in the official BOM, but in our week 1 plan
| Item | Qty | Note |
| --- | --- | --- |
| USB webcam 1080p | 2 | One top view, one side or front view |
| Powered USB hub | 1 | Two cameras and two boards on one Mac mini, powered hub avoids dropouts |
| Phone tripod | 1 | For camera mounting and videos |
| PLA or PLA+ filament | 2 to 3 spools of 1 kg | See print section |
| Small block and a cup | 1 each | The task objects. Pick a block that fits the gripper |

Total US reference for the official BOM items: about USD 230 for both arms.

## B. Parts to 3D print

Files are in the SO-ARM100 repo, STL folder. Print in PLA+ (plain PLA works too), 0.2 mm layers with a 0.4 nozzle, 15% infill, supports everywhere except slopes over 45 degrees. Clean bed first.

The repo gives ready-made plates for a 220 x 220 mm bed (Ender_Follower_SO101.stl, Ender_Leader_SO101.stl). Your Bambu Lab X2D bed is 256 x 256 x 260 mm, so those two plate files fit directly: one plate job per arm. Or load the single parts below into Bambu Studio and arrange them yourself.
X2D notes: single nozzle is enough for the arm. Keep the heated chamber off for PLA. Use AMS-friendly 1 kg spools.

Before printing the arm, print the small gauge files from the repo. They check that the servo fits your printer's tolerance. If the servo does not fit the gauge, adjust the slicer and print the gauge again. Do not print the whole arm first.

### Common parts (print 2 of each, one per arm)
- Base_SO101
- Base_motor_holder_SO101
- Motor_holder_SO101_Base
- Motor_holder_SO101_Wrist
- Under_arm_SO101
- Upper_arm_SO101
- Rotation_Pitch_SO101
- Wrist_Roll_Pitch_SO101
- WaveShare_Mounting_Plate_SO101

### Leader only (print 1 each)
- Handle_SO101
- Trigger_SO101
- Wrist_Roll_SO101

### Follower only (print 1 each)
- Moving_Jaw_SO101
- Wrist_Roll_Follower_SO101

## C. Order of work
1. Order all servos and boards today. Servos are the long pole from India.
2. When the printer arrives: gauge print first, then the follower arm, then the leader.
3. Cameras, hub, tripod are needed in week 2 for teleop. Order now, they are easy to get.
