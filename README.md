# Research__UCM-Distill# UCM-Distill: Multi-Teacher Distillation with Uncertainty Modeling and Contrastive Learning for Weakly Supervised Medical Image Segmentation

<font style="color:rgb(0,0,0);">Te Guo, fan Huang, Hongwei Yu, Manxi Xu, Guolin Ma, </font> Kunfeng Wang<font style="color:rgb(0,0,0);"></font>

## Framework Overview
<img width="6664" height="3929" alt="框架图_01" src="https://github.com/user-attachments/assets/4e95726c-a0be-46bb-b70c-b1166efd8f4a" />


<font style="color:rgb(0,0,0);">The overall framework of the proposed UCM-Distill. Our framework utilizes a multi-teacher distillation paradigm to generate robust supervision. The CUPG module quantifies inter-teacher discrepancies via entropy modeling to produce refined, uncertainty-aware soft pseudo-labels $\hat{Y}$. Subsequently, the MGCD strategy incorporates a mask-guided contrastive distillation loss $\mathcal{L}_{con}$ to enforce feature disentanglement in the embedding space $E$, enhancing intra-class compactness and inter-class separability. The entire network is optimized end-to-end through joint segmentation and contrastive learning objectives.</font>

## Install
### Environment
<font style="color:rgb(31, 35, 40);">The code is built with following libraries:</font>

+ Python = 3.10
+ <font style="color:rgb(31, 35, 40);"> PyTorch = 2.1.2 </font>
+ <font style="color:rgb(31, 35, 40);"> torchvision = 0.16.2 </font>
+ <font style="color:rgb(31, 35, 40);"> CUDA = 12.1 </font>
+ <font style="color:rgb(31, 35, 40);"> numpy = 1.26.4 </font>
+ <font style="color:rgb(31, 35, 40);"> opencv-python = 4.11 </font>
+ <font style="color:rgb(31, 35, 40);"> scipy = 1.13.1 </font>
+ <font style="color:rgb(31, 35, 40);"> tqdm = 4.67.1 </font>
+ <font style="color:rgb(31, 35, 40);"> hydra-core = 1.3.2 </font>
+ <font style="color:rgb(31, 35, 40);"> omegaconf = 2.3.0 </font>
+ <font style="color:rgb(31, 35, 40);"> PyYAML = 6.0.2 </font>
+ <font style="color:rgb(31, 35, 40);"> matplotlib = 3.9.4 </font>
+ <font style="color:rgb(31, 35, 40);"> scikit-image = 0.24.0 </font>
+ <font style="color:rgb(31, 35, 40);"> thop = 0.1.1.post2209072238 </font>
+ <font style="color:rgb(31, 35, 40);"> segmentation-models-pytorch = 0.3.3</font>

### <font style="color:rgb(31, 35, 40);">Training</font>
#### <font style="color:rgb(31, 35, 40);">1.Download Datasets</font>
<font style="color:rgb(31, 35, 40);">You can download the </font><font style="color:rgb(0,0,0);">public</font><font style="color:rgb(31, 35, 40);"> datasets using the following links: </font>

[http://medicaldecathlon.com/](http://medicaldecathlon.com/)  
[https://www.kaggle.com/datasets/atikaakter11/brain-tumor-segmentation-dataset](https://www.kaggle.com/datasets/atikaakter11/brain-tumor-segmentation-dataset)

#### <font style="color:rgb(31, 35, 40);">2.Data preprocessing</font>
python preprocessing.py 

#### <font style="color:rgb(0,0,0);">3.Distillation network</font>
pyhton UCM-Distill.py

#### 4.Test
python test.py 

### <font style="color:rgb(31, 35, 40);">Contact Us</font>
<font style="color:rgb(31, 35, 40);">If you have any problem about this work, please feel free to reach us out at </font>`<font style="color:rgb(31, 35, 40);background-color:rgba(129, 139, 152, 0.12);">te.guo@buct.edu.cn</font>`





