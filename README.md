# Research__UCM-Distill# UCM-Distill: Multi-Teacher Distillation with Uncertainty Modeling and Contrastive Learning for Weakly Supervised Medical Image Segmentation

<font style="color:rgb(0,0,0);">Te Guo, fan Huang, Hongwei Yu, Manxi Xu, Guolin Ma, </font> Kunfeng Wang<font style="color:rgb(0,0,0);"></font>

## Framework Overview
<img width="6664" height="3929" alt="框架图_01" src="https://github.com/user-attachments/assets/4e95726c-a0be-46bb-b70c-b1166efd8f4a" />


<font style="color:rgb(0,0,0);">The overall framework of the proposed UCM-Distill. Our framework utilizes a multi-teacher distillation paradigm to generate robust supervision. The CUPG module quantifies inter-teacher discrepancies via entropy modeling to produce refined, uncertainty-aware soft pseudo-labels $\hat{Y}$. Subsequently, the MGCD strategy incorporates a mask-guided contrastive distillation loss $\mathcal{L}_{con}$ to enforce feature disentanglement in the embedding space $E$, enhancing intra-class compactness and inter-class separability. The entire network is optimized end-to-end through joint segmentation and contrastive learning objectives.</font>

## Install
### Environment
<font style="color:rgb(31, 35, 40);">The code is built with following libraries:</font>

+ <font style="color:rgb(31, 35, 40);">Python = 3.10</font>
+ <font style="color:rgb(31, 35, 40);">tensorflow = 2.19</font>
+ <font style="color:rgb(31, 35, 40);">h5py = 3.13</font>
+ <font style="color:rgb(31, 35, 40);">imageio = 2.37</font>
+ <font style="color:rgb(31, 35, 40);">keras = 3.10</font>
+ markdown = 3.5.1
+ <font style="color:rgb(31, 35, 40);">medpy = 0.5.2</font>
+ <font style="color:rgb(31, 35, 40);">nibabel = 5.3.2</font>
+ <font style="color:rgb(31, 35, 40);">opencv-python = 4.11</font>
+ <font style="color:rgb(31, 35, 40);">pandas =2.2.3</font>
+ <font style="color:rgb(31, 35, 40);">scikit-image = 0.25.2</font>

### <font style="color:rgb(31, 35, 40);">Training</font>
#### <font style="color:rgb(31, 35, 40);">1.Download Datasets</font>
<font style="color:rgb(31, 35, 40);">You can download the </font><font style="color:rgb(0,0,0);">public</font><font style="color:rgb(31, 35, 40);"> datasets using the following links: </font>[https://www.kaggle.com/datasets/atikaakter11/brain-tumor-segmentation-dataset](https://www.kaggle.com/datasets/atikaakter11/brain-tumor-segmentation-dataset)
#### <font style="color:rgb(31, 35, 40);">2.Data preprocessing</font>
    --python Creat_yolodata.py --dataset 'p'
#### <font style="color:rgb(31, 35, 40);">3.Box Generation </font><font style="color:rgb(0,0,0);">Sub-network</font>
    --pyhton detection.py 
#### <font style="color:rgb(0,0,0);">4.Distillation Sub-network</font>
    --pyhton meddistill.py
#### <font style="color:rgb(0,0,0);">5.Test
    --python predict_eval.py \
    --image_dir /root/autodl-tmp/p/1/test/images\
    --mask_dir /root/autodl-tmp/p/1/testmasks \
    --model_path sam2-unetpp-1.pth  \
    --vis_dir vis_results
### <font style="color:rgb(31, 35, 40);">Contact Us</font>
<font style="color:rgb(31, 35, 40);">If you have any problem about this work, please feel free to reach us out at te.guo@buct.edu.cn</font>`

