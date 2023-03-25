# Stable Diffusion Cheat Sheet
- Cheat Sheet with the most needed stuff..

<br><br>

## Hardware

<br><br>

### Google Cloud VM

#### safetensors-Modell
Um ein .safetensors-Modell in Google Cloud zu nutzen, benötigen Sie eine VM-Instanz mit einer NVIDIA-GPU und einer entsprechenden CUDA-Version. Die genaue Konfiguration hängt jedoch von der Größe des Modells, der Größe der Daten, der Anzahl der Schritte usw. ab, die für die Ausführung des Modells erforderlich sind.

Eine gute Option für die Verwendung von .safetensors-Modellen in Google Cloud ist die Verwendung einer VM-Instanz mit einer NVIDIA Tesla T4-GPU. Die Tesla T4 ist eine leistungsstarke GPU, die speziell für Machine-Learning-Aufgaben entwickelt wurde und eine gute Wahl für die Beschleunigung von Deep-Learning-Workloads darstellt. Die T4 ist auch eine relativ kosteneffektive Option und bietet ein gutes Verhältnis von Preis zu Leistung.

In Bezug auf die VM-Instanztypen bietet Google Cloud eine Vielzahl von Optionen, darunter die N1- und C2-Serie. Für kleinere Modelle können Sie eine Instanz der N1-Serie in Betracht ziehen, die über eine NVIDIA T4-GPU verfügt. Für größere Modelle oder wenn Sie eine höhere Leistung benötigen, können Sie eine Instanz der C2-Serie in Betracht ziehen, die über eine NVIDIA A100-GPU verfügt.

Beachten Sie jedoch, dass diese GPU-beschleunigten Instanzen höhere Preise als Standard-VMs haben können. Sie sollten die Preise sorgfältig überprüfen, um sicherzustellen, dass Sie die geeignete Größe der Instanz für Ihr Budget auswählen.

In Bezug auf die CUDA-Version sollten Sie sicherstellen, dass die auf Ihrer VM-Instanz installierte CUDA-Version mit der CUDA-Version kompatibel ist, auf der das .safetensors-Modell trainiert wurde. Sie können dies tun, indem Sie die Dokumentation des Modells überprüfen oder den Entwickler des Modells kontaktieren, um die entsprechende CUDA-Version zu erfahren.

Eine gängige Option für die Verwendung von NVIDIA-Tesla-GPUs in Google Cloud ist die Verwendung von Deep Learning VMs, die speziell für Machine-Learning-Workloads optimiert sind und die erforderlichen Softwarekomponenten vorinstalliert haben, einschließlich TensorFlow, PyTorch und anderen Bibliotheken. Sie können eine Deep Learning VM mit einer Tesla T4-GPU oder einer A100-GPU auswählen und die Größe der Instanz an Ihre Anforderungen anpassen.
















# Install

<br><br>


## CUDA

<br><br>


### Ubuntu
1. Make sure that you use the latest driver for your graphiccard

You can find a list of nvidia driver here and check there if your graphiccard is supported
https://wiki.ubuntuusers.de/Grafikkarten/Nvidia/nvidia/


#### Gtx 1050 ti
```
sudo apt-get purge 'nvidia*'
sudo add-apt-repository ppa:graphics-drivers/ppa
sudo apt-get update
sudo apt-get install nvidia-driver-525 nvidia-settings
reboot
```

2. Install CUDA
```
sudo apt-get install cuda
reboot
```

















<br><br>
<br><br>
__________________________________________________________
__________________________________________________________

<br><br>
<br><br>



## WEB UI
- https://github.com/AUTOMATIC1111/stable-diffusion-webui

### Install
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


### Download
- https://civitai.com


<br><br>
<br><br>

#### Photogaphy

<br><br>

##### OrangeChillMix
- https://civitai.com/models/9486/orangechillmix


<br><br>

### Realistic Vision V1.3
- https://civitai.com/models/4201/realistic-vision-v13

<br><br>

#### -Deliberate-
- https://civitai.com/api/download/models/5616
  - Powerful All-purpose Model, Stylized Art & Realism Focus
  
<br><br>
  
### -Dreamshaper-
- https://civitai.com/api/download/models/5636
  -Oil Painting-like Portraits, Fantasy art, Scenery

<br><br>

#### -AOM3-
- https://civitai.com/api/download/models/11811
  - A fan favorite anime model mix, highly versatile

<br><br>


#### -WaifuDiffusion-
- https://huggingface.co/hakurei/waifu-diffusion-v1-4/resolve/main/wd-1-4-anime_e2.ckpt
  - 	A model trained on heaps of Danbooru images
