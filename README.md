# Skin Cancer Detection

*Disclaimer: this notebook was developed out of personal curiosity and therefore it is not completely implemented. There may also be some minor errors that have gone unnoticed*.

Thanks to the pattern recognition capabilities of Convolutional Neural Networks, skin cancer can nowadays be early detected by visually analyzing the characteristic of a skin mole. In this notebook we propose a skin cancer detection algorithm based on some of the most typical CNN arquitectures (Resnet, Inception, MobileNet, DenseNet and a from scrath network) that performs binary image classification ('0': non-cancer, '1': cancer). 

We used ISIC DB 2018 dataset to evaluate the experiments, a highly imbalanced dataset containing 2750 dermoscopic images, publicly available here: https://challenge.isic-archive.com/data

A patch-based preprocessing stage is implemented in order to reduce the size of the input images to (300x300), due to the memory limitations of Google Colab. A comparison of different arquitectures is carried out. 
