# OpenCS2 Dataset

![OpenCS2 Dataset — 10 tick-aligned player POVs, inputs, world state, and audio, built from professional HLTV demos.](https://huggingface.co/datasets/blanchon/opencs2_dataset/resolve/main/static/header.webp)

<p align="center">
  <a href="https://huggingface.co/spaces/blanchon/opencs2-dataset-viewer"><b>🎯 Open the Viewer</b></a> ·
  <a href="https://huggingface.co/datasets/blanchon/opencs2_dataset">Dataset</a> ·
  <a href="https://huggingface.co/datasets/blanchon/opencs2_dataset_wds">WebDataset</a> ·
  <a href="https://huggingface.co/datasets/blanchon/opencs2_dataset_demo">Raw demos</a> ·
  <a href="https://huggingface.co/collections/blanchon/opencs2">Collection</a>
</p>

A rendered Counter-Strike 2 dataset built from professional HLTV demos: every round is replayed
from all 10 player perspectives, with video, spatial audio, inputs and world state aligned on the
same tick clock.

**[Browse it in the viewer →](https://huggingface.co/spaces/blanchon/opencs2-dataset-viewer)**
every match, map and round, with all 10 player POVs synced on one timeline, right in your browser.

## What's inside

Per player, per round:

- **Video**: 1280×720 @ 32 fps, near-lossless H.264
- **Audio**: per-player stereo, mixed from that player's position and orientation
- **Inputs**: every tick: keys, mouse delta, view angles, fire/jump/use, weapon switches
- **World state**: every tick: position, velocity, view, health, armor, weapon, alive flag
- **Events**: kills, duels, clutches, round outcomes, match metadata

Current build: **165,270 POV rounds** (~2,974 hours of POV video) across 16,527 rounds and
794 pro match/maps.

## Datasets

| Repo | Description |
| --- | --- |
| [`blanchon/opencs2_dataset`](https://huggingface.co/datasets/blanchon/opencs2_dataset) | POV renders, loose-file layout with parquet indexes and event tables |
| [`blanchon/opencs2_dataset_wds`](https://huggingface.co/datasets/blanchon/opencs2_dataset_wds) | Same data packaged as WebDataset tar shards for large-scale training |
| [`blanchon/opencs2_dataset_demo`](https://huggingface.co/datasets/blanchon/opencs2_dataset_demo) | Source HLTV `.dem` files with per-map metadata and analysis |
| [`opencs2-dataset-viewer`](https://huggingface.co/spaces/blanchon/opencs2-dataset-viewer) | Browser-based viewer for the whole dataset |

Usage examples, schemas and loading code live in each dataset card on Hugging Face.

## Source code

The generation and rendering pipeline is not published. This repository only serves as a home
page for the project.

## Citation

```bibtex
@misc{blanchon2026opencs2,
  author       = {Julien Blanchon},
  title        = {OpenCS2 Dataset},
  year         = {2026},
  publisher    = {Hugging Face},
  howpublished = {\url{https://github.com/julien-blanchon/opencs2-dataset}},
}
```

## License

Dataset: [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/).

Counter-Strike 2 is a trademark of Valve Corporation. This project is not affiliated with or
endorsed by Valve.
