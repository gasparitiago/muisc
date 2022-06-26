# Unified Image-sequence Classifier (MUIsC)
Paper: **Automatic Generation of Product-Image Sequence in E-commerce**
<br>
In KDD 2022 ADS 
<br>

This repo includes the inference code for MUIsC, the main module of our AGPIS (Automatic Generation of Product-Image Sequence) framework for JD.com.

## Environment setup
- ```conda create -n agpis python=3.6 ```
- ```pip3 install torch torchvision torchaudio```
- Go to ./transformers/ and run ```pip install -e .```

## Description
- The main code is at ```./muisc_inference.py```. You can find input data processing code in function ```build_data```; model loading code in function ```load_model``` (instantiation of language tower and image tower and their interaction are also here); and inferece code is in function ```inference```.  
- ```muisc_model.py``` contains data iterator and image-tower modeling. 
- The model checkpoint is not available for some reason, sorry.

## Update
- Performance could be futher impoved if
  - Simultaneously predicting product title in the training stage
  - Adding pruduct categpry to its title
  - Training lm_head (a linear layer) from scratch
