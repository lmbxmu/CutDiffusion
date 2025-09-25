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

## Visual results of our CutDiffusion on SDXL (1024×1024) with Ultra-higher resolutions.

### Prompt: a fantasy forest. (4096×4096)

![](assets/a%20fantasy%20forest.png)

### Prompt: A picturesque mountain scene with a clear lake reflecting the surrounding peaks (4096×4096)


![](assets/A%20picturesque%20mountain%20scene%20with%20a%20clear%20lake%20reflecting%20the%20surrounding%20peaks.png)

### Prompt: The vast starry sky. (8192×8192)

![](assets/The%20vast%20starry%20sky.png)



## Acknowledgement
We would like to express our profound appreciation and respect towards [MultiDiffusion](https://multidiffusion.github.io/), which has been a significant source of inspiration for our concept. 
Furthermore, our code is heavily influenced by the principles and methodologies established in [DemoFusion](https://ruoyidu.github.io/demofusion/demofusion.html).
