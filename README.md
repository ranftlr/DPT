## Vision Transformers for Dense Prediction

This repository contains code and models for:

> Vision Transformers for Dense Prediction  

### Setup 

1) Download the model weights and place them in the `weights` folder:

Monodepth:
- [dpt_hybrid-midas-501f0c75.pt](https://drive.google.com/file/d/1chxMbP7X-VQL3MfkTqkoggApMaI_d8Ow/view?usp=sharing)
- [dpt_large-midas-2f21e586.pt](https://drive.google.com/file/d/1Jqe8eSWrCWUa58yMHUPSDvNCQ7nchCio/view?usp=sharing)

Segmentation:
 - [dpt_hybrid-ade20k-53898607.pt](https://drive.google.com/file/d/1h1V0c1zcDOJFB-xIiJXJ4aprQKIj0b9y/view?usp=sharing)
 - [dpt_large-ade20k-b12dca68.pt](https://drive.google.com/file/d/15EemBa0iKHkQsBpQLt0G0YQbK1q9qO-7/view?usp=sharing)
 
2) Set up dependencies: 

    ```shell
    conda install pytorch torchvision opencv 
    pip install timm
    ```

   The code was tested with Python 3.7, PyTorch 1.8.0, OpenCV 4.5.1, and timm 0.4.5

    
### Usage 

1) Place one or more input images in the folder `input`.

2) Run a monocular depth estimation model:

    ```shell
    python run_monodepth.py
    ```

    Or run a semantic segmentation model:

    ```shell
    python run_segmentation.py
    ```

3) The results are written to the folder `output_monodepth` and `output_segmentation`, respectively.

Use the flag `-t` to switch between different models. Possible options are `dpt_hybrid` (default) and `dpt_large`.
