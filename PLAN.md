# 90-day plan (short version)


## Build 1: SO-101 arm with LeRobot (days 1 to 30, Sep 18 to Oct 17)
Done when: the arm picks a block and drops it in a cup 14 times out of 20, and the repo and video are public.
- Week 1: orders, Mac setup, LeRobot install, one simulation training run on Colab, MuJoCo, repo, first X post.
- Week 2: assemble, calibrate, teleoperate, fix cameras in place.
- Week 3: record 50 episodes, train ACT on Colab, run on arm, 20-trial test. Order build 2 parts by end of this week.
- Week 4: break tests, fixes, README, YouTube video 1, day 30 review.
If servos are late: do ROS 2 basics (week 5) and the Reachy Mini teardown first, then come back.

## Build 2: Wheeled robot with ROS 2 (days 31 to 60, Oct 18 to Nov 16)
Done when: the robot maps the flat and drives to a point on the map by itself.
Parts: Raspberry Pi 5 (8 GB), SD card, cooler, 2-wheel chassis, 2 DC motors with encoders, motor driver, 2D lidar, battery with 5 V step-down.
- Week 5: ROS 2 basics in UTM, Pi setup.
- Week 6: assemble and drive by keyboard, Foxglove. Order duck parts.
- Week 7: lidar, SLAM, Nav2.
- Week 8: Fusion 360 mount, break tests, README, YouTube video 2, day 60 review.

## Build 3: Duck robot v0 (days 61 to 90, Nov 17 to Dec 21)
Done when: an existing open-source duck (such as Open Duck Mini) is assembled, standing and walking with its reference software.
- Week 9: study docs, MuJoCo sim, tear down one companion robot.
- Week 10: print and assemble.
- Week 11: stand and walk.
- Week 12: break, fix, README, YouTube video 3, first pull request from upstream-bugs.md.
- Week 13: day 90 review, and the list "what I would change to make this a kit".

## Scoreboard for day 90
| Number | Target |
| --- | --- |
| Builds finished | 3 |
| Public repos with full README | 3 |
| YouTube videos | 3 |
| Weekly X posts | 13 |
| Real conversations with builders | 25 or more |
| Pull requests opened | 1 |
