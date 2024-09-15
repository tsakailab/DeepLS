## DeepLS

*DeepLS* is a novel unsupervised deep learning approach designed for online separation of sparse signal components. This method leverages the low-rank and sparse priors inherent in datasets for training purposes. It utilizes a U-Net-based model, structured similarly to an hourglass, which efficiently encodes and decodes sparse components. During training, the model employs a loss function based on a combination of nuclear and $\ell_1$ norms, mirroring the objective function of Robust Principal Component Analysis (RPCA). This approach encourages the model to discern and isolate the sparse components within the input data. 

Notably, once trained, the DeepLS model gains the capacity to extract learned sparse components from a diverse range of inputs, not limited to those exhibiting low-rank characteristics. This capability eliminates the need for retraining the model for varying backgrounds, leading to computationally efficient online separation of target signals that share features with the learned sparse components from the training dataset.


![](model_architecture.png)

## available codes
[demo programs](./demo)
- [Application to background subtraction](./demo/demo_background_subtraction.ipynb)
  - Airport dataset [Li+04]
  - including comparison to RPCA [Candes+09]
- [Application to cell segmentation](./demo/demo_cell_segmentation.ipynb)
  - [ISBI 2014 dataset](https://cs.adelaide.edu.au/~carneiro/isbi14_challenge/)
  - including introduction of [anisotropic total variation](https://en.wikipedia.org/wiki/Total_variation_denoising) for loss function

## Paper
"Unsupervised deep learning for online foreground segmentation exploiting low-rank and sparse priors"
2022 International Conference on Digital Image Computing: Techniques and Applications (DICTA)
https://ieeexplore.ieee.org/document/10034581

Incoming!:
Background subtraction approach to unsupervised cell segmentation toward excluding spurious featues in degraded cytology slides
2023 IEEE 20th International Symposium on Biomedical Imaging (ISBI)

## Citation
Low-rank and sparse loss:
```bib
@INPROCEEDINGS{takeda22,
  author={Takeda, Keita and Fujiwara, Kohei and Sakai, Tomoya},
  booktitle={2022 International Conference on Digital Image Computing: Techniques and Applications (DICTA)}, 
  title={Unsupervised deep learning for online foreground segmentation exploiting low-rank and sparse priors}, 
  year={2022},
  pages={1-7},
  doi={10.1109/DICTA56598.2022.10034581}}
```


