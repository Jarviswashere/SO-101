# SO-101 print plan: folder, file, colour, quantity

Folder: SO-ARM100-main/STL/
Scheme: white body, orange ends. Same scheme for every arm you print later.
Settings: PLA, 0.20 mm, 15% infill, tree supports, 45 deg threshold. Chamber off.

## Gauges/  (print first, white, 1 each)
| File | Colour | Qty | Note |
| --- | --- | --- | --- |
| Gauge_0.STL | White | 1 | Servo fit test, normal tolerance |
| Gauge_tight_1.STL | White | 1 | Servo fit test, tight tolerance. Print both, see which fits snug |
| Lego_Size_Test_02_zero.STL | skip | 0 | Lego test, not needed |
| Lego_Size_Test_02_minuspoint1.STL | skip | 0 | Lego test, not needed |

## SO101/Individual/  (this is the folder you print from)
Qty is for 2 arms (1 follower + 1 leader). For 4 arms, double it.

### White
| File | Qty | Used on |
| --- | --- | --- |
| Base_SO101.stl | 2 | both |
| Base_motor_holder_SO101.stl | 2 | both |
| Motor_holder_SO101_Base.stl | 2 | both |
| Motor_holder_SO101_Wrist.stl | 2 | both |
| Under_arm_SO101.stl | 2 | both |
| Upper_arm_SO101.stl | 2 | both |
| Rotation_Pitch_SO101.stl | 2 | both |
| Wrist_Roll_Pitch_SO101.stl | 2 | both |
| WaveShare_Mounting_Plate_SO101.stl | 2 | both, holds the Waveshare board |

### Orange
| File | Qty | Used on |
| --- | --- | --- |
| Moving_Jaw_SO101.stl | 1 | follower gripper |
| Wrist_Roll_Follower_SO101.stl | 1 | follower gripper |
| Handle_SO101.stl | 1 | leader grip |
| Trigger_SO101.stl | 1 | leader grip |
| Wrist_Roll_SO101.stl | 1 | leader grip |

### Skip
| File | Why |
| --- | --- |
| SO101 Assembly.stl | Whole arm in one piece, for viewing only |
| Seeedstudio_Mounting_Plate_SO101.stl | For the Seeed board. You have Waveshare |

## SO101/Follower/ and SO101/Leader/  (skip)
Ender_, Prusa_, BambuLabA1mini_ files are pre-arranged single-colour plates. Not used, because we split colours.

## SO100/  (skip entirely)
Old arm version. Do not print anything from here.

## Print order
1. Gauges, white. Check with a servo when servos arrive, or keep for later.
2. Plate A: white follower set (9 parts). Overnight.
3. Plate B: orange parts, all 5. Short job.
4. Assemble follower when servos arrive.
5. Plate C: white leader set (9 parts). Overnight.

## Update 21 Sep: use the plate files, not Individual/
Individual STLs load in design orientation (measured: Upper_arm 67 mm tall on 86 mm2 of contact vs 24 mm tall on 3963 mm2 in the plate file). Printing them as loaded fails.
Instead: import SO101/Follower/Ender_Follower_SO101.stl or SO101/Leader/Ender_Leader_SO101.stl, click Yes, right-click, Split to Objects, delete the parts you do not want, then arrange.
- Follower plate = 9 white + Moving_Jaw + Wrist_Roll_Follower (orange).
- Leader plate = 9 white + Handle + Trigger + Wrist_Roll (orange).
Settings that work: 0.20 mm Standard, tree support 45 deg, brim outer only 5 mm (needed for Rotation_Pitch and Wrist_Roll_Pitch, tiny bed contact).
Individual/ is for identifying shapes only.
