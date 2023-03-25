# Stable Diffusion
- Cheat Sheet with the most needed stuff..




## Install
- https://rentry.org/voldy

<br>
<br>

1. Clone Stable Diffusion WebUI
```
cd ~/Projects
git clone https://github.com/AUTOMATIC1111/stable-diffusion-webui
```

<br><br>

2. Download Model
- SD 1.5 - https://huggingface.co/runwayml/stable-diffusion-v1-5/resolve/main/v1-5-pruned.ckpt

<br><br>

3. Rename your .ckpt or .safetensors file file to "model.ckpt" or "model.safetensors", and place it in the /models/Stable-diffusionfolder
-You can have as many models as you want in the folder, "model" is just the one it will load by default

<br><br>

4. Install Python 3.10+

<br><br>

5. This reduces VRAM, and allows you to generate at larger resolutions or batch sizes for a <10% loss in raw generation speed
(For me, singular results were slightly slower, but generating with a batch size of 4 made each result 25% faster on average)
This is recommended for most users
- Edit webui-user.sh
```
export COMMANDLINE_ARGS="--medvram --opt-split-attention"
```




6. Launch webui-user.bat, Open it as normal user, not as administrator.

Wait patiently while it installs dependencies and does a first time run.
It may seem "stuck" but it isn't. It may take up to 10-15 minutes.
And you're done!

<br><br>
<br><br>


## Models

<br><br>

### -Deliberate-
- https://civitai.com/api/download/models/5616
  - Powerful All-purpose Model, Stylized Art & Realism Focus
  
<br><br>
  
### -Dreamshaper-
- https://civitai.com/api/download/models/5636
  -Oil Painting-like Portraits, Fantasy art, Scenery

<br><br>

### -AOM3-
- https://civitai.com/api/download/models/11811
  - A fan favorite anime model mix, highly versatile

<br><br>


### -WaifuDiffusion-
- https://huggingface.co/hakurei/waifu-diffusion-v1-4/resolve/main/wd-1-4-anime_e2.ckpt
  - 	A model trained on heaps of Danbooru images
