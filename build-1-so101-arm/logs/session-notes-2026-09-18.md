# Session notes, 2026-09-18 (Day 1)

- Did: checked the Mac. Homebrew, cmake and ffmpeg were already there. Installed Miniforge (conda 26.7.2) via Homebrew.
- Did: created conda env `lerobot` (Python 3.12) and installed LeRobot with extras core_scripts, training, feetech, pusht, plus MuJoCo. Followed the official install guide at huggingface.co/docs/lerobot/installation.
- Broke: TorchCodec failed to load. conda gave ffmpeg 9.0.1, TorchCodec supports 4 to 8. Fixed by pinning ffmpeg=7.1.1. Row added to fix-log.md and upstream-bugs.md.
- Verified: lerobot 0.6.1, torch 2.11.0 with MPS, torchcodec 0.11.1, mujoco 3.13.0, gym-pusht, feetech SDK. CLI tools lerobot-find-port, lerobot-calibrate, lerobot-record, lerobot-train are on the path inside the env.
- Next: orders (Day 1 list), GitHub/HF/Colab accounts, Discord (Day 2), repo + first X post (Day 3).
