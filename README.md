# Environment
Our experimental environment setup is listed below:
* Graphic Card: NVIDIA GeForce RTX 4090
* Processor: Intel(R) Xeon(R) Platinum 8358P CPU @ 2.60GHz
* Operating System: Ubuntu 20.04
* Container: Docker version 24.0.2
* Python Version: 3.7
* Python Libraries: transformers 4.23.1, datasets 2.1.0, pytorch 1.11.0

# Dataset
Download 5ds dataset from [link](https://drive.google.com/file/d/1rWcgnVcNpwxmBI3c5ovNx-E8XKOEL77S/view).
Extract contents from 'LAMOL.tar.gz' to 'data' directory, and run command below.
```sh
python preprocess.py
```
	
# Run
The syntax of command is listed below:
```sh
python run.py \
    --dataset {5ds|WOS} \
    --prompt_fusion_mode {None|fusion|last|mean|SMD} \
    --method epi \
    --query_mode mahalanobis \
    --prompt_mode prefix \
    --pre_seq_len 32 \
    --n_per_class {2000|10|20|50} \
    --batch_size 32 \
    --lr 0.05 \
    --epochs 5
```