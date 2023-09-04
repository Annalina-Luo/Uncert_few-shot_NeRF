# Uncert_few-shot_NeRF


Neural Radiance Fields is a method that achieves state-of-the-art results for synthesizing novel views of complex scenes. However, it performs bad when limited inputs are available and ignores the importance of uncertainty estimation.

This project aims to quantify both aleatoric and epistemic uncertainties within few-shot NeRF, while preserving the fidelity of images derived from novel viewpoints.

## Installation

```
pip install -r requirements.txt
```

<details>
  <summary> Dependencies (click to expand) </summary>
  
  ## Dependencies
  - PyTorch 1.4
  - matplotlib
  - numpy
  - imageio
  - imageio-ffmpeg
  - configargparse
  
The LLFF data loader requires ImageMagick.

You will also need the [LLFF code](http://github.com/fyusion/llff) (and COLMAP) set up to compute poses if you want to run on your own real data.
  
</details>

## How To Run?

### Quick Start

Download data for two example datasets: `lego` and `fern`
```
bash download_example_data.sh
```

To train a low-res `lego` NeRF:
```
python run_nerf.py --config configs/lego.txt
```

---

To train a low-res `fern` NeRF:
```
python run_nerf.py --config configs/fern.txt
```
---
