CPU 환경

```bash
conda create -n solar python=3.10
conda activate solar
pip install -r requirements.txt
```


---
<br>

GPU환경

기존 torch 삭제
```bash
pip install torch torchvision torchauidio -y
```

CUDA 버전 확인
```bash
nvidia-smi
```
- CUDA Version: 12.x -> 최신 torch 가능

torch 설치
```bash
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
```
- cu118이 가장 안정적
- 현재 환경 GTX 1050 Ti에 적합

설치확인
```python
import torch

print(torch.cuda.is_available())  # True 나와야 정상
print(torch.cuda.get_device_name()) # NVIDIA GeForce GTX 1050 Ti
```
