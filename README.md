# LIVE- Towards Layer-wise Image Vectorization (CVPR 2022 Oral)

| [[arXiv]]() |[[Colab]]()|[[HuggingFace Space]]()| Primary contact: [[Xu Ma]](mailto:ma.xu1@northeastern.edu)
<div align="center">
    <img src="images/teaser.png" width="70%">
</div>
We present a new method to progressively generate a SVG that fits the raster image in a layer-wise fashion. Given an arbitrary input image, LIVE recursively learns the visual concepts by adding new optimizable closed bezier paths and optimizing all these paths.


### Updated for rebuttal (Jan/28/2022)： 
#### User study
We create a [user study](https://wj.qq.com/s2/9665341/19ed) as suggested. A more complex user study will be added in the revised version.

The results are collected here: [user study details](user_study_state.csv)

#### Code installation

we added  detailed [conda env file](env.yml) and collected detail [system information](system_info.txt) to help the installation.

A more detailed docker and Google Colab demo will be provided.

<div align="center">
    <img src="images/smile.png" width="150px" height="150px" alt="Elephant at sunset">
    <img src="images/out_diffvg4.gif" width="150px" height="150px" alt="Elephant at sunset">
    <img src="images/out_diffvg256.gif" width="150px" height="150px" alt="Elephant at sunset">
    <img src="images/live-smile.gif" width="150px" height="150px" alt="Elephant at sunset">
</div>
<div align="center">
    <div style="width=150px; height=20px;display:inline;">Input Raster Image</div>
    <div style="width=150px; height=20px;display:inline;">DiffVG (4 paths)</div>
    <div style="width=150px; height=20px;display:inline;">DiffVG (256 paths)</div>
    <div style="width=150px; height=20px;display:inline;">LIVE (4 paths)</div>
</div>

<div align="center">
  <img src="example.png" width="650px" height="300px">
</div>
LIVE is able to explicitly presents a Layer-wise representation for simple images. 

## Installation
```bash
pip3 install torch torchvision
pip install svgwrite
pip install svgpathtools
pip install cssutils
pip install numba
pip install torch-tools
pip install visdom
pip install scikit-fmm
pip install opencv-python==4.5.4.60 
pip install easydict
pip install scikit-fmm

```
Next, please refer DiffVG to install [pydiffvg](https://github.com/BachiLi/diffvg)


## Run
```bash
python main.py --config config/all.yaml --experiment experiment_8x1 --signature demo1 --target data/demo1.png
```
Please modify the config files to change configurations.
