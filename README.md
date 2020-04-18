# Detectron2 Packages
FAIR Detectron2 https://github.com/facebookresearch/detectron2

Model Zoo Backbone/Pretrained are saved in \~/.torch/fvcore_cache/detectron2

## Trained Models
https://drive.google.com/drive/folders/1IkcKH8hAhpjryCaGts3VwGPuOnlKRJMe?usp=sharing

## [Colab Notebooks](colab)
[COCO 2017 Training](colab/Detectron2_Train_COCO_2017.ipynb)

## COCO 2017 Colab Download/Setup
[COCO Download & Setup](dataset_download)

## Setup and Install
### Detectron2 GPU
```bash
# Clone and go into directory
git clone --recurse-submodules https://github.com/sawyermade/detectron2_pkgs.git
cd detectron2_pkgs

# Create conda environment and activate it
conda create -n detectron2 python=3.6 -y
conda activate detectron2

# Install packages
conda install pytorch torchvision cudatoolkit=10.1 -c pytorch -y
pip install cython requests jsonpickle pyrealsense2 flask imageio shapely flask-ngrok
pip install -U 'git+https://github.com/cocodataset/cocoapi.git#subdirectory=PythonAPI'
pip install -U 'git+https://github.com/cocodataset/panopticapi.git'
pip install -U 'git+https://github.com/lvis-dataset/lvis-api.git'
pip install -U 'git+https://github.com/mcordts/cityscapesScripts.git'
rm -rf detectron2/build
pip install -e detectron2
```

### Detectron2 CPU
```bash
conda create -n detectron2cpu python=3.6 -y
conda activate detectron2cpu
pip install detectron2 -f \
	https://dl.fbaipublicfiles.com/detectron2/wheels/cpu/index.html
conda install pytorch torchvision cpuonly -c pytorch
conda install cython -y
conda install -c menpo opencv -y
pip install 'git+https://github.com/cocodataset/cocoapi.git#subdirectory=PythonAPI'
pip install requests jsonpickle pyrealsense2 flask
```

## Packages
### Demos
[Go to demo directory](demo)

### HTTP Server
[Go to http directory](http)

### ROS Package
[Go to ros directory](http)

## Training
[Go to train directory](train)