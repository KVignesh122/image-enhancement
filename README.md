# Notebook for inferencing Real-ESRGAN and GFPGAN v1.4 to enhance images
The State-of-the-Art (SOTA) models being used for this project:

**1. Real-ESRGAN (Real Enhanced Super-Resolution Generative Adversarial Network)**
  * As seen from the name, it is an enhanced version of the ordinary SRGAN model.
  * Can be used for both 2D and 360-degree images.
  * Adversarially-trained, so improves perceptual quality, and can generate more realistic/detailed textures.
  * Actual image enhancement is done with ESRGAN, and output image upscaling is done with LANCZOS4 resampling.
  * Preferable to run with GPU.

**2. GFPGAN (Generative Facial Pre-trained Generative Adversarial Network) version 1.4**
  * Used for face enhancement and restoration in 2d images.
  * Built on-top of StyleGAN2 model. More realistic facial expression reconstructions compared to previous models.
  * Can be appended into the Real-ESRGAN for general image restoration and run together.
  * Preferable to run with GPU.

<Demo of OIP>

**One can choose between 2 options to enhance their image: a 2-layered NN version (RealESRGAN_x2plus.pth) or a 4-layered NN version (RealESRGAN_x4plus.pth).** This means that the 4-layered model passes the original image through 4 layers of neural networks compared to the 2-layered model which only passes the original image through 2 layers of neural networks. A general rule will be that the more NN layers our image passes through means the enhancement is much more perfect. But at the same time, this means that running the x4layer model takes more time than the x2layer model.

**_*Note: If your image contains repeated textures or patters, using the 2-layers over the 4-layers may sometimes produce more satisfactory results._**

View the Google Colab notebook for inferencing and enhancing your images [here](https://colab.research.google.com/drive/1jchSitQtj7c3g9wJDdqOVaXK-WVNPJjm?usp=sharing)! Make a copy of it and get started! 😜
