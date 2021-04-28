# 1. Clone repo  
`git clone https://github.com/SwinTransformer/Swin-Transformer-Object-Detection.git`
# 2. Setup docker 
```
cd Swin-Transformer-Object-Detection
docker build -t swin_mmd docker/
nvidia-docker run --name swin --gpus all --shm-size=32g -p 5000:5000 -p 5001:5001 -it -v /data/thang/Swin-Transformer-Object-Detection/:/mmdetection swin_mmd 
```
# 3. Instal apex
```
git clone https://github.com/NVIDIA/apex
cd apex
git checkout f3a960f80244cf9e80558ab30f7f7e8cbf03c0a0
python setup.py install --cuda_ext --cpp_ext
```