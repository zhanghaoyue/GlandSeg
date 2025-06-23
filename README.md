
# Masked Image Modeling Meets Self-Distillation: A Transformer-Based Prostate Gland Segmentation Framework for Pathology Slides
[Haoyue Zhang](https://github.com/zhanghaoyue), Sushant Patkar, Rosina Lis, Maria J Merino, Peter A Pinto, Peter L Choyke, Baris Turkbey, Stephanie Harmon

[read paper here](https://www.mdpi.com/2072-6694/16/23/3897)

## Simple Summary
The accurate characterization of prostate cancer glands is vital for diagnosis and grading, and the segmentation of these glands is critical for quantitative analysis and machine-learning models. Human annotation is unrealistic given the size of whole-slide images, yet there lacks a reliable fully automated segmentation framework. This study addressed the limitations of previous state-of-the-art approaches reported on this task, popular segmentation frameworks, and foundational models. Our proposed framework leverages the strength of self-supervised and self-distillation to achieve a high segmentation performance, offering a reliable prostate gland segmentation to pave the way for better downstream analysis of whole-slide images.
## Abstract
Detailed evaluation of prostate cancer glands is an essential yet labor-intensive step in grading prostate cancer. Gland segmentation can serve as a valuable preliminary step for machine-learning-based downstream tasks, such as Gleason grading, patient classification, cancer biomarker building, and survival analysis. Despite its importance, there is currently a lack of a reliable gland segmentation model for prostate cancer. Without accurate gland segmentation, researchers rely on cell-level or human-annotated regions of interest for pathomic and deep feature extraction. This approach is sub-optimal, as the extracted features are not explicitly tailored to gland information. Although foundational segmentation models have gained a lot of interest, we demonstrated the limitations of this approach. This work proposes a prostate gland segmentation framework that utilizes a dual-path Swin Transformer UNet structure and leverages Masked Image Modeling for large-scale self-supervised pretaining. A tumor-guided self-distillation step further fused the binary tumor labels of each patch to the encoder to ensure the encoders are suitable for the gland segmentation step. We united heterogeneous data sources for self-supervised training, including biopsy and surgical specimens, to reflect the diversity of benign and cancerous pathology features. We evaluated the segmentation performance on two publicly available prostate cancer datasets. We achieved state-of-the-art segmentation performance with a test mDice of 0.947 on the PANDA dataset and a test mDice of 0.664 on the SICAPv2 dataset.


## Framework illustration:
![framework](https://github.com/user-attachments/assets/b9614d00-896c-4a35-ad6f-ce909f30a90e)


## Citation
If you find our work useful, please consider citing:
```
@article{zhang2024masked,
  title={Masked Image Modeling Meets Self-Distillation: A Transformer-Based Prostate Gland Segmentation Framework for Pathology Slides},
  author={Zhang, Haoyue and Patkar, Sushant and Lis, Rosina and Merino, Maria J and Pinto, Peter A and Choyke, Peter L and Turkbey, Baris and Harmon, Stephanie},
  journal={Cancers},
  volume={16},
  number={23},
  pages={3897},
  year={2024},
  publisher={MDPI}
}
```
## update
### GlandSeg
codebase for prostate gland segmentation model "Masked Image Modeling Meets Self-Distillation: A Transformer-based Prostate Gland Segmentation Framework for Pathology Slides"

### Model Code
now, the model code is uploaded

### Model weights
https://huggingface.co/zhanghaoyue/ProstateGlandSeg
Based on the feedback, Panda models generalize better on other datasets while SICAPv2 is more tuned towards itself.
