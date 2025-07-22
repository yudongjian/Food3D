
### 🚀 Required Environment
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
```bash
### 1. Create and activate conda environment
conda create -n yudongjian_23_LucidDreamer python=3.10 -y  
conda activate yudongjian_23_LucidDreamer

### 2. Install PyTorch with CUDA 12.1
conda install pytorch==2.2.2 torchvision==0.17.2 torchaudio==2.2.2 pytorch-cuda=12.1 -c pytorch -c nvidia -y

### 3. Install Python dependencies
pip install plyfile tqdm  
pip install submodules/diff-gaussian-rasterization  
# If error occurs, try:  
sudo apt-get install libglm-dev  
pip install submodules/simple-knn

### 4. Install xformers for CUDA 12.1
pip3 install -U xformers==0.0.25.post1 --index-url https://download.pytorch.org/whl/cu121

### 5. Install transformers and diffusers
conda install transformers -y  
conda install diffusers==0.18.2 -y

### 6. Install local point-e-main package
cd ./point-e-main/  
python setup.py install

### 7. Additional dependencies
pip install imageio==2.19.3  
pip install imageio-ffmpeg==0.4.7  
pip install accelerate  
pip install git+https://github.com/openai/CLIP.git  
pip install numpy==1.24.1  

---


