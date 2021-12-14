# TransBTS: Multimodal Brain Tumor Segmentation Using Transformer
## Abstract:
1. For the first time exploits Transformer in 3D CNN for MRI Brain Tumor Segmentation --> TransBTS
2. Encoder-decoder structure: The encoder first utilizes 3D CNN to extract the volumetric spatial feature maps. Meanwhile, the feature maps are reformed elaborately for tokens that are fed into Transformer for global feature modeling. The decoder leverages the features embedded by Transformer and performs progressive upsampling to predict the detailed segmentation map.
3. Source code: https://github.com/Wenxuan-1119/TransBTS

## Introduction:
1. U-Net uses a symmetric encoder-decoder structure with skip-connections to improve detail retention, becoming the mainstream architecture for medical image segmentation.
2. 

## 生词
| 单词     | 中文|
| :-----------: | :-----------:|
| Gliomas     | 胶质瘤       |
| malignant  | 致命的，传染性强的，恶毒的，有害的|
| malignancy  | 恶性肿瘤|
| malignancy  | 恶性肿瘤|
 
