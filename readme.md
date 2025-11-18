
Dongjian Yu; Weiqing Min; Xin Jin; Qian Jiang; Shaowen Yao; Shuqiang Jiang
All Authors
[![ 🧾 Paper Information]([https://www.sciencedirect.com/science/article/abs/pii/S1566253525004282](https://ieeexplore.ieee.org/document/11230236))]

## ⚡ Paper Status
**This work has been accepted by 2025 IEEE Transactions on Image Processing (2025 TIP).**

## 🚀 Required Environment
- Operating System: Ubuntu 22.04.2 LTS  
- Python version: 3.10  
- PyTorch version: 2.2.2  
- CUDA version: 12.1 (pytorch-cuda=12.1)  
## 🖥️ Hardware Information

- GPU: NVIDIA A100 40GB 
- CPU: Intel(R) Xeon(R) Gold 6154 CPU @ 3.00GHz  

---

## 🔧 Tips: Temporarily switch CUDA version

If you have multiple CUDA versions installed, you can temporarily switch CUDA version by setting the environment variable before running your program:

```bash
export PATH=/usr/local/cuda-12.1/bin:$PATH  
export LD_LIBRARY_PATH=/usr/local/cuda-12.1/lib64:$LD_LIBRARY_PATH
```

## ⚙️ Installation Instructions
⚠️ Please choose your preferred installation method: 🔧 Manual Installation or 🤖 Automatic Installation.

### 🤖 Automatic Installation
```bash
conda env create -f environment.yml
```

### 🔧 Manual Installation

#### 1. Create and activate conda environment
```bash
conda create -n Food3D python=3.10 -y  
conda activate Food3D
```
#### 2. Install PyTorch with CUDA 12.1
```bash
conda install pytorch==2.2.2 torchvision==0.17.2 torchaudio==2.2.2 pytorch-cuda=12.1 -c pytorch -c nvidia -y
```
#### 3. Install Python dependencies
```bash
pip install plyfile tqdm  
pip install submodules/diff-gaussian-rasterization
```
##### If error occurs, try:  
```bash
sudo apt-get install libglm-dev  
pip install submodules/simple-knn
```
#### 4. Install xformers for CUDA 12.1
```bash
pip3 install -U xformers==0.0.25.post1 --index-url https://download.pytorch.org/whl/cu121
```
#### 5. Install transformers and diffusers
```bash
conda install transformers -y  
conda install diffusers==0.18.2 -y
```

#### 6. Install local point-e-main package
```bash
cd ./point-e-main/  
python setup.py install
```

#### 7. Additional dependencies
```
pip install imageio==2.19.3  
pip install imageio-ffmpeg==0.4.7  
pip install accelerate  
pip install git+https://github.com/openai/CLIP.git  
pip install numpy==1.24.1  
```
```bash
@ARTICLE{11230236,
  author={Yu, Dongjian and Min, Weiqing and Jin, Xin and Jiang, Qian and Yao, Shaowen and Jiang, Shuqiang},
  journal={IEEE Transactions on Image Processing}, 
  title={Food3D: Text-Driven Customizable 3D Food Generation With Gaussian Splatting}, 
  year={2025},
  volume={34},
  number={},
  pages={7290-7304},
  keywords={Three-dimensional displays;Solid modeling;Text to image;Visualization;Diffusion models;Accuracy;Shape;Optimization;IEEE Senior Members;Geometry;Deep learning;diffusion model;3D food generation;food computing;pre-trained model},
  doi={10.1109/TIP.2025.3627408}}

```



