# 1. Create and activate a Python 3.10 environment
conda create -n yudongjian_23_LucidDreamer python=3.10 -y
conda activate yudongjian_23_LucidDreamer

# 2. Install PyTorch and CUDA support (version 12.1)
conda install pytorch==2.2.2 torchvision==0.17.2 torchaudio==2.2.2 pytorch-cuda=12.1 -c pytorch -c nvidia -y

# 3. Install basic Python libraries
pip install plyfile tqdm

# 4. Install submodule dependencies
pip install submodules/diff-gaussian-rasterization
# If you encounter errors, try installing the system dependency first:
# sudo apt-get install libglm-dev
pip install submodules/simple-knn

# 5. Install xformers (specific version with CUDA 12.1 support)
pip3 install -U xformers==0.0.25.post1 --index-url https://download.pytorch.org/whl/cu121

# 6. Install transformers and diffusers
conda install transformers -y
conda install diffusers==0.18.2 -y

# 7. Enter project directory and install local package
cd ./point-e-main/
python setup.py install

# 8. Install other dependencies
pip install imageio==2.19.3
pip install imageio-ffmpeg==0.4.7
pip install accelerate

# 9. Install OpenAI CLIP
pip install git+https://github.com/openai/CLIP.git

# 10. Specify numpy version
pip install numpy==1.24.1
