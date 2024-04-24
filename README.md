# CutDiffusion 
Code release for "CutDiffusion: A Simple, Fast, Cheap, and Strong Diffusion Extrapolation Method" [Paper Link](https://arxiv.org/abs/2404.15141).

## Experiments environment
### Set up the dependencies as:
```
conda create -n CutDiffusion python=3.9
conda activate CutDiffusion
pip install -r requirements.txt
```
## Higher-image generation
```
python cutdiffusion.py --experiment_name="cutdiffusion" \
    --model_ckpt="stabilityai/stable-diffusion-xl-base-1.0" \   # your model ckpt path
    --num_inference_steps=50 \
    --view_batch_size=1 \
    --seed=6 \
    --resolution="2048,2048" \
    --prompt="A corgi sits on a beach chair on a beautiful beach, with palm trees behind, high details." \
    --stride=64 \
    --shuffle 
``` 

## Acknowledgement
We would like to express our profound appreciation and respect towards [MultiDiffusion](https://multidiffusion.github.io/), which has been a significant source of inspiration for our concept. 
Furthermore, our code is heavily influenced by the principles and methodologies established in [DemoFusion](https://ruoyidu.github.io/demofusion/demofusion.html).
