# Notebook for inferencing Real-ESRGAN and GFPGAN v1.4 to enhance images
[![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-34A853?style=flat-square&logo=googlecolab&logoColor=white)](https://colab.research.google.com/drive/1jchSitQtj7c3g9wJDdqOVaXK-WVNPJjm?usp=sharing)
[![Model Zoo](https://img.shields.io/badge/Model%20Zoo-Real%20ESRGAN-blue?style=flat-square&logo=github&logoColor=white)](https://github.com/xinntao/Real-ESRGAN/blob/master/docs/model_zoo.md)
[![Face Enhancement](https://img.shields.io/badge/Face%20Enhancement-GFPGAN-red?style=flat-square&logo=github&logoColor=white)](https://github.com/TencentARC/GFPGAN)

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

## Example

<table align="center">
 <tr>
  <td><b>Original</b></td>
  <td><b>Real-ESRGANx2</b></td>
  <td><b>Real-ESRGANx4</b></td>
  <td><b>Real-ESRGANx4 +<br>GFPGAN Face Enhancement</b></td>
 </tr>
 <tr>
  <td><img src="https://github.com/KVignesh122/image-enhancement/assets/55841532/906326e1-1526-444b-ab8f-0a38cded1c09" width=230 height=160)></td>
  <td><img src="https://github.com/KVignesh122/image-enhancement/assets/55841532/ff2a9d6a-b0bd-4ab3-a696-54ab5d672883" width=230 height=160)></td>
  <td><img src="https://github.com/KVignesh122/image-enhancement/assets/55841532/265eca15-d209-41ae-a270-c225fa9ab0f6" width=230 height=160)></td>
  <td><img src="https://github.com/KVignesh122/image-enhancement/assets/55841532/83d297fd-35f2-4bea-9756-bb77dd5caed8" width=230 height=160)></td>
 </tr>
</table>

**One can choose between 2 options to enhance their image: a 2-layered NN version (RealESRGAN_x2plus.pth) or a 4-layered NN version (RealESRGAN_x4plus.pth).** This means that the 4-layered model passes the original image through 4 layers of neural networks compared to the 2-layered model which only passes the original image through 2 layers of neural networks. A general rule will be that the more NN layers our image passes through means the enhancement is much more perfect. But at the same time, this means that running the x4layer model takes more time than the x2layer model.

**_*Note: If your image contains repeated textures or patters, using the 2-layers over the 4-layers may sometimes produce more satisfactory results._**

View the Google Colab notebook for inferencing and enhancing your images [here](https://colab.research.google.com/drive/1jchSitQtj7c3g9wJDdqOVaXK-WVNPJjm?usp=sharing)! Make a copy of it and get started! 😜
