![LOGO](logo.png)
<!-- omit in toc -->
## 📖 Recommendations of Document Image Processing
This repository contains a paper collection of the methods for document image processing, including appearance enhancement, deshadow, dewarping, deblur, and binarization.

<!-- omit in toc -->
## 🔥 Contents
- [1. Appearance Enhancement](#1-appearance-enhancement)
  - [1.1 Papers](#11-papers)
  - [1.2 Datasets](#12-datasets)
  - [1.3 Apps](#13-apps)
  - [1.4 SOTA](#14-sota)
- [2. Deshadow](#2-deshadow)
  - [2.1 Papers](#21-papers)
  - [2.2 Datasets](#22-datasets)
  - [2.3 SOTA](#23-sota)
- [3. Dewarping](#3-dewarping)
  - [3.1 Papers](#31-papers)
  - [3.2 Dataset](#32-dataset)
  - [3.3 SOTA](#33-sota)
- [4. Deblur](#4-deblur)
  - [4.1 Papers](#41-papers)
  - [4.2 Datasets](#42-datasets)
  - [4.3 SOTA](#43-sota)
- [5. Binarization](#5-binarization)
  - [5.1 Papers](#51-papers)
  - [5.2 Datasets](#52-datasets)
  - [5.3 SOTA](#53-sota)
- [⭐ Star Rising](#-star-rising)

## 1. Appearance Enhancement
Appearance enhancement (also known as illumination correction) is not limited to a specific degradation type and aims to restore a clean appearance similar to that obtained from a scanner or digital born PDF files.

### 1.1 Papers
|Year|Venue|Title|Repo|
|----|----|-----|----|
|2019|ACM TOG|[Document Rectification and Illumination Correction using a Patch-based CNN](https://dl.acm.org/doi/abs/10.1145/3355089.3356563)|[Code](https://github.com/xiaoyu258/DocProj)|
|2020|BMVC|[Intrinsic Decomposition of Document Images In-the-wild](https://arxiv.org/abs/2011.14447)|[Code](https://github.com/cvlab-stonybrook/DocIIW)|
|2021|ICCV|[DewarpNet: Single-Image Document Unwarping With Stacked 3D and 2D Regression Networks](https://openaccess.thecvf.com/content_ICCV_2019/html/Das_DewarpNet_Single-Image_Document_Unwarping_With_Stacked_3D_and_2D_Regression_ICCV_2019_paper.html)|[Code](https://github.com/cvlab-stonybrook/DewarpNet)|
|2021|ACM MM|[DocTr: Document Image Transformer for Geometric Unwarping and Illumination Correction](https://arxiv.org/pdf/2110.12942v2.pdf)|[Code](https://github.com/fh2019ustc/DocTr)|
|2022|CVPR|[Fourier Document Restoration for Robust Document Dewarping and Recognition](https://openaccess.thecvf.com/content/CVPR2022/html/Xue_Fourier_Document_Restoration_for_Robust_Document_Dewarping_and_Recognition_CVPR_2022_paper.html)||
|2022|ACM MM|[UDoc-GAN: Unpaired Document Illumination Correction with Background Light Prior](https://dl.acm.org/doi/abs/10.1145/3503161.3547916)|[Code](https://github.com/harrytea/UDoc-GAN)|
|2023|TAI|[Appearance Enhancement for Camera-captured Document Images in the Wild](https://ieeexplore.ieee.org/abstract/document/10268585/)|[Code](https://github.com/ZZZHANG-jx/GCDRNet)|
|2023|ICCVW|[Template-guided Illumination Correction for Document Images with Imperfect Geometric Reconstruction](https://openaccess.thecvf.com/content/ICCV2023W/NIVT/html/Hertlein_Template-Guided_Illumination_Correction_for_Document_Images_with_Imperfect_Geometric_Reconstruction_ICCVW_2023_paper.html)|[Code](https://github.com/FelixHertlein/illtrtemplate-model)|
|2023|arxiv|[DocStormer: Revitalizing Multi-Degraded Colored Document Images to Pristine PDF Versions](https://arxiv.org/abs/2310.17910)||
|2024|ICASSP|[Efficient Joint Rectification of Photometric and Geometric Distortions in Document Images](https://ieeexplore.ieee.org/abstract/document/10447446)||
|2024|CVPR|[DocRes: A Generalist Model Toward Unifying Document Image Restoration Tasks](https://arxiv.org/abs/2405.04408)|[Code](https://github.com/ZZZHANG-jx/DocRes)|


### 1.2 Datasets

|Dataset|Num. (train/test)|Type|Example|Download|
|----|----|----|----|----|
|[Doc3DShade](https://arxiv.org/abs/2011.14447)|90K|Synth|[Example](./Dataset_image/doc3dshade/readme.md)|[Link](https://github.com/cvlab-stonybrook/DocIIW)|
|[DocProj](https://dl.acm.org/doi/abs/10.1145/3355089.3356563)|2450|Synth|[Example](./Dataset_image/docproj/readme.md)|[Link](https://github.com/xiaoyu258/DocProj)|
|[DocUNet from DocAligner](https://openaccess.thecvf.com/content_cvpr_2018/html/Ma_DocUNet_Document_Image_CVPR_2018_paper.html)|130|Real|[Example](./Dataset_image/docunet_docaligner/readme.md)|[Link](https://github.com/ZZZHANG-jx/DocAligner)|
|[RealDAE](https://ieeexplore.ieee.org/abstract/document/10268585/)|600 (450/150)|Real|[Example](./Dataset_image/realdae/readme.md)|[Link](https://github.com/ZZZHANG-jx/GCDRNet)|
|[Inv3D](https://link.springer.com/article/10.1007/s10032-023-00434-x)|25K|Synth|[Example](./Dataset_image/inv3d/readme.md)|[Link](https://github.com/FelixHertlein/inv3d)|


### 1.3 Apps

- [CamScanner](https://www.camscanner.com/)
- [Adobe Acrobat](https://helpx.adobe.com/acrobat/using/enhance-camera-images.html)
- [Lenovo Smart Scanner](https://static.xue.lenovomm.com/scannerpc.html)
- [Quark](https://www.quark.cn/)

### 1.4 SOTA
<table class="tg">
<thead>
  <tr>
    <th class="tg-c3ow" rowspan="2">Venue</th>
    <th class="tg-c3ow" rowspan="2">Methods</th>
    <th class="tg-c3ow" rowspan="2">Training data</th>
    <th class="tg-c3ow" colspan="2">DocUNet from DocAligner (130)</th>
    <th class="tg-c3ow" colspan="2">RealDAE (150)</th>
  </tr>
  <tr>
    <th class="tg-c3ow">SSIM</th>
    <th class="tg-c3ow">PSNR</th>
    <th class="tg-c3ow">SSIM</th>
    <th class="tg-c3ow">PSNR</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">0.7195</td>
    <td class="tg-c3ow">13.09</td>
    <td class="tg-c3ow">0.8264</td>
    <td class="tg-c3ow">12.26</td>
  </tr>
  <tr>
    <td class="tg-c3ow">TOG'19</td>
    <td class="tg-c3ow"><a href="https://arxiv.org/pdf/1909.09470.pdf">DocProj</a></td>
    <td class="tg-c3ow">DocProj</td>
    <td class="tg-c3ow">0.7098</td>
    <td class="tg-c3ow">14.71</td>
    <td class="tg-c3ow">0.8684</td>
    <td class="tg-c3ow">19.35</td>
  </tr>
  <tr>
    <td class="tg-c3ow">BMVC'20</td>
    <td class="tg-c3ow"><a href="https://arxiv.org/abs/2011.14447">Das et al.</a></td>
    <td class="tg-c3ow">Doc3DShade</td>
    <td class="tg-c3ow">0.7276</td>
    <td class="tg-c3ow">16.42</td>
    <td class="tg-c3ow">0.8633</td>
    <td class="tg-c3ow">19.87</td>
  </tr>
  <tr>
    <td class="tg-c3ow">MM'21</td>
    <td class="tg-c3ow"><a href="https://arxiv.org/pdf/2110.12942.pdf">DocTr</a></td>
    <td class="tg-c3ow">DocProj</td>
    <td class="tg-c3ow">0.7067</td>
    <td class="tg-c3ow">15.78</td>
    <td class="tg-c3ow">0.7925</td>
    <td class="tg-c3ow">18.62</td>
  </tr>
  <tr>
    <td class="tg-c3ow">MM'22</td>
    <td class="tg-c3ow"><a href="https://dl.acm.org/doi/abs/10.1145/3503161.3547916">UDoc-GAN</a></td>
    <td class="tg-c3ow">DocProj</td>
    <td class="tg-c3ow">0.6833</td>
    <td class="tg-c3ow">14.29</td>
    <td class="tg-c3ow">0.7558</td>
    <td class="tg-c3ow">16.43</td>
  </tr>
  <tr>
    <td class="tg-c3ow">TAI'23</td>
    <td class="tg-c3ow"><a href="https://ieeexplore.ieee.org/abstract/document/10268585/">GCDRNet</a></td>
    <td class="tg-c3ow">RealDAE</td>
    <td class="tg-c3ow"><b>0.7658</b></td>
    <td class="tg-c3ow">17.09</td>
    <td class="tg-c3ow"><b>0.9423</b></td>
    <td class="tg-c3ow">24.42</td>
  </tr>
  <tr>
    <td class="tg-c3ow">CVPR'24</td>
    <td class="tg-c3ow"><a href="https://arxiv.org/pdf/2405.04408">DocRes</a></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">0.7598</td>
    <td class="tg-c3ow"><b>17.60</b></td>
    <td class="tg-c3ow">0.9219</td>
    <td class="tg-c3ow"><b>24.65</b></td>
  </tr>
</tbody>
</table>


## 2. Deshadow
Deshadowing aims to eliminate shadows that are mainly caused by occlusion to obtain shadow-free document images.

### 2.1 Papers
|Year|Venue|Title|Repo|
|----|----|-----|----|
|2018|CVPR|[Document Enhancement Using Visibility Detection](https://openaccess.thecvf.com/content_cvpr_2018/html/Kligler_Document_Enhancement_Using_CVPR_2018_paper.html)|[Code](https://github.com/CV-Reimplementation/Document-Enhancement-using-Visibility-Detection)|
|2020|CVPR|[BEDSR-Net A Deep Shadow Removal Network from a Single Document Image](https://openaccess.thecvf.com/content_CVPR_2020/html/Lin_BEDSR-Net_A_Deep_Shadow_Removal_Network_From_a_Single_Document_CVPR_2020_paper.html)|[Code*](https://github.com/IsHYuhi/BEDSR-Net_A_Deep_Shadow_Removal_Network_from_a_Single_Document_Image)|
|2022|ICPR|[Document Shadow Removal with Foreground Detection Learning From Fully Synth Images](https://ieeexplore.ieee.org/abstract/document/9897217)|[Code](https://github.com/IsHYuhi/DSRFGD)|
|2022|MERCon|[Shadow Removal for Documents with Reflective Textured Surface](https://ieeexplore.ieee.org/abstract/document/9906227)||
|2023|ICASSP|[ShaDocNet: Learning Spatial-Aware Tokens in Transformer for Document Shadow Removal](https://arxiv.org/abs/2211.16675)|[Code](https://github.com/CXH-Research/ShadocNet)|
|2023|ICASSP|[Shadow Removal of Text Document Images Using Background Estimation and Adaptive Text Enhancement](https://ieeexplore.ieee.org/abstract/document/10096115)||
|2023|ICASSP|[LP-IOANet: Efficient High Resolution Document Shadow Removal](https://arxiv.org/pdf/2303.12862.pdf)||
|2023|Optical Review|[Shadow removal from document image based on background estimation employing selective median filter and black-top-hat transform](https://link.springer.com/article/10.1007/s10043-023-00806-y)||
|2023|CVPR|[Document Image Shadow Removal Guided by Color-Aware Background](https://openaccess.thecvf.com/content/CVPR2023/html/Zhang_Document_Image_Shadow_Removal_Guided_by_Color-Aware_Background_CVPR_2023_paper.html)|[Code](https://github.com/hyyh1314/BGShadowNet)|
|2023|arxiv|[ShaDocFormer: A Shadow-attentive Threshold Detector with Cascaded Fusion Refiner for document shadow removal](https://arxiv.org/abs/2309.06670)||
|2023|ICCV|[High-Resolution Document Shadow Removal via A Large-Scale Real-World Dataset and A Frequency-Aware Shadow Erasing Net](https://openaccess.thecvf.com/content/ICCV2023/html/Li_High-Resolution_Document_Shadow_Removal_via_A_Large-Scale_Real-World_Dataset_and_ICCV_2023_paper.html)|[Code](https://github.com/CXH-Research/DocShadow-SD7K)|
|2023|Sensors|[Synthetic Document Images with Diverse Shadows for Deep Shadow Removal Networks](https://www.mdpi.com/1424-8220/24/2/654)|[Code](https://github.com/ym4t50/SynDoc4DSFN)|
|2024|AAAI|[DocNLC: A Document Image Enhancement Framework with Normalized and Latent Contrastive Representation for Multiple Degradations](https://ojs.aaai.org/index.php/AAAI/article/view/28366)|[Code](https://github.com/RylonW/DocNLC)|
|2024|CVPR|[DocRes: A Generalist Model Toward Unifying Document Image Restoration Tasks](https://arxiv.org/abs/2405.04408)|[Code](https://github.com/ZZZHANG-jx/DocRes)|
|2024|IJDAR|[Am I readable? Transfer learning based document image rectification](https://link.springer.com/article/10.1007/s10032-024-00476-9)||

\* indicates that the implementation is unofficial.


### 2.2 Datasets

|Dataset|Num. (train/test)|Type|Example|Download|
|----|----|----|----|----|
|[RDD](https://openaccess.thecvf.com/content/CVPR2023/html/Zhang_Document_Image_Shadow_Removal_Guided_by_Color-Aware_Background_CVPR_2023_paper.html)|4916 (4371/545)|Real|[Example](./Dataset_image/rdd/readme.md)|[Link](https://github.com/hyyh1314/RDD)|
|[Kligler et al.](https://openaccess.thecvf.com/content_cvpr_2018/html/Kligler_Document_Enhancement_Using_CVPR_2018_paper.html)|300|Real|[Example](./Dataset_image/kligler/kligler.md)|[Link](https://pan.baidu.com/s/17s0aD6Aqq9lFI_TTH5PJVg?pwd=3slt)|
|[FSDSRD](https://ieeexplore.ieee.org/abstract/document/9897217)|14200|Synth|[Example](./Dataset_image/fsdsrd/fsdsrd.md)|[Link](https://github.com/IsHYuhi/DSRFGD)|
|[Jung et al.](https://link.springer.com/chapter/10.1007/978-3-030-20887-5_25)|87|Real|[Example](./Dataset_image/jung/jung.md)|[Link](https://static-content.springer.com/esm/chp%3A10.1007%2F978-3-030-20887-5_25/MediaObjects/484511_1_En_25_MOESM1_ESM.zip)|
|[OSR](https://www.mdpi.com/1424-8220/20/23/6929)|237|Real|[Example](./Dataset_image/osr/osr.md)|[Link](https://github.com/BingshuCV/DocumentShadowRemoval)|
|[WEZUT OCR](https://www.mdpi.com/1424-8220/20/10/2914)|176|Real|[Example](./Dataset_image/wezut/wezut.md)|[Link](https://okarma.zut.edu.pl/?id=dataset&L=1)|
|[SD7K](https://openaccess.thecvf.com/content/ICCV2023/html/Li_High-Resolution_Document_Shadow_Removal_via_A_Large-Scale_Real-World_Dataset_and_ICCV_2023_paper.html)|7620 (6479/760)|Real|[Example](./Dataset_image/sd7k/readme.md)|[Link](https://github.com/CXH-Research/DocShadow-SD7K)|
|[SynDocDS](https://www.mdpi.com/1424-8220/24/2/654)|50K (40K/5K)|Synth||[Link](https://github.com/ym4t50/SynDoc4DSFN)|




### 2.3 SOTA
<table class="tg">
<thead>
  <tr>
    <th class="tg-c3ow" rowspan="2">Venue</th>
    <th class="tg-c3ow" rowspan="2">Method</th>
    <th class="tg-c3ow" rowspan="2">Training data</th>
    <th class="tg-c3ow" colspan="3"><a href="https://openaccess.thecvf.com/content_cvpr_2018/html/Kligler_Document_Enhancement_Using_CVPR_2018_paper.html">Kligler et al. (300)</a></th>
    <th class="tg-c3ow" colspan="3"><a href="https://link.springer.com/chapter/10.1007/978-3-030-20887-5_25">Jung et al. (87)</a></th>
    <th class="tg-c3ow" colspan="3"><a href="https://www.mdpi.com/1424-8220/20/23/6929">OSR (237)</a></th>
    <th class="tg-c3ow" colspan="3"><a href="https://www.mdpi.com/1424-8220/20/23/6929">RDD (545)</a></th>
    <th class="tg-c3ow" colspan="3"><a href="https://www.mdpi.com/1424-8220/20/23/6929">SD7K (760)</a></th>
  </tr>
  <tr>
    <th class="tg-c3ow">RMSE↓</th>
    <th class="tg-c3ow">PSNR↑</th>
    <th class="tg-c3ow">SSIM↑</th>
    <th class="tg-c3ow">RMSE↓</th>
    <th class="tg-c3ow">PSNR↑</th>
    <th class="tg-c3ow">SSIM↑</th>
    <th class="tg-c3ow">RMSE↓</th>
    <th class="tg-c3ow">PSNR↑</th>
    <th class="tg-c3ow">SSIM↑</th>
    <th class="tg-c3ow">RMSE↓</th>
    <th class="tg-c3ow">PSNR↑</th>
    <th class="tg-c3ow">SSIM↑</th>
    <th class="tg-c3ow">RMSE↓</th>
    <th class="tg-c3ow">PSNR↑</th>
    <th class="tg-c3ow">SSIM↑</th>
  </tr>
</thead>
<tbody>
</tbody>
<tbody>
  <!-- <tr>
    <td class="tg-c3ow">CVPR'18</td>
    <td class="tg-c3ow">Kligler et al.</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">22.81</td>
    <td class="tg-c3ow">21.21</td>
    <td class="tg-c3ow">0.8058</td>
    <td class="tg-c3ow">29.06</td>
    <td class="tg-c3ow">19.05</td>
    <td class="tg-c3ow">0.8274</td>
    <td class="tg-c3ow">33.50</td>
    <td class="tg-c3ow">17.84</td>
    <td class="tg-c3ow">0.8451</td>
    <td class="tg-c3ow">37.67</td>
    <td class="tg-c3ow">16.84</td>
    <td class="tg-c3ow">0.7668</td>
  </tr> -->
  <!-- <tr>
    <td class="tg-c3ow">CVPR'20</td>
    <td class="tg-c3ow">BEDSR-Net</td>
    <td class="tg-c3ow">SDSRD</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">32.90</td>
    <td class="tg-c3ow">0.9354</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">27.23</td>
    <td class="tg-c3ow">0.9115</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
  </tr>
</tbody>
<tbody>
  <tr>
    <td class="tg-c3ow">CVPR'20</td>
    <td class="tg-c3ow">BEDSR-Net</td>
    <td class="tg-c3ow">FSDSRD</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">22.36</td>
    <td class="tg-c3ow">0.9286</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">22.38</td>
    <td class="tg-c3ow">0.9464</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
  </tr>
</tbody>
<tbody>
  <tr>
    <td class="tg-c3ow">CVPR'20</td>
    <td class="tg-c3ow">BEDSR-Net</td>
    <td class="tg-c3ow">RDD</td>
    <td class="tg-c3ow">6.533</td>
    <td class="tg-c3ow">28.12</td>
    <td class="tg-c3ow">0.9320</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">2.937</td>
    <td class="tg-c3ow">34.928</td>
    <td class="tg-c3ow">0.973</td>
  </tr>
    <td class="tg-c3ow">CVPR'20</td>
    <td class="tg-c3ow">BEDSR-Net</td>
    <td class="tg-c3ow">Jung</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
</tbody>
<tbody>
  <tr>
    <td class="tg-c3ow">ICIP'22</td>
    <td class="tg-c3ow">DSRFGD</td>
    <td class="tg-c3ow">FSDSRD</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">23.02</td>
    <td class="tg-c3ow">0.9302</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">21.62</td>
    <td class="tg-c3ow">0.9525</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
  </tr>
</tbody>
<tbody>
  <tr>
    <td class="tg-c3ow">ArXiv'23</td>
    <td class="tg-c3ow">ShaDocFormer</td>
    <td class="tg-c3ow">RDD</td>
    <td class="tg-c3ow">13.17</td>
    <td class="tg-c3ow">26.36</td>
    <td class="tg-c3ow">0.90</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">8.9</td>
    <td class="tg-c3ow">29.46</td>
    <td class="tg-c3ow">0.92</td>  
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>  
  </tr>
</tbody>
<tbody>
  <tr>
    <td class="tg-c3ow">CVPR'23</td>
    <td class="tg-c3ow">BGShadeNet_retest</td>
    <td class="tg-c3ow">RDD</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">35.36</td>
    <td class="tg-c3ow">17.34</td>
    <td class="tg-c3ow">0.9040</td>
    <td class="tg-c3ow">19.72</td>
    <td class="tg-c3ow">22.64</td>
    <td class="tg-c3ow">0.9388</td>
    <td class="tg-c3ow">6.02</td>
    <td class="tg-c3ow">33.33</td>
    <td class="tg-c3ow">0.9520</td>    
  </tr>
</tbody>
<tbody>
  <tr>
    <td class="tg-c3ow">ICASSP'23</td>
    <td class="tg-c3ow"><a href='https://arxiv.org/abs/2211.16675'>ShaDocNet</a></td>
    <td class="tg-c3ow">kilger</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
  </tr>
</tbody>
<tbody>
  <tr>
    <td class="tg-c3ow">ICASSP'23</td>
    <td class="tg-c3ow">ShaDocNet</td>
    <td class="tg-c3ow">Jung</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
  </tr> -->
<tbody>
  <tr>
    <td class="tg-c3ow">CVPR'23</td>
    <td class="tg-c3ow"><a href='https://openaccess.thecvf.com/content/CVPR2023/html/Zhang_Document_Image_Shadow_Removal_Guided_by_Color-Aware_Background_CVPR_2023_paper.html'>BGShadowNet</a></td>
    <td class="tg-c3ow">RDD</td>
    <td class="tg-c3ow">5.377</td>
    <td class="tg-c3ow">29.17</td>
    <td class="tg-c3ow">0.948</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>    
    <td class="tg-c3ow">2.219</td>
    <td class="tg-c3ow">37.58</td>
    <td class="tg-c3ow">0.983</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>    
  </tr>
</tbody>
  <tr>
    <td class="tg-c3ow">ICCV'23</td>
    <td class="tg-c3ow"><a href='https://openaccess.thecvf.com/content/ICCV2023/html/Li_High-Resolution_Document_Shadow_Removal_via_A_Large-Scale_Real-World_Dataset_and_ICCV_2023_paper.html'>FSENet</a></td>
    <td class="tg-c3ow">SD7K</td>
    <td class="tg-c3ow">10.60</td>
    <td class="tg-c3ow">28.98</td>
    <td class="tg-c3ow">0.93</td>
    <td class="tg-c3ow">17.56</td>
    <td class="tg-c3ow">23.60 </td>
    <td class="tg-c3ow">0.85</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">10.00</td>
    <td class="tg-c3ow">28.67</td>
    <td class="tg-c3ow">0.96</td>
  </tr>
</tbody>
</tbody>
  <tr>
    <td class="tg-c3ow">CVPR'24</td>
    <td class="tg-c3ow"><a href='https://arxiv.org/pdf/2405.04408'>DocRes</a></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">27.14</td>
    <td class="tg-c3ow">0.900</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">23.02</td>
    <td class="tg-c3ow">0.908</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">21.64</td>
    <td class="tg-c3ow">0.937</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
</tbody>
</table>


## 3. Dewarping
Dewarping, also referred to as geometric rectification, aims to rectify document images that suffer from curves, folds, crumples, perspective/affine deformation and other geometric distortions.

### 3.1 Papers
|Year|Venue|Title|Repo|
|----|----|-----|----|
|2018|CVPR|[DocUNet: Document Image Unwarping via A Stacked U-Net](https://openaccess.thecvf.com/content_cvpr_2018/papers/Ma_DocUNet_Document_Image_CVPR_2018_paper.pdf)||
|2019|TOG|[Document Rectification and Illumination Correction using a Patch-based CNN](https://arxiv.org/pdf/1909.09470.pdf)|[Code](https://github.com/xiaoyu258/DocProj)|
|2019|ICCV|[DewarpNet: Single-Image Document Unwarping With Stacked 3D and 2D Regression Networks](https://openaccess.thecvf.com/content_ICCV_2019/papers/Das_DewarpNet_Single-Image_Document_Unwarping_With_Stacked_3D_and_2D_Regression_ICCV_2019_paper.pdf)|[Code](https://github.com/cvlab-stonybrook/DewarpNet)|[Link](https://drive.google.com/drive/folders/1aPfQHGrGxpuIbYLONydbSkGNygRX2z2P?usp=sharing)|
|2020|PR|[Geometric Rectification of Document Images using Adversarial Gated Unwarping Network](https://www.sciencedirect.com/science/article/pii/S0031320320303794)||
|2020|ECCV|[Can You Read Me Now? Content Aware Rectification using Angle Supervision](https://arxiv.org/pdf/2008.02231.pdf)||
|2020|DAS|[Dewarping Document Image by Displacement Flow Estimation with Fully Convolutional Network](https://arxiv.org/pdf/2104.06815.pdf)|[Code](https://github.com/gwxie/Dewarping-Document-Image-By-Displacement-Flow-Estimation)|
|2021|ACM MM|[DocTr: Document Image Transformer for Geometric Unwarping and Illumination Correction](https://arxiv.org/pdf/2110.12942.pdf)|[Code](https://github.com/fh2019ustc/DocTr)|
|2021|ICCV|[End-to-end Piece-wise Unwarping of Document Images](https://openaccess.thecvf.com/content/ICCV2021/papers/Das_End-to-End_Piece-Wise_Unwarping_of_Document_Images_ICCV_2021_paper.pdf)|[Code](https://github.com/sagniklp/PiecewiseUnwarp)|
|2021|ICDAR|[Document Dewarping with Control Points](https://arxiv.org/pdf/2203.10543.pdf)|[Code](https://github.com/gwxie/Document-Dewarping-with-Control-Points)|
|2022|CVPR|[Fourier Document Restoration for Robust Document Dewarping and Recognition](https://openaccess.thecvf.com/content/CVPR2022/papers/Xue_Fourier_Document_Restoration_for_Robust_Document_Dewarping_and_Recognition_CVPR_2022_paper.pdf)|||
|2022|CVPR|[Revisiting Document Image Dewarping by Grid Regularization](https://openaccess.thecvf.com/content/CVPR2022/papers/Jiang_Revisiting_Document_Image_Dewarping_by_Grid_Regularization_CVPR_2022_paper.pdf)||
|2022|ACM MM|[Marior: Margin Removal and Iterative Content Rectification for Document Dewarping in the Wild](https://arxiv.org/pdf/2207.11515.pdf)||
|2022|SIGGRAPH|[Learning From Documents in the Wild to Improve Document Unwarping](https://dl.acm.org/doi/pdf/10.1145/3528233.3530756)|[Code](https://github.com/cvlab-stonybrook/PaperEdge)|
|2022|ECCV|[Geometric Representation Learning for Document Image Rectification](https://arxiv.org/pdf/2210.08161.pdf)|[Code](https://github.com/fh2019ustc/DocGeoNet)|
|2022|ECCV|[Learning an Isometric Surface Parameterization for Texture Unwrapping](https://www.ecva.net/papers/eccv_2022/papers_ECCV/papers/136970568.pdf)|[Code](https://github.com/cvlab-stonybrook/Iso-UVField)|
|2022|Arxiv|[DocScanner: Robust Document Image Rectification with Progressive Learning](https://arxiv.org/abs/2110.14968)|[Code](https://github.com/fh2019ustc/DocScanner)|
|2022|ICPR|[Document Image Rectification in Complex Scene Using Stacked Siamese Networks](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=9956331&casa_token=3EP6PWPjea0AAAAA:5-ijMq2DXm9fcefC_Y4ryNM3d4deZpi_u6EOIjmZ6K-qp4tNwsHq2Y81xbr42aczVvyuR3xZiT_h)||
|2023|Arxiv|[Geometric Rectification of Creased Document Images based on Isometric Mapping](https://arxiv.org/abs/2212.08365)||
|2023|IJDAR|[Adaptive Dewarping of Severely Warped Camera-captured Document Images Based on Document Map Generation](https://link.springer.com/content/pdf/10.1007/s10032-022-00425-4.pdf?pdf=button)||
|2023|TMM|[Deep Unrestricted Document Image Rectification](https://arxiv.org/abs/2304.08796)|[Code](https://github.com/fh2019ustc/DocTr-Plus)|
|2023|Arxiv|[Neural Document Unwarping using Coupled Grids](https://arxiv.org/pdf/2302.02887.pdf)||
|2023|IJDAR|[Inv3D: A High-resolution 3D Invoice Dataset for Template-guided Single-image Document Unwarping](https://link.springer.com/article/10.1007/s10032-023-00434-x)|[Code](https://github.com/FelixHertlein/inv3d)|
|2023|Arxiv|[MataDoc: Margin and Text Aware Document Dewarping for Arbitrary Boundary](https://arxiv.org/pdf/2307.12571)||
|2023|ICCVW|[Template-guided Illumination Correction for Document Images with Imperfect Geometric Reconstruction](https://openaccess.thecvf.com/content/ICCV2023W/NIVT/papers/Hertlein_Template-Guided_Illumination_Correction_for_Document_Images_with_Imperfect_Geometric_Reconstruction_ICCVW_2023_paper.pdf)|[Code](https://github.com/FelixHertlein/illtrtemplate-model)|
|2023|ICCV|[Foreground and Text-lines Aware Document Image Rectification](https://openaccess.thecvf.com/content/ICCV2023/papers/Li_Foreground_and_Text-lines_Aware_Document_Image_Rectification_ICCV_2023_paper.pdf)|[Code](https://github.com/xiaomore/document-image-dewarping)|
|2023|ACM TOG|[Layout-Aware Single-Image Document Flatening](https://dl.acm.org/doi/pdf/10.1145/3627818)|[Code](https://github.com/BunnySoCrazy/LA-DocFlatten)|[Link](https://github.com/BunnySoCrazy/LA-DocFlatten)|
|2023|WACV|[DocReal: Robust Document Dewarping of Real-Life Images via Attention-Enhanced Control Point Prediction](https://openaccess.thecvf.com/content/WACV2024/papers/Yu_DocReal_Robust_Document_Dewarping_of_Real-Life_Images_via_Attention-Enhanced_Control_WACV_2024_paper.pdf)|[Code](https://github.com/irisXcoding/DocReal)|
|2023|TCSVT|[Rethinking Supervision in Document Unwarping: A Self-consistent Flow-free Approach](https://ieeexplore.ieee.org/abstract/document/10327775)|||
|2023|SIGGRAPH|[UVDoc: Neural Grid-based Document Unwarping](https://dl.acm.org/doi/fullHtml/10.1145/3610548.3618174)|[Code](https://github.com/tanguymagne/UVDoc)|
|2023|Arxiv|[Polar-Doc: One-Stage Document Dewarping with Multi-Scope Constraints under Polar Representation](https://arxiv.org/abs/2312.07925)||
|2024|ICASSP|[Efficient Joint Rectification of Photometric and Geometric Distortions in Document Images](https://ieeexplore.ieee.org/abstract/document/10447446)||
|2024|ICDAR|Coarse-to-Fine Document Image Registration for Dewarping|[Code](https://github.com/hanquansanren/DIRD)|
|2024|CVPR|[DocRes: A Generalist Model Toward Unifying Document Image Restoration Tasks](https://arxiv.org/abs/2405.04408)|[Code](https://github.com/ZZZHANG-jx/DocRes)|
|2024|IJDAR|[Am I readable? Transfer learning based document image rectification](https://link.springer.com/article/10.1007/s10032-024-00476-9)||




### 3.2 Dataset
|Dataset|Num.|Type|Example|Download/Codes|
|----|----|----|----|----|
|[DocUNet](https://openaccess.thecvf.com/content_cvpr_2018/papers/Ma_DocUNet_Document_Image_CVPR_2018_paper.pdf)|130|Real|[Example](./Dataset_image/docunet/docunet.md)|[Link](https://www3.cs.stonybrook.edu/~cvl/docunet.html)|
|[Doc3D](https://openaccess.thecvf.com/content_ICCV_2019/papers/Das_DewarpNet_Single-Image_Document_Unwarping_With_Stacked_3D_and_2D_Regression_ICCV_2019_paper.pdf)|100K|Synth|-|[Link](https://github.com/cvlab-stonybrook/doc3D-dataset)|
|[DIW](https://dl.acm.org/doi/abs/10.1145/3528233.3530756)|5K|Real|[Example](./Dataset_image/diw/readme.md)|[Link](https://github.com/cvlab-stonybrook/PaperEdge)|
|[WarpDoc](https://openaccess.thecvf.com/content/CVPR2022/papers/Xue_Fourier_Document_Restoration_for_Robust_Document_Dewarping_and_Recognition_CVPR_2022_paper.pdf)|1020|Real|[Example](./Dataset_image/warpdoc/warpdoc.md)|[Link](https://sg-vilab.github.io/event/warpdoc)|
|[DIR300](https://arxiv.org/pdf/2210.08161.pdf)|300|Real|[Example](./Dataset_image/dir300/readme.md)|[Link](https://drive.google.com/drive/folders/1yySouQQ3BlH7OjnUhq4CLuvpX2KXtifX)|
|[Inv3D](https://link.springer.com/article/10.1007/s10032-023-00434-x)|25K|Synth|[Example](./Dataset_image/inv3d/readme.md)|[Link](https://github.com/FelixHertlein/inv3d)|
|[Inv3DReal](https://link.springer.com/article/10.1007/s10032-023-00434-x)|360|Real|[Example](./Dataset_image/inv3d_real/readme.md)|[Link](https://github.com/FelixHertlein/inv3d-model/tree/main/input/inv3d_real/data)|
|[DICP](https://arxiv.org/pdf/2203.10543.pdf)|-|Synth|-|[Link](https://github.com/gwxie/Document-Dewarping-with-Control-Points)|
|[DIF](https://arxiv.org/pdf/2104.06815.pdf)|-|Synth|-|[Link](https://github.com/gwxie/Distorted-Image-With-Flow)|
|[Simulated Paper](https://dl.acm.org/doi/pdf/10.1145/3627818)|90K|Synth|-|[Link](https://github.com/BunnySoCrazy/LA-DocFlatten)|
|[DocReal](https://openaccess.thecvf.com/content/WACV2024/html/Yu_DocReal_Robust_Document_Dewarping_of_Real-Life_Images_via_Attention-Enhanced_Control_WACV_2024_paper.html)|200|Real|[Example](./Dataset_image/docreal/readme.md)|[Link](https://github.com/irisXcoding/DocReal)|
|[UVDoc](https://dl.acm.org/doi/fullHtml/10.1145/3610548.3618174)|20K|Synth|[Example](./Dataset_image/uvdoc/readme.md)|[Link](https://github.com/tanguymagne/UVDoc-Dataset)|


### 3.3 SOTA
<table class="tg">
<thead>
  <tr>
    <th class="tg-c3ow" rowspan="2">Venue</th>
    <th class="tg-c3ow" rowspan="2">Method</th>
    <th class="tg-c3ow" colspan="3">DocUNet (130)</th>
    <th class="tg-c3ow" colspan="3">DIR300 (300)</th>
    <th class="tg-c3ow" colspan="2">DocReal (200)</th>
    <th class="tg-c3ow" colspan="2">UVDoc (50)</th>
  </tr>
  <tr>
    <th class="tg-c3ow">MS-SSIM↑</th>
    <th class="tg-c3ow">LD↓</th>
    <th class="tg-c3ow">AD↓</th>
    <th class="tg-c3ow">MS-SSIM↑</th>
    <th class="tg-c3ow">LD↓</th>
    <th class="tg-c3ow">AD↓</th>
    <th class="tg-c3ow">MS-SSIM↑</th>
    <th class="tg-c3ow">LD↓</th>
    <th class="tg-c3ow">MS-SSIM↑</th>
    <th class="tg-c3ow">AD↓</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-c3ow">ICCV'19</td>
    <td class="tg-c3ow"><a href="https://openaccess.thecvf.com/content_ICCV_2019/html/Das_DewarpNet_Single-Image_Document_Unwarping_With_Stacked_3D_and_2D_Regression_ICCV_2019_paper.html">DewarpNet</a></td>
    <td class="tg-c3ow">0.474</td>
    <td class="tg-c3ow">8.39</td>
    <td class="tg-c3ow">0.426</td>
    <td class="tg-c3ow">0.492</td>
    <td class="tg-c3ow">13.94</td>
    <td class="tg-c3ow">0.331</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">0.589</td>
    <td class="tg-c3ow">0.193</td>
  </tr>
  <tr>
    <td class="tg-c3ow">DAS'20</td>
    <td class="tg-c3ow"><a href="https://arxiv.org/pdf/2104.06815.pdf">FCN-based</a></td>
    <td class="tg-c3ow">0.448</td>
    <td class="tg-c3ow">7.84</td>
    <td class="tg-c3ow">0.434</td>
    <td class="tg-c3ow">0.503</td>
    <td class="tg-c3ow">9.75</td>
    <td class="tg-c3ow">0.331</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>

  <tr>
    <td class="tg-c3ow">ICCV'21</td>
    <td class="tg-c3ow"><a href="https://openaccess.thecvf.com/content/ICCV2021/papers/Das_End-to-End_Piece-Wise_Unwarping_of_Document_Images_ICCV_2021_paper.pdf">Piece-Wise</a></td>
    <td class="tg-c3ow">0.492</td>
    <td class="tg-c3ow">8.64</td>
    <td class="tg-c3ow">0.468</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-c3ow">ICDAR'21</td>
    <td class="tg-c3ow"><a href="https://arxiv.org/pdf/2203.10543.pdf">DDCP</a></td>
    <td class="tg-c3ow">0.473</td>
    <td class="tg-c3ow">8.99</td>
    <td class="tg-c3ow">0.453</td>
    <td class="tg-c3ow">0.552</td>
    <td class="tg-c3ow">10.95</td>
    <td class="tg-c3ow">0.357</td>
    <td class="tg-c3ow">0.46</td>
    <td class="tg-c3ow">16.04</td>
    <td class="tg-c3ow">0.585</td>
    <td class="tg-c3ow">0.290</td>
  </tr>
  <tr>
    <td class="tg-c3ow">MM'21</td>
    <td class="tg-c3ow"><a href="https://arxiv.org/pdf/2110.12942.pdf">DocTr</a></td>
    <td class="tg-c3ow">0.511</td>
    <td class="tg-c3ow">7.76</td>
    <td class="tg-c3ow">0.396</td>
    <td class="tg-c3ow">0.616</td>
    <td class="tg-c3ow">7.21</td>
    <td class="tg-c3ow">0.254</td>
    <td class="tg-c3ow">0.55</td>
    <td class="tg-c3ow">12.66</td>
    <td class="tg-c3ow">0.697</td>
    <td class="tg-c3ow">0.160</td>
  </tr>
  <tr>
    <td class="tg-c3ow">CVPR'22</td>
    <td class="tg-c3ow"><a href="https://openaccess.thecvf.com/content/CVPR2022/papers/Jiang_Revisiting_Document_Image_Dewarping_by_Grid_Regularization_CVPR_2022_paper.pdf">RDGR</a></td>
    <td class="tg-c3ow">0.497</td>
    <td class="tg-c3ow">8.51</td>
    <td class="tg-c3ow">0.461</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">0.610</td>
    <td class="tg-c3ow">0.280</td>
  </tr>
  <tr>
    <td class="tg-c3ow">MM'22</td>
    <td class="tg-c3ow"><a href="https://arxiv.org/pdf/2207.11515.pdf">Marior</a></td>
    <td class="tg-c3ow">0.478</td>
    <td class="tg-c3ow">7.27</td>
    <td class="tg-c3ow">0.403</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-c3ow">ECCV'22</td>
    <td class="tg-c3ow"><a href="https://arxiv.org/pdf/2210.08161.pdf">DocGeoNet</a></td>
    <td class="tg-c3ow">0.504</td>
    <td class="tg-c3ow">7.71</td>
    <td class="tg-c3ow">0.380</td>
    <td class="tg-c3ow">0.638</td>
    <td class="tg-c3ow">6.40</td>
    <td class="tg-c3ow">0.242</td>
    <td class="tg-c3ow">0.55</td>
    <td class="tg-c3ow">12.22</td>
    <td class="tg-c3ow">0.706</td>
    <td class="tg-c3ow">0.168</td>
  </tr>
  <tr>
    <td class="tg-c3ow">SIGGRAPH'22</td>
    <td class="tg-c3ow"><a href="https://dl.acm.org/doi/pdf/10.1145/3528233.3530756">PaperEdge</a></td>
    <td class="tg-c3ow">0.473</td>
    <td class="tg-c3ow">7.81</td>
    <td class="tg-c3ow">0.392</td>
    <td class="tg-c3ow">0.583</td>
    <td class="tg-c3ow">8.00</td>
    <td class="tg-c3ow">0.255</td>
    <td class="tg-c3ow">0.52</td>
    <td class="tg-c3ow">11.46</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-c3ow">Arxiv'22</td>
    <td class="tg-c3ow"><a href="https://arxiv.org/abs/2110.14968">DocScanner-L</a></td>
    <td class="tg-c3ow">0.518</td>
    <td class="tg-c3ow">7.45</td>
    <td class="tg-c3ow">0.334</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr> 
  <tr>
    <td class="tg-c3ow">ICCV'23</td>
    <td class="tg-c3ow"><a href="https://openaccess.thecvf.com/content/ICCV2023/papers/Li_Foreground_and_Text-lines_Aware_Document_Image_Rectification_ICCV_2023_paper.pdf">Li et al.</td>
    <td class="tg-c3ow">0.497</td>
    <td class="tg-c3ow">8.43</td>
    <td class="tg-c3ow">0.376</td>
    <td class="tg-c3ow">0.607</td>
    <td class="tg-c3ow">7.68</td>
    <td class="tg-c3ow">0.244</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-c3ow">WACV'23</td>
    <td class="tg-c3ow"><a href="https://openaccess.thecvf.com/content/WACV2024/papers/Yu_DocReal_Robust_Document_Dewarping_of_Real-Life_Images_via_Attention-Enhanced_Control_WACV_2024_paper.pdf">DocReal</a></td>
    <td class="tg-c3ow">0.50</td>
    <td class="tg-c3ow">7.03</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"><b>0.56</b></td>
    <td class="tg-c3ow"><b>9.83</b></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-c3ow">TCSVT'23</td>
    <td class="tg-c3ow"><a href="https://ieeexplore.ieee.org/abstract/document/10327775">DRNet</a></td>
    <td class="tg-c3ow">0.51</td>
    <td class="tg-c3ow">7.42</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-c3ow">TMM'23</td>
    <td class="tg-c3ow"><a href="https://arxiv.org/abs/2304.08796">DocTr++</a></td>
    <td class="tg-c3ow">0.51</td>
    <td class="tg-c3ow">7.54</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">0.45</td>
    <td class="tg-c3ow">19.88</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-c3ow">Arxiv'23</td>
    <td class="tg-c3ow"><a href="https://arxiv.org/abs/2312.07925">Polar-Doc</a></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">0.605</td>
    <td class="tg-c3ow">7.17</td>
    <td class="tg-c3ow">0.206</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-c3ow">Arxiv'23</td>
    <td class="tg-c3ow"><a href="https://arxiv.org/pdf/2307.12571.pdf">MetaDoc</a></td>
    <td class="tg-c3ow">0.502</td>
    <td class="tg-c3ow">7.42</td>
    <td class="tg-c3ow">0.315</td>
    <td class="tg-c3ow">0.638</td>
    <td class="tg-c3ow">5.75</td>
    <td class="tg-c3ow"><b>0.178</b></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-c3ow">SIGGRAPH'23</td>
    <td class="tg-c3ow"><a href="https://dl.acm.org/doi/fullHtml/10.1145/3610548.3618174">UVDoc</a></td>
    <td class="tg-c3ow"><b>0.544</b></td>
    <td class="tg-c3ow">6.83</td>
    <td class="tg-c3ow">0.315</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"><b>0.785</b></td>
    <td class="tg-c3ow"><b>0.119</b></td>
  </tr>
  <tr>
    <td class="tg-c3ow">ACM TOG'23</td>
    <td class="tg-c3ow"><a href="https://dl.acm.org/doi/pdf/10.1145/3627818">LA-DocFlatten</a></td>
    <td class="tg-c3ow">0.526</td>
    <td class="tg-c3ow"><b>6.72</b></td>
    <td class="tg-c3ow"><b>0.300</b></td>
    <td class="tg-c3ow">0.651</td>
    <td class="tg-c3ow"><b>5.70</b></td>
    <td class="tg-c3ow">0.195</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-c3ow">CVPR'24</td>
    <td class="tg-c3ow"><a href="https://arxiv.org/pdf/2405.04408">DocRes</a></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">0.626</td>
    <td class="tg-c3ow">6.83</td>
    <td class="tg-c3ow">0.241</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-c3ow">IJDAR'24</td>
    <td class="tg-c3ow"><a href="https://link.springer.com/article/10.1007/s10032-024-00476-9">DocTLNet</a></td>
    <td class="tg-c3ow">0.51</td>
    <td class="tg-c3ow"> 6.70</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"><b>0.658</b></td>
    <td class="tg-c3ow">5.75</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
</tbody>
</table>

- Note that the 127th and 128th distorted images in DocUNet benchmark are rotated by 180 degrees, which do not match the ground truth documents. The performance reported here is based on corrected data.
- Note that the UVDoc benchmark reported in our repository is based on the full UVDoc benchmark dataset (reported on the [official github page](https://github.com/tanguymagne/UVDoc)). The results in the paper used only half of the UVDoc benchmark.


## 4. Deblur

### 4.1 Papers
|Year|Venue|Title|Repo|
|----|----|-----|----|
|2019|NIPS|[SVDocNet: Spatially Variant U-Net for Blind Document Deblurring](https://openreview.net/forum?id=Hyx3f65qLS)||
|2019|MTA|[DeepDeblur: text image recovery from blur to sharp](https://link.springer.com/article/10.1007/s11042-019-7251-y)|[code](https://github.com/meijianhan/DeepDeblur)|
|2020|TPAMI|[DE-GAN: A Conditional Generative Adversarial Network for Document Enhancement](https://ieeexplore.ieee.org/document/9187695)|[code](https://github.com/dali92002/DE-GAN)|
|2021|ICCV|[End-to-End Unsupervised Document Image Blind Denoising](https://openaccess.thecvf.com/content/ICCV2021/html/Gangeh_End-to-End_Unsupervised_Document_Image_Blind_Denoising_ICCV_2021_paper.html)||
|2023|ACM MM|[DocDiff: Document Enhancement via Residual Diffusion ModelscDiff](https://arxiv.org/abs/2305.03892)|[code](https://github.com/Royalvice/DocDiff)|
|2024|AAAI|[DocNLC: A Document Image Enhancement Framework with Normalized and Latent Contrastive Representation for Multiple Degradations](https://ojs.aaai.org/index.php/AAAI/article/view/28366)|[Code](https://github.com/RylonW/DocNLC)|
|2024|CVPR|[DocRes: A Generalist Model Toward Unifying Document Image Restoration Tasks](https://arxiv.org/abs/2405.04408)|[Code](https://github.com/ZZZHANG-jx/DocRes)|
|2024|Arxiv|[NAF-DPM: A Nonlinear Activation-Free Diffusion Probabilistic Model for Document Enhancement](https://arxiv.org/abs/2404.05669)|[Code](https://github.com/ispamm/NAF-DPM)|

### 4.2 Datasets
|Dataset|Num. (train/test)|Type|Example|Download|
|----|----|----|----|----|
|[TDD (text deblur dataset)](https://www.fit.vut.cz/research/publication-file/10922/hradis15CNNdeblurring.pdf)|67.6K (66K/1.6K)|Synth|[Example](./Dataset_image/tdd/tdd.md)|[Link](http://www.fit.vutbr.cz/~ihradis/CNN-Deblur/)|

### 4.3 SOTA
Comding Soon ...

## 5. Binarization

### 5.1 Papers
|Year|Venue|Title|Repo|
|----|----|-----|----|
|2019|PR|[DeepOtsu: Document enhancement and binarization using iterative deep learning](https://www.sciencedirect.com/science/article/pii/S0031320319300330)|[code](https://www.ai.rug.nl/~sheng/DeepOtsu.html)|
|2021|PR|[Complex image processing with less data—Document image binarization by integrating multiple pre-trained U-Net modules](https://www.sciencedirect.com/science/article/pii/S0031320320303800)|[code](https://www.ai.rug.nl/~sheng/DeepOtsu.html)|
|2022|PR|[Two-Stage Generative Adversarial Networks for Binarization of Color Document Images](https://www.sciencedirect.com/science/article/pii/S0031320322002916)|[code](https://github.com/opensuh/DocumentBinarization)|
|2023|PR|[GDB: Gated Convolutions-based Document Binarization](https://www.sciencedirect.com/science/article/pii/S0031320323006878)|[code](https://github.com/Royalvice/GDB)|
|2023|ACM MM|[DocDiff: Document Enhancement via Residual Diffusion ModelscDiff](https://arxiv.org/abs/2305.03892)|[code](https://github.com/Royalvice/DocDiff)|
|2023|ICDAR|[ColDBin: Cold Diffusion for Document Image Binarization](https://link.springer.com/chapter/10.1007/978-3-031-41734-4_13)|[code](https://github.com/saifullah3396/coldbin)|
|2023|IF|[A Novel Degraded Document Binarization Model through Vision Transformer Network](https://www.sciencedirect.com/science/article/pii/S1566253522002597)||
|2023|Arxiv|[DocBinFormer: A Two-Level Transformer Network for Effective Document Image Binarization](https://arxiv.org/pdf/2312.03568.pdf)||
|2024|AAAI|[DocNLC: A Document Image Enhancement Framework with Normalized and Latent Contrastive Representation for Multiple Degradations](https://ojs.aaai.org/index.php/AAAI/article/view/28366)|[Code](https://github.com/RylonW/DocNLC)|
|2024|CVPR|[DocRes: A Generalist Model Toward Unifying Document Image Restoration Tasks](https://arxiv.org/abs/2405.04408)|[Code](https://github.com/ZZZHANG-jx/DocRes)|
|2024|Arxiv|[NAF-DPM: A Nonlinear Activation-Free Diffusion Probabilistic Model for Document Enhancement](https://arxiv.org/abs/2404.05669)|[Code](https://github.com/ispamm/NAF-DPM)|


### 5.2 Datasets

|Dataset|Num.|Type|Example|Download|
|----|----|----|----|----|
|[DocEng 2019]()|15|Real|[Example](./Dataset_image/doceng/doceng.md)|[Link](https://github.com/hyyh1314/RDD)|
|[DocEng 2020]()|32|Real|[Example](./Dataset_image/doceng/doceng.md)|[Link](https://github.com/hyyh1314/RDD)|
|[DocEng 2021]()|222|Real|[Example](./Dataset_image/doceng/doceng.md)|[Link](https://github.com/hyyh1314/RDD)|
|[DocEng 2022]()|80|Real|[Example](./Dataset_image/doceng/doceng.md)|[Link](https://github.com/hyyh1314/RDD)|
|[DIBCO 2009]()|10|Real|[Example](./Dataset_image/dibco/readme.md)|[Link](http://users.iit.demokritos.gr/~bgat/DIBCO2009/benchmark/)|
|[H-DIBCO 2010]()|10|Real|[Example](./Dataset_image/dibco/readme.md)|[Link](http://users.iit.demokritos.gr/~bgat/H-DIBCO2010/benchmark/)|
|[DIBCO 2011]()|16|Real|[Example](./Dataset_image/dibco/readme.md)|[Link](http://utopia.duth.gr/~ipratika/DIBCO2011/benchmark/)|
|[H-DIBCO 2012]()|14|Real|[Example](./Dataset_image/dibco/readme.md)|[Link](http://utopia.duth.gr/~ipratika/HDIBCO2012/benchmark/)|
|[DIBCO 2013]()|16|Real|[Example](./Dataset_image/dibco/readme.md)|[Link](http://utopia.duth.gr/~ipratika/DIBCO2013/benchmark/)|
|[H-DIBCO 2014]()|10|Real|[Example](./Dataset_image/dibco/readme.md)|[Link](http://users.iit.demokritos.gr/~bgat/HDIBCO2014/benchmark/)|
|[H-DIBCO 2016]()|10|Real|[Example](./Dataset_image/dibco/readme.md)|[Link](http://vc.ee.duth.gr/h-dibco2016/benchmark/)|
|[DIBCO 2017]()|20|Real|[Example](./Dataset_image/dibco/readme.md)|[Link](http://vc.ee.duth.gr/dibco2017/benchmark/)|
|[DIBCO 2018]()|10|Real|[Example](./Dataset_image/dibco/readme.md)|[Link](http://vc.ee.duth.gr/h-dibco2018/benchmark/)|
|[DIBCO 2019]()|10|Real|[Example](./Dataset_image/dibco/readme.md)|[Link](https://vc.ee.duth.gr/dibco2019/benchmark/)|
|[Bickly-diary](https://dl.acm.org/doi/abs/10.1145/1816123.1816161)|7|Real|[Example](./Dataset_image/bickly/readme.md)|[Link](https://1drv.ms/f/s!Ak15mSdV3Wy4iY4sW5gm7ak4aWjtFQ?e=1l7vRi)|
|[Synchromedia Multispectral (MSI)](https://www.sciencedirect.com/science/article/pii/S0031320313000642)|240|Real|[Example](./Dataset_image/msi/readme.md)|[Link](https://tc11.cvc.uab.es/datasets/SMADI_1)|
|[Persian Heritage Image Binarization （PHIBD）](https://ieeexplore.ieee.org/abstract/document/6528442)|15|Real|[Example](./Dataset_image/phibd/readme.md)|[Link](http://www.iapr-tc11.org/mediawiki/index.php/Persian_Heritage_Image_Binarization_Dataset_(PHIBD_2012))|
|[Palm Leaf]()|50|Real|[Example](./Dataset_image/palm_leaf/readme.md)|[Link](http://amadi.univ-lr.fr/ICFHR2016_Contest/index.php/download-123)|
|[NoiseOffice]()|216|Synth|[Example](./Dataset_image/noise_office/readme.md)|[Link](https://archive.ics.uci.edu/dataset/318/noisyoffice)|
|[LRDE Document Binarization Dataset](https://link.springer.com/article/10.1007/s10032-013-0209-0)|125|Real|-|[Link](https://www.lrde.epita.fr/wiki/Olena/DatasetDBD)|
|[Shipping label dataset](https://www.sciencedirect.com/science/article/pii/S0031320322002916)|1082|Real|[Example](./Dataset_image/shipping/shipping.md)|[Link](https://www.dropbox.com/sh/gqqugvclzltfldt/AACNELpHwTW-1bHLZzipxQWja?dl=0)|


### 5.3 SOTA
Coming Soon ...


## ⭐ Star Rising
[![Star Rising](https://api.star-history.com/svg?repos=ZZZHANG-jx/Recommendations-Document-Image-Processing&type=Timeline)](https://star-history.com/#ZZZHANG-jx/Recommendations-Document-Image-Processing&Timeline)
