Staganography is data hiding technique, through which we can hide a piece of information in an object.Based on the nature of covering object Staganography is divided into Text Staganography,Image Steganography,Video Steganography,Audio Steganography etc.


In this repository I performed Image Staganography using an encoder architecture to embed a secret message into an image and a decoder architecture to extract the hidden message from the Stegastamp.
These encoder and decoder architectures are trained with MIRFLICKR dataset.




To encode a messege "Hello" in an image img.png run encode_image.py by passing necessary arguments as
    python encode_image.py \
    saved_models/encoder.pth \
  --image img.png  \
  --save_dir out/ \
  --secret Hello
  After the execution of the above script a Stegastamp and a residual applied to original image will be saved in "out" directory.
  
  
  
  
To decode the hidden message from Stegastamp run decode_image.py by passing necessary arguments as 
    python decode_image.py \
    saved_models/decoder.pth \
    --image out/Stegastamp.png
   
 After the execution of the above script,the hidden message "Hello" will be displayed on the terminal.
    
    