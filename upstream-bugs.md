# Upstream bugs

Bugs or confusing docs found in open-source projects while building. One of these becomes my first pull request in week 12.

| Date | Project | What happened | How to reproduce | My fix or workaround | Issue or PR link |
| --- | --- | --- | --- | --- | --- |
| 2026-09-18 | huggingface/lerobot (docs) | Install guide says `conda install ffmpeg -c conda-forge` "usually installs ffmpeg 8.X". On 2026-09-18 it installed ffmpeg 9.0.1. TorchCodec 0.11.1 supports ffmpeg 4 to 8, so video decoding fails to load on a fresh install. | macOS 26.5 Apple Silicon, Miniforge, `conda create -n lerobot python=3.12`, `conda install ffmpeg -c conda-forge`, `pip install 'lerobot[core_scripts]'`, then `python -c "import torchcodec"`. | `conda install ffmpeg=7.1.1 -c conda-forge`. Possible docs PR: pin a supported version (for example `ffmpeg<9`) in the main command, not only in the tip. Check first if an issue already exists. | |
| 2026-09-24 | huggingface/notebooks (lerobot/training-act.ipynb) | Install cell runs `pip install -e ".[train, dataset]"` but the extra in lerobot's pyproject.toml is named `training`, not `train`. pip warns the extra does not exist and skips it. The notebook also does not install any sim env, so `--env.type` eval fails. | Open the Colab notebook, run cell 1, read the pip warning. Check pyproject.toml optional-dependencies. | Use `pip install -e ".[training,pusht]"`. Possible PR: fix the extra name in the notebook. | |
