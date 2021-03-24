## Vision Transformers for Dense Prediction

This repository contains code and models for:

> Vision Transformers for Dense Prediction  

### Setup 

1) Download the model weights and place them in the `weights` folder:

Monodepth:
- [dpt_hybrid-midas-501f0c75.pt](https://drive.google.com/file/d/1dgcJEYYw1F8qirXhZxgNK8dWWz_8gZBD/view?usp=sharing)
- [dpt_large-midas-2f21e586.pt](https://drive.google.com/file/d/1vnuhoMc6caF-buQQ4hK0CeiMk9SjwB-G/view?usp=sharing)

Segmentation:
 - [dpt_hybrid-ade20k-53898607.pt](https://drive.google.com/file/d/1zKIAMbltJ3kpGLMh6wjsq65_k5XQ7_9m/view?usp=sharing)
 - [dpt_large-ade20k-b12dca68.pt](https://drive.google.com/file/d/1foDpUM7CdS8Zl6GPdkrJaAOjskb7hHe-/view?usp=sharing)
 
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

### License 

MIT License 
