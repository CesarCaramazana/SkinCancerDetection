# Skin Cancer Detection

*Disclaimer: this notebook was developed out of personal curiosity and therefore it is not completely implemented. There may also be some minor errors that have gone unnoticed. For a more interesting and developed project on the matter, visit my Dermoscopic Segmentation repository*.

Thanks to the pattern recognition capabilities of Convolutional Neural Networks, skin cancer can nowadays be early detected by visually analyzing the characteristic of a skin mole. In this notebook we propose a skin cancer detection algorithm based on some of the most typical CNN arquitectures (Resnet, Inception, MobileNet, DenseNet and a from scrath network) that performs binary image classification ('0': non-cancer, '1': cancer). We used ISIC DB 2018 dataset to evaluate the experiments, a highly imbalanced dataset containing 2750 dermoscopic images, publicly available here: https://challenge.isic-archive.com/data

<img src="https://github.com/CesarCaramazana/SkinCancerDetection/blob/main/images/cancer_nocancer.PNG">

Image source: extracted from the dataset


<h2>Description</h2>

A patch-based preprocessing stage is implemented in order to reduce the size of the input images to (300x300), motivated by the memory limitations of Google Colab. 


A comparison of different classifier arquitectures is carried out, trying to discover the strenghts and weaknesses of each of them, and trying to find the balance between performance and computational cost. 


<h2>Dataset scheme</h2>

The dataset was stored in a Google Drive account (<code>/content/drive/My Drive/db_isic</code>), with the following folder structure:

<pre>
<code>
  db_isic/
      idx/
          isic_2017.mat
      
      ISIC-2017_Training_Data/
          ISIC_0000421.jpg
          ...          
      ISIC-2017_Training_Part2_GroundTruth/
          gtann/
              ISIC_0000421.mat
              ...
      ISIC-2017_Validation_Data/
          ISIC_0006651.jpg
          ...        
      ISIC-2017_Validation_Part2_GroundTruth/
          gtann/
            ISIC_0006651.mat
            ...
      ISIC-2017_Test_v2_Data/
          ISIC_0016072.jpg
          ...
      ISIC-2017_Test_v2_Part2_GroundTruth/
          gtann/
              ISIC_0016072.mat
    
</code>
</pre>

<h2>Code usage</h2>

The project is implemented in a Google Colab notebook <code>cancer_detection.ipynb</code>, writen in Pytorch and using the following libraries:

<ul>
  
  <li> Numpy </li>
  <li> Matplotlib </li>
  <li> Torchvision </li>
  
  </ul>
