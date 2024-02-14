<p align="center">
  <img width="70%" src="https://raw.githubusercontent.com/Kent0n-Li/nnUNet_GUI/main/img/icon.png">
</p>



# nnUNet with GUI <br> 可视化网页版本nnUNet

The current code is designed for Windows, not for Linux. 

## If you already have nnUNet installed, only install the GUI page （如果你已经安装nnUNet，只安装GUI页面）

```bash
git clone https://github.com/Kent0n-Li/nnUNet_GUI_tiny.git
cd nnUNet_GUI_tiny
pip install -r requirements.txt
```



## Install from scratch 从零开始安装
Install (安装步骤):

```bash
conda create -n nnsam python=3.9
conda activate nnsam
```

Choose a suitable Pytorch with CUDA to install <br> 
根据CUDA选择合适版本的Pytorch进行安装
```bash
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu117
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
```

```bash
pip install git+https://github.com/ChaoningZhang/MobileSAM.git
pip install timm
pip install git+https://github.com/Kent0n-Li/nnSAM.git

git clone https://github.com/Kent0n-Li/nnUNet_GUI.git
cd Medical-Image-Segmentation-Benchmark
pip install -r requirements.txt
```



## Install from scratch without nnSAM 只安装nnUNet
Install (安装步骤):

```bash
conda create -n nnu python=3.9
conda activate nnu
```

Choose a suitable Pytorch with CUDA to install <br> 
根据CUDA选择合适版本的Pytorch进行安装
```bash
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu117
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
```

```bash
pip install nnunetv2

git clone https://github.com/Kent0n-Li/nnUNet_GUI_tiny.git
cd nnUNet_GUI_tiny
pip install -r requirements.txt
```


## 运行可视化软件
```bash
python web.py
```

If you only want to use nnSAM, please install [this](https://github.com/Kent0n-Li/nnSAM). <br>
如果你只想运行nnSAM,请访问该代码仓库[this](https://github.com/Kent0n-Li/nnSAM)

样例数据集：[Demo Dataset](https://github.com/Kent0n-Li/Medical-Image-Segmentation/tree/main/Demo_dataset)


## Overview 页面总览
![image](https://github.com/Kent0n-Li/Medical-Image-Segmentation-Benchmark/blob/main/img/img1.png)

## Choose Model  选择模型
![image](https://github.com/Kent0n-Li/Medical-Image-Segmentation-Benchmark/blob/main/img/img2.png)

## Import Data 导入你的数据集 （2D: png, 3D: nii.gz) 
### 样例数据集：[Demo Dataset](https://github.com/Kent0n-Li/Medical-Image-Segmentation/tree/main/Demo_dataset)
![image](https://github.com/Kent0n-Li/Medical-Image-Segmentation-Benchmark/blob/main/img/img3.png)

## Full Auto 全自动模式，一键完成从数据预处理到训练测试和结果总结
![image](https://github.com/Kent0n-Li/Medical-Image-Segmentation-Benchmark/blob/main/img/img4.png)

## Result Summary 结果总结
![image](https://github.com/Kent0n-Li/Medical-Image-Segmentation-Benchmark/blob/main/img/img5.png)



## Citation

If you find this repository useful for your research, please use the following.

```
@article{li2023nnsam,
  title={nnSAM: Plug-and-play Segment Anything Model Improves nnUNet Performance},
  author={Li, Yunxiang and Jing, Bowen and Li, Zihan and Wang, Jing and Zhang, You},
  journal={arXiv preprint arXiv:2309.16967},
  year={2023}
}
```
