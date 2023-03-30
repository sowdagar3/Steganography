Steganography is data hiding technique, through which we can hide a piece of information in an object.Based on the nature of covering object Steganography is divided into Text Steganography,Image Steganography,Video Steganography,Audio Steganography etc.


This repository contains required code and pretrained models to perform Image Steganography using an encoder architecture to embed a secret message into an image and a decoder architecture to extract the hidden message from the Stegastamp.These encoder and decoder architectures are trained with MIRFLICKR dataset.

To download the pretrained encoder and decoder use the link [Pretrained_models](https://drive.google.com/drive/folders/102Gws6tW6zlAMpr7cYTG_0JE1mDaJWF9?usp=sharing).After downloading the pretrained models keep them in "saved_models" folder.To install the required libraries run the command
```
pip install -r requirement.txt
```


To encode a messege "Hello" in an image img.png run encode_image.py by passing necessary arguments as

```
    python3 Encode_image.py \
    saved_models/Encoder.pth \
    --image img.png  \
    --save_dir out/ \
    --secret Hello
  
```
  
After the execution of the above script a Stegastamp and a residual applied to original image will be saved in "out" directory.
  
  
  
  
To decode the hidden message from Stegastamp run decode_image.py by passing necessary arguments as 
```
    python3 Decode_image.py \
    saved_models/Decoder.pth \
    --image out/Stegastamp.png

```   
 After the execution of the above script,the hidden message "Hello" will be displayed on the terminal.
 
 
Refference:

1.[StegaStamp: Invisible Hyperlinks in Physical Photographs](https://arxiv.org/abs/1904.05343)

2.[https://github.com/JisongXie/StegaStamp_pytorch](https://github.com/JisongXie/StegaStamp_pytorch)
    
