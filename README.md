# DeepLS
This repository proposes unsupervised deep learning exploiting low-rank and sparse priors of dataset.
Robust principal component analysis (RPCA) can achieve background subtraction by minimizing nuclear and $\ell_1$ norms to exploit the prior knowledge about spatio-temporal sparseness and low-rankness of the foreground objects and background scene.
With a combination of these norms as a loss function, the proposed method trains a U-Net-based model so as to encode and decode the sparse foreground objects for a batch of input images with a low-rank background.
Once the model has learned enough features common to the foreground objects, it has the potential to detect them from any single image regardless of the low-rankness and sparseness.
The proposed model performs online object segmentation with much less computational expense than that of RPCA.
Our method can build up a well-generalized model from only a few dozen of unannotated training images.

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


