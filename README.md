## Recommendations of Document Image Processing
<h4 align="center">A curated list of resources dedicated to Document Image Processing</h4>


## Contents
- [1. Appearance Enhancement](#1appearance)
  - [1.1 Papers](#11-papers)
  - [1.2 Datasets](#12-datasets)
  - [1.3 APPs](#13-apps)
  - [1.4 SOTA](#14-sota)
- [2. Deshadow](#2-deshadow)
  - [2.1 Papers](#21-papers)
  - [2.2 Datasets](#22-datasets)
  - [2.3 SOTA](#23-sota)
- [3. Dewarping](#3-dewarping)
  - [3.1 Papers](#31-papers)
  - [3.2 Datasets](#32-dataset)
  - [3.3 SOTA](#33-sota)
- [4. Deblur](#4-deblur)
  - [4.1 Papers](#41-papers)
  - [4.2 Datasets](#42-datasets)
  - [4.3 SOTA](#43-sota)
- [5. Binarization](#5-binarization)
  - [5.1 Papers](#51-papers)
  - [5.2 Datasets](#52-datasets)
  - [5.3 SOTA](#53-sota)

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


### 1.2 Datasets

|Dataset|Num. (train/test)|Type|Example|Download|
|----|----|----|----|----|
|[Doc3DShade](https://arxiv.org/abs/2011.14447)|90K|Sythetic|[Example](./Dataset_image/doc3dshade/doc3dshade.md)|[Link](https://github.com/cvlab-stonybrook/DocIIW)|
|[DocProj](https://dl.acm.org/doi/abs/10.1145/3355089.3356563)|2450|Sythetic|[Example](./Dataset_image/docproj/docproj.md)|[Link](https://github.com/xiaoyu258/DocProj)|
|[DocUNet from DocAligner](https://openaccess.thecvf.com/content_cvpr_2018/html/Ma_DocUNet_Document_Image_CVPR_2018_paper.html)|130|Real|[Example](./Dataset_image/docunet_docaligner/docunet_docaligner.md)|[Link](https://www3.cs.stonybrook.edu/~cvl/docunet.html)|
|[RealDAE](https://ieeexplore.ieee.org/abstract/document/10268585/)|600 (450/150)|Real|[Example](./Dataset_image/realdae/realdae.md)|[Link](https://github.com/ZZZHANG-jx/GCDRNet)|
|[Inv3D](https://link.springer.com/article/10.1007/s10032-023-00434-x)|25K|Sythetic|[Example](./Dataset_image/inv3d/inv3d.md)|[Link](https://github.com/FelixHertlein/inv3d)|

### 1.3 Apps

[CamScanner](https://www.camscanner.com/), [Adobe Acrobat](https://helpx.adobe.com/acrobat/using/enhance-camera-images.html), [Lenovo Smart Scanner](https://static.xue.lenovomm.com/scannerpc.html), [Quark](https://www.quark.cn/)

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
    <td class="tg-c3ow">DocProj</td>
    <td class="tg-c3ow">DocProj</td>
    <td class="tg-c3ow">0.7098</td>
    <td class="tg-c3ow">14.71</td>
    <td class="tg-c3ow">0.8684</td>
    <td class="tg-c3ow">19.35</td>
  </tr>
  <tr>
    <td class="tg-c3ow">BMVC'20</td>
    <td class="tg-c3ow">Das et al.</td>
    <td class="tg-c3ow">Doc3DShade</td>
    <td class="tg-c3ow">0.7276</td>
    <td class="tg-c3ow">16.42</td>
    <td class="tg-c3ow">0.8633</td>
    <td class="tg-c3ow">19.87</td>
  </tr>
  <!-- <tr>
    <td class="tg-c3ow">ICCV'21</td>
    <td class="tg-c3ow">DewarpNet</td>
    <td class="tg-c3ow">Doc3D</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr> -->
  <tr>
    <td class="tg-c3ow">ACM MM'21</td>
    <td class="tg-c3ow">DocTr</td>
    <td class="tg-c3ow">DocProj</td>
    <td class="tg-c3ow">0.7067</td>
    <td class="tg-c3ow">15.78</td>
    <td class="tg-c3ow">0.7925</td>
    <td class="tg-c3ow">18.62</td>
  </tr>
  <tr>
    <td class="tg-c3ow">ACM MM'22</td>
    <td class="tg-c3ow">UDoc-GAN</td>
    <td class="tg-c3ow">DocProj</td>
    <td class="tg-c3ow">0.6833</td>
    <td class="tg-c3ow">14.29</td>
    <td class="tg-c3ow">0.7558</td>
    <td class="tg-c3ow">16.43</td>
  </tr>
  <tr>
    <td class="tg-c3ow">TAI'23</td>
    <td class="tg-c3ow">GCDRNet</td>
    <td class="tg-c3ow">RealDAE</td>
    <td class="tg-c3ow">0.7658</td>
    <td class="tg-c3ow">17.09</td>
    <td class="tg-c3ow">0.9423</td>
    <td class="tg-c3ow">24.42</td>
  </tr>
</tbody>
</table>


## 2. Deshadow
Deshadowing aims to eliminate shadows caused by occlusion to obtain shadow-free document images.

### 2.1 Papers
|Year|Venue|Title|Repo|
|----|----|-----|----|
|2018|CVPR|[Document Enhancement Using Visibility Detection](https://openaccess.thecvf.com/content_cvpr_2018/html/Kligler_Document_Enhancement_Using_CVPR_2018_paper.html)|[baidu]()|
|2020|CVPR|[BEDSR-Net A Deep Shadow Removal Network from a Single Document Image](https://openaccess.thecvf.com/content_CVPR_2020/html/Lin_BEDSR-Net_A_Deep_Shadow_Removal_Network_From_a_Single_Document_CVPR_2020_paper.html)|[Code]([http](https://github.com/IsHYuhi/BEDSR-Net_A_Deep_Shadow_Removal_Network_from_a_Single_Document_Image))|
|2022|ICPR|[Document Shadow Removal with Foreground Detection Learning From Fully Synth Images](https://ieeexplore.ieee.org/abstract/document/9897217)|[Code](https://github.com/IsHYuhi/DSRFGD)|
|2022|MERCon|[Shadow Removal for Documents with Reflective Textured Surface](https://ieeexplore.ieee.org/abstract/document/9906227)||
|2023|ICASSP|[ShaDocNet: Learning Spatial-Aware Tokens in Transformer for Document Shadow Removal](https://arxiv.org/abs/2211.16675)|[Code](https://github.com/CXH-Research/ShadocNet)|
|2023|ICASSP|[Shadow Removal of Text Document Images Using Background Estimation and Adaptive Text Enhancement](https://ieeexplore.ieee.org/abstract/document/10096115)||
|2023|ICASSP|[LP-IOANet: Efficient High Resolution Document Shadow Removal](https://arxiv.org/pdf/2303.12862.pdf)||
|2023|Optical Review|[Shadow removal from document image based on background estimation employing selective median filter and black-top-hat transform](https://link.springer.com/article/10.1007/s10043-023-00806-y)||
|2023|CVPR|[Document Image Shadow Removal Guided by Color-Aware Background](https://openaccess.thecvf.com/content/CVPR2023/html/Zhang_Document_Image_Shadow_Removal_Guided_by_Color-Aware_Background_CVPR_2023_paper.html)|[Code](https://github.com/hyyh1314/BGShadowNet)|
|2023|arxiv|[ShaDocFormer: A Shadow-attentive Threshold Detector with Cascaded Fusion Refiner for document shadow removal](https://arxiv.org/abs/2309.06670)||
|2023|ICCV|[High-Resolution Document Shadow Removal via A Large-Scale Real-World Dataset and A Frequency-Aware Shadow Erasing Net](https://openaccess.thecvf.com/content/ICCV2023/html/Li_High-Resolution_Document_Shadow_Removal_via_A_Large-Scale_Real-World_Dataset_and_ICCV_2023_paper.html)|[code](https://github.com/CXH-Research/DocShadow-SD7K)|


### 2.2 Datasets

|Dataset|Num. (train/test)|Type|Example|Download|
|----|----|----|----|----|
|[RDD](https://openaccess.thecvf.com/content/CVPR2023/html/Zhang_Document_Image_Shadow_Removal_Guided_by_Color-Aware_Background_CVPR_2023_paper.html)|4916 (4371/545)|Real|[Example](./Dataset_image/rdd/rdd.md)|[Link](https://github.com/hyyh1314/RDD)|
|[Kligler et al.](https://openaccess.thecvf.com/content_cvpr_2018/html/Kligler_Document_Enhancement_Using_CVPR_2018_paper.html)|300|Real|[Example](./Dataset_image/kligler/kligler.md)|[baidu]()|
|[FSDSRD](https://ieeexplore.ieee.org/abstract/document/9897217)|14200|Synth|[Example](./Dataset_image/fsdsrd/fsdsrd.md)|[Link](https://github.com/IsHYuhi/DSRFGD)|
|[Jung et al.](https://link.springer.com/chapter/10.1007/978-3-030-20887-5_25)|87|Real|[Example](./Dataset_image/jung/jung.md)|[Link](https://static-content.springer.com/esm/chp%3A10.1007%2F978-3-030-20887-5_25/MediaObjects/484511_1_En_25_MOESM1_ESM.zip)|
|[OSR](https://www.mdpi.com/1424-8220/20/23/6929)|237|Real|[Example](./Dataset_image/osr/osr.md)|[Link](https://github.com/BingshuCV/DocumentShadowRemoval)|
|[WEZUT OCR](https://www.mdpi.com/1424-8220/20/10/2914)|176|Real|[Example](./Dataset_image/wezut/wezut.md)|[Link](https://okarma.zut.edu.pl/?id=dataset&L=1)|
|[SD7K](https://openaccess.thecvf.com/content/ICCV2023/html/Li_High-Resolution_Document_Shadow_Removal_via_A_Large-Scale_Real-World_Dataset_and_ICCV_2023_paper.html)|7620 (6479/760)|Real|[Example](./Dataset_image/sd7k/sd7k.md)|[Link](https://github.com/CXH-Research/DocShadow-SD7K)|


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
  </tr>
</thead>
<tbody>
</tbody>
<tbody>
  <tr>
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
  </tr>
  <tr>
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
    <td class="tg-c3ow">BGShadeNet</td>
    <td class="tg-c3ow">RDD</td>
    <td class="tg-c3ow">5.377</td>
    <td class="tg-c3ow">29.17</td>
    <td class="tg-c3ow">0.9480</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">2.219</td>
    <td class="tg-c3ow">37.58</td>
    <td class="tg-c3ow">0.983</td>    
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
    <td class="tg-c3ow">ShaDocNet</td>
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
  </tr>
  <tr>
    <td class="tg-c3ow">ICCV'23</td>
    <td class="tg-c3ow">FSENet</td>
    <td class="tg-c3ow">SD7K</td>
    <td class="tg-c3ow">14.74</td>
    <td class="tg-c3ow">25.12</td>
    <td class="tg-c3ow">0.9088</td>
    <td class="tg-c3ow">24.23</td>
    <td class="tg-c3ow">21.05</td>
    <td class="tg-c3ow">0.9005</td>
    <td class="tg-c3ow">32.47</td>
    <td class="tg-c3ow">18.25</td>
    <td class="tg-c3ow">0.9023</td>
    <td class="tg-c3ow">29.85</td>
    <td class="tg-c3ow">19.90</td>
    <td class="tg-c3ow">0.8786</td>
  </tr>
</tbody>
</table>


## 3. Dewarping
Dewarping, also referred to as geometric rectification, aims to rectify document images that suffer from curves, folds, crumples, perspective/affine deformation and other geometric distortions.

### 3.1 Papers
|Year|Venue|Title|Repo|
|----|----|-----|----|
|2023|ICCV|[Foreground and Text-lines Aware Document Image Rectification](https://openaccess.thecvf.com/content/ICCV2023/html/Li_Foreground_and_Text-lines_Aware_Document_Image_Rectification_ICCV_2023_paper.html)|[Code](https://github.com/xiaomore/Document-Image-Dewarping)|


### 3.2 Dataset
|Dataset|Num.|Type|Example|Download/Codes|
|----|----|----|----|----|
|[DocUNet](https://openaccess.thecvf.com/content_cvpr_2018/papers/Ma_DocUNet_Document_Image_CVPR_2018_paper.pdf)|130|Real|[Example](./Dataset_image/rdd/rdd.md)|[Link](https://www3.cs.stonybrook.edu/~cvl/docunet.html)|
|[Doc3D](https://openaccess.thecvf.com/content_ICCV_2019/papers/Das_DewarpNet_Single-Image_Document_Unwarping_With_Stacked_3D_and_2D_Regression_ICCV_2019_paper.pdf)|100K|Synth|[Example](./Dataset_image/rdd/rdd.md)|[Link](https://github.com/cvlab-stonybrook/doc3D-dataset)|
|[DIW](https://dl.acm.org/doi/abs/10.1145/3528233.3530756)|5K|Real|[Example](./Dataset_image/rdd.md)|[Link](https://github.com/cvlab-stonybrook/PaperEdge)|
|[WarpDoc](https://openaccess.thecvf.com/content/CVPR2022/papers/Xue_Fourier_Document_Restoration_for_Robust_Document_Dewarping_and_Recognition_CVPR_2022_paper.pdf)|1020|Real|[Example](./Dataset_image/rdd.md)|[Link](https://sg-vilab.github.io/event/warpdoc)|
|[DIR300](https://arxiv.org/pdf/2210.08161.pdf)|300|Real|[Example](./Dataset_image/rdd.md)|[Link](https://drive.google.com/drive/folders/1yySouQQ3BlH7OjnUhq4CLuvpX2KXtifX)|
|[DICP](https://arxiv.org/pdf/2203.10543.pdf)|-|Synth|[Example](./Dataset_image/rdd.md)|[Link](https://github.com/gwxie/Document-Dewarping-with-Control-Points)|
|[DIF](https://arxiv.org/pdf/2104.06815.pdf)|-|Synth|[Example](./Dataset_image/rdd.md)|[Link](https://github.com/gwxie/Distorted-Image-With-Flow)|
|[Simulated Paper](https://dl.acm.org/doi/pdf/10.1145/3627818)|90K|Synth|[Example]()|[Link](https://github.com/BunnySoCrazy/LA-DocFlatten)|


### 3.3 SOTA
<!-- ### 3.3 SOTA (all the results can be downloaded [here]()) -->

<table class="tg">
<thead>
  <tr>
    <th class="tg-c3ow" rowspan="2">Venue</th>
    <th class="tg-c3ow" rowspan="2">Method</th>
    <th class="tg-c3ow" colspan="4">DocUNet (130)</th>
    <th class="tg-c3ow" colspan="4">DIR300 (300)</th>
    <!-- <th class="tg-c3ow" colspan="4">WarpDoc</th> -->
    <!-- <th class="tg-baqh" rowspan="2">Download</th> -->
  </tr>
  <tr>
    <th class="tg-c3ow">MS-SSIM↑</th>
    <th class="tg-c3ow">LD↓</th>
    <th class="tg-c3ow">Li-D↓</th>
    <th class="tg-c3ow">AD↓</th>
    <th class="tg-c3ow">MS-SSIM↑</th>
    <th class="tg-c3ow">LD↓</th>
    <th class="tg-c3ow">Li-D↓</th>
    <th class="tg-c3ow">AD↓</th>
    <!-- <th class="tg-c3ow">MS-SSIM↑</th>
    <th class="tg-c3ow">LD↓</th>
    <th class="tg-c3ow">Li-D↓</th>
    <th class="tg-c3ow">AD↓</th> -->
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-c3ow">CVPR'18</td>
    <td class="tg-c3ow">DocUNet</td>
    <td class="tg-c3ow">0.4336</td>
    <td class="tg-c3ow">8.92</td>
    <td class="tg-c3ow">2.60</td>
    <td class="tg-c3ow">0.482</td>
    <td class="tg-c3ow">0.5322</td>
    <td class="tg-c3ow">8.80</td>
    <td class="tg-c3ow">2.62</td>
    <td class="tg-c3ow">0.328</td>
    <!-- <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td> -->
    <!-- <td class="tg-baqh"></td> -->
  </tr>
  <tr>
    <td class="tg-c3ow">ICCV'19</td>
    <td class="tg-c3ow">DewarpNet</td>
    <td class="tg-c3ow">0.4735</td>
    <td class="tg-c3ow">8.39</td>
    <td class="tg-c3ow">2.31</td>
    <td class="tg-c3ow">0.426</td>
    <td class="tg-c3ow">0.4921</td>
    <td class="tg-c3ow">13.95</td>
    <td class="tg-c3ow">2.78</td>
    <td class="tg-c3ow">0.332</td>
    <!-- <td class="tg-c3ow">0.33</td>
    <td class="tg-c3ow">31.15</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td> -->
    <!-- <td class="tg-baqh"></td> -->
  </tr>
  <!-- <tr>
    <td class="tg-c3ow">DAS'21</td>
    <td class="tg-c3ow">FCN</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <!-- <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td> -->
    <!-- <td class="tg-baqh"></td> -->
  <!-- </tr> -->
  <tr>
    <td class="tg-c3ow">ICDAR'21</td>
    <td class="tg-c3ow">DDCP</td>
    <td class="tg-c3ow">0.4729</td>
    <td class="tg-c3ow">8.99</td>
    <td class="tg-c3ow">2.19</td>
    <td class="tg-c3ow">0.427</td>
    <td class="tg-c3ow">0.5523</td>
    <td class="tg-c3ow">10.96</td>
    <td class="tg-c3ow">2.45</td>
    <td class="tg-c3ow">0.355</td>
    <!-- <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td> -->
    <!-- <td class="tg-baqh"></td> -->
  </tr>
  <tr>
    <td class="tg-c3ow">ACM MM'21</td>
    <td class="tg-c3ow">DocTr</td>
    <td class="tg-c3ow">0.5105</td>
    <td class="tg-c3ow">7.88</td>
    <td class="tg-c3ow">2.15</td>
    <td class="tg-c3ow">0.369</td>
    <td class="tg-c3ow">0.6160</td>
    <td class="tg-c3ow">7.24</td>
    <td class="tg-c3ow">2.15</td>
    <td class="tg-c3ow">0.255</td>
    <!-- <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td> -->
    <!-- <td class="tg-baqh"></td> -->
  </tr>
  <tr>
    <td class="tg-c3ow">ICCV'21</td>
    <td class="tg-c3ow">PieceWise</td>
    <td class="tg-c3ow">0.4915</td>
    <td class="tg-c3ow">8.64</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <!-- <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td> -->
    <!-- <td class="tg-baqh"></td> -->
  </tr>
  <tr>
    <td class="tg-c3ow">ECCV'22</td>
    <td class="tg-c3ow">DocGeoNet</td>
    <td class="tg-c3ow">0.5050</td>
    <td class="tg-c3ow">7.71</td>
    <td class="tg-c3ow">2.21</td>
    <td class="tg-c3ow">0.381</td>
    <td class="tg-c3ow">0.6379</td>
    <td class="tg-c3ow">6.37</td>
    <td class="tg-c3ow">2.09</td>
    <td class="tg-c3ow">0.241</td>
    <!-- <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td> -->
    <!-- <td class="tg-baqh"></td> -->
  </tr>
  <!-- <tr>
    <td class="tg-c3ow">ACM MM'22</td>
    <td class="tg-c3ow">Marior</td>
    <td class="tg-c3ow">0.4780</td>
    <td class="tg-c3ow">7.44</td>
    <td class="tg-c3ow">2.03</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <!-- <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td> -->
    <!-- <td class="tg-baqh"></td> -->
  <!-- </tr> -->
  <tr>
    <td class="tg-c3ow">CVPR'22</td>
    <td class="tg-c3ow">FDRNet</td>
    <td class="tg-c3ow">0.5420</td>
    <td class="tg-c3ow">8.21</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <!-- <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td> -->
    <!-- <td class="tg-baqh"></td> -->
  </tr>
  <tr>
    <td class="tg-c3ow">CVPR'22</td>
    <td class="tg-c3ow">RDGR</td>
    <td class="tg-c3ow">0.4968</td>
    <td class="tg-c3ow">8.51</td>
    <td class="tg-c3ow">2.12</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">0.6274</td>
    <td class="tg-c3ow">6.92</td>
    <td class="tg-c3ow">2.12</td>
    <td class="tg-c3ow">0.271</td>
    <!-- <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td> -->
    <!-- <td class="tg-baqh"></td> -->
  </tr>
  <tr>
    <td class="tg-c3ow">SIGGRAPH'22</td>
    <td class="tg-c3ow">PaperEdge</td>
    <td class="tg-c3ow">0.4724</td>
    <td class="tg-c3ow">7.99</td>
    <td class="tg-c3ow">1.83</td>
    <td class="tg-c3ow">0.392</td>
    <td class="tg-c3ow">0.5836</td>
    <td class="tg-c3ow">7.98</td>
    <td class="tg-c3ow">1.96</td>
    <td class="tg-c3ow">0.255</td>
    <!-- <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td> -->
    <!-- <td class="tg-baqh"></td> -->
  </tr>
  <!-- <tr>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">promptir</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">0.6005</td>
    <td class="tg-c3ow">6.92</td>
    <td class="tg-c3ow">1.83</td>
    <td class="tg-c3ow">0.219</td>
    <!-- <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td> -->
    <!-- <td class="tg-baqh"></td> -->
  <!-- </tr> -->
  <tr>
    <td class="tg-c3ow">ICCV'23</td>
    <td class="tg-c3ow">Li et al.</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <!-- <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td> -->
    <!-- <td class="tg-baqh"></td> -->
  <tr>
    <td class="tg-c3ow">ACM TOG'23</td>
    <td class="tg-c3ow">LA-DocFlatten</td>
    <td class="tg-c3ow">0.526</td>
    <td class="tg-c3ow">6.72</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">0.300</td>
    <td class="tg-c3ow">0.6518</td>
    <td class="tg-c3ow">5.70</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">0.195</td>
    <!-- <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td> -->
    <!-- <td class="tg-baqh"></td> -->
  </tr>
</tbody>
</table>


## 4. Deblur

### 4.1 Papers
|Year|Venue|Title|Repo|
|----|----|-----|----|
|2019|NIPS|[SVDocNet: Spatially Variant U-Net for Blind Document Deblurring](https://openreview.net/forum?id=Hyx3f65qLS)||
|2019|MTA|[DeepDeblur: text image recovery from blur to sharp](https://link.springer.com/article/10.1007/s11042-019-7251-y)|[code](https://github.com/meijianhan/DeepDeblur)|
|2020|TPAMI|[DE-GAN: A Conditional Generative Adversarial Network for Document Enhancement](https://ieeexplore.ieee.org/document/9187695)|[code](https://github.com/dali92002/DE-GAN)|
|2023|ACM MM|[DocDiff: Document Enhancement via Residual Diffusion ModelscDiff](https://arxiv.org/abs/2305.03892)|[code](https://github.com/Royalvice/DocDiff)|

### 4.2 Datasets
|Dataset|Num. (train/test)|Type|Example|Download|
|----|----|----|----|----|
|[TDD (text deblur dataset)](https://www.fit.vut.cz/research/publication-file/10922/hradis15CNNdeblurring.pdf)|67.6K (66K/1.6K)|Synthetic|[Example](./Dataset_image/tdd/tdd.md)|[Link](http://www.fit.vutbr.cz/~ihradis/CNN-Deblur/)|

### 4.3 SOTA

<table class="tg">
<thead>
  <tr>
    <th class="tg-c3ow" rowspan="2">Venue</th>
    <th class="tg-c3ow" rowspan="2">Methods</th>
    <th class="tg-c3ow" rowspan="2">Training data</th>
    <th class="tg-c3ow" colspan="2">TDD (1600)</th>
  </tr>
  <tr>
    <th class="tg-c3ow">SSIM</th>
    <th class="tg-c3ow">PSNR</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">0.5783</td>
    <td class="tg-c3ow">16.77</td>
  </tr>
  <tr>
    <td class="tg-c3ow">TPAMI'20</td>
    <td class="tg-c3ow">DE-GAN</td>
    <td class="tg-c3ow">TDD (4K)</td>
    <td class="tg-c3ow">0.9226</td>
    <td class="tg-c3ow">22.24</td>
  </tr>
  <tr>
    <td class="tg-c3ow">ACM MM'23</td>
    <td class="tg-c3ow">DocDiff (Native)-100</td>
    <td class="tg-c3ow">TDD (30K)</td>
    <td class="tg-c3ow">0.9559</td>
    <td class="tg-c3ow">24.01</td>
  </tr>
</tbody>
</table>


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


### 5.2 Datasets
https://www.sciencedirect.com/science/article/pii/S0031320318303091 dataset

|Dataset|Num.|Type|Example|Download|
|----|----|----|----|----|
|[DocEng 2019]()|15|Real|[Example](./Dataset_image/rdd.md)|[Link](https://github.com/hyyh1314/RDD)|
|[DocEng 2020]()|32|Real|[Example](./Dataset_image/rdd.md)|[Link](https://github.com/hyyh1314/RDD)|
|[DocEng 2021]()|222|Real|[Example](./Dataset_image/rdd.md)|[Link](https://github.com/hyyh1314/RDD)|
|[DocEng 2022]()|80|Real|[Example](./Dataset_image/rdd.md)|[Link](https://github.com/hyyh1314/RDD)|
|[DIBCO 2009](https://openaccess.thecvf.com/content/CVPR2023/html/Zhang_Document_Image_Shadow_Removal_Guided_by_Color-Aware_Background_CVPR_2023_paper.html)|10|Real|[Example](./Dataset_image/rdd.md)|[Link](https://github.com/hyyh1314/RDD)|
|[H-DIBCO 2010](https://openaccess.thecvf.com/content/CVPR2023/html/Zhang_Document_Image_Shadow_Removal_Guided_by_Color-Aware_Background_CVPR_2023_paper.html)|10|Real|[Example](./Dataset_image/rdd.md)|[Link](https://github.com/hyyh1314/RDD)|
|[DIBCO 2011](https://openaccess.thecvf.com/content/CVPR2023/html/Zhang_Document_Image_Shadow_Removal_Guided_by_Color-Aware_Background_CVPR_2023_paper.html)|16|Real|[Example](./Dataset_image/rdd.md)|[Link](https://github.com/hyyh1314/RDD)|
|[H-DIBCO 2012](https://openaccess.thecvf.com/content/CVPR2023/html/Zhang_Document_Image_Shadow_Removal_Guided_by_Color-Aware_Background_CVPR_2023_paper.html)|14|Real|[Example](./Dataset_image/rdd.md)|[Link](https://github.com/hyyh1314/RDD)|
|[DIBCO 2013](https://openaccess.thecvf.com/content/CVPR2023/html/Zhang_Document_Image_Shadow_Removal_Guided_by_Color-Aware_Background_CVPR_2023_paper.html)|16|Real|[Example](./Dataset_image/rdd.md)|[Link](https://github.com/hyyh1314/RDD)|
|[H-DIBCO 2014](https://openaccess.thecvf.com/content/CVPR2023/html/Zhang_Document_Image_Shadow_Removal_Guided_by_Color-Aware_Background_CVPR_2023_paper.html)|10|Real|[Example](./Dataset_image/rdd.md)|[Link](https://github.com/hyyh1314/RDD)|
|[H-DIBCO 2016](https://openaccess.thecvf.com/content/CVPR2023/html/Zhang_Document_Image_Shadow_Removal_Guided_by_Color-Aware_Background_CVPR_2023_paper.html)|10|Real|[Example](./Dataset_image/rdd.md)|[Link](https://github.com/hyyh1314/RDD)|
|[DIBCO 2017](https://openaccess.thecvf.com/content/CVPR2023/html/Zhang_Document_Image_Shadow_Removal_Guided_by_Color-Aware_Background_CVPR_2023_paper.html)|20|Real|[Example](./Dataset_image/rdd.md)|[Link](https://github.com/hyyh1314/RDD)|
|[DIBCO 2018](https://openaccess.thecvf.com/content/CVPR2023/html/Zhang_Document_Image_Shadow_Removal_Guided_by_Color-Aware_Background_CVPR_2023_paper.html)|10|Real|[Example](./Dataset_image/rdd.md)|[Link](https://github.com/hyyh1314/RDD)|
|[DIBCO 2019](https://openaccess.thecvf.com/content/CVPR2023/html/Zhang_Document_Image_Shadow_Removal_Guided_by_Color-Aware_Background_CVPR_2023_paper.html)|10|Real|[Example](./Dataset_image/rdd.md)|[Link](https://github.com/hyyh1314/RDD)|
|[Bickly-diary](https://dl.acm.org/doi/abs/10.1145/1816123.1816161)|7|Real|[Example](./Dataset_image/rdd.md)|[Link](https://1drv.ms/f/s!Ak15mSdV3Wy4iY4sW5gm7ak4aWjtFQ?e=1l7vRi)|
|[Synchromedia Multispectral (MSI)](https://www.sciencedirect.com/science/article/pii/S0031320313000642)|240|Real|[Example](./Dataset_image/rdd.md)|[Link](ttps://tc11.cvc.uab.es/datasets/SMADI_1)|
|[Persian Heritage Image Binarization （PHIBD）](https://ieeexplore.ieee.org/abstract/document/6528442)|15|Real|[Example](./Dataset_image/rdd.md)|[Link](http://www.iapr-tc11.org/mediawiki/index.php/Persian_Heritage_Image_Binarization_Dataset_(PHIBD_2012))|
|[Palm Leaf]()|50|Real|[Example]()|[Link](http://amadi.univ-lr.fr/ICFHR2016_Contest/index.php/download-123)|
|[NoiseOffice]()|216|Synthetic|[Example]()|[Link](https://archive.ics.uci.edu/dataset/318/noisyoffice)|
|[LRDE Document Binarization Dataset]()|125|Real|[Example]()|[Link](https://www.lrde.epita.fr/wiki/Olena/DatasetDBD)|
|[Shipping label dataset](https://www.sciencedirect.com/science/article/pii/S0031320322002916)|1082|Real|[Example](./Dataset_image/shipping/shipping.md)|[Link](https://www.dropbox.com/sh/gqqugvclzltfldt/AACNELpHwTW-1bHLZzipxQWja?dl=0)|


### 5.3 SOTA

<table class="tg">
<thead>
  <tr>
    <th class="tg-c3ow" rowspan="2">Venue</th>
    <th class="tg-c3ow" rowspan="2">Methods</th>
    <th class="tg-c3ow" rowspan="2">Training data</th>
    <th class="tg-c3ow" colspan="4">DIBCO'18</th>
    <th class="tg-c3ow" colspan="4">DIBCO'19</th>
  </tr>
  <tr>
    <th class="tg-c3ow">FM</th>
    <th class="tg-c3ow">p-FM</th>
    <th class="tg-c3ow">PSNR</th>
    <th class="tg-c3ow">DRD</th>
    <th class="tg-c3ow">FM</th>
    <th class="tg-c3ow">p-FM</th>
    <th class="tg-c3ow">PSNR</th>
    <th class="tg-c3ow">DRD</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-c3ow">TPAMI'20</td>
    <td class="tg-c3ow">DE-GAN</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">61.41</td>
    <td class="tg-c3ow">62.67</td>
    <td class="tg-c3ow">14.81</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">54.72</td>
    <td class="tg-c3ow">54.59</td>
    <td class="tg-c3ow">11.25</td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-c3ow">DocDiff</td>
    <td class="tg-c3ow">ACM MM'23</td>
    <td class="tg-c3ow">(H-)DIBCO LOYO (9, 10, 11, 12, 13, 14, 16, 17, 18, 19), Bckly-diary, PHIB, SM, NoiseOffice</td>
    <td class="tg-c3ow">88.11</td>
    <td class="tg-c3ow">90.43</td>
    <td class="tg-c3ow">17.92</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">73.38</td>
    <td class="tg-c3ow">75.12</td>
    <td class="tg-c3ow">15.14</td>
    <td class="tg-c3ow">-</td>
  </tr>
  <tr>
    <td class="tg-c3ow">ColDBin</td>
    <td class="tg-c3ow">ICDAR'23</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">89.71</td>
    <td class="tg-c3ow">93.00</td>
    <td class="tg-c3ow">19.53</td>
    <td class="tg-c3ow">3.82</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">-</td>
  </tr>
  <tr>
    <td class="tg-c3ow">D<sup>2</sup>BFormer</td>
    <td class="tg-c3ow">IF'23</td>
    <td class="tg-c3ow">(H-)DIBCO LOYO (9, 10, 11, 12, 13, 14, 16, 17, 18, 19), Bckly-diary, PHIB, SM </td>
    <td class="tg-c3ow">88.84</td>
    <td class="tg-c3ow">93.42</td>
    <td class="tg-c3ow">18.91</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-c3ow">GBD</td>
    <td class="tg-c3ow">PR'24</td>
    <td class="tg-c3ow">(H-)DIBCO LOYO (9, 10, 11, 12, 13, 14, 16, 17, 18, 19), Bckly-diary, PHIB, SM </td>
    <td class="tg-c3ow">91.09</td>
    <td class="tg-c3ow">94.57</td>
    <td class="tg-c3ow">19.92</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">73.51</td>
    <td class="tg-c3ow">74.81</td>
    <td class="tg-c3ow">14.96</td>
    <td class="tg-c3ow"></td>
  </tr>
</tbody>
</table>

Leave-one-year out (LOYO) strategy means that we consider whole documents of one particular (H-)DIBCO year as a testing dataset, while treat all remaining documents from other years as training data.