# Multi-Object Tracking in the Dark

The official repo of the CVPR 2024 paper [Multi-Object Tracking in the Dark](https://arxiv.org/abs/2405.06600)


![LMOT](imgs/data_preview.jpg)


## News
<!-- * [TODO] code release
* [TODO] codalab test
* [TODO] pull request TrackEval -->
* [TODO] Testing website is under development.
* [TODO] We are checking the privacy issues of our dataset



## Abstract

Low-light scenes are prevalent in real-world applications (e.g. autonomous driving and surveillance at night). Recently, multi-object tracking in various practical use cases have received much attention, but multi-object tracking in dark scenes is rarely considered. In this paper, we focus on multi-object tracking in dark scenes. To address the lack of datasets, we first build a **L**ow-light **M**ulti-**O**bject **T**racking (LMOT) dataset. LMOT provides well-aligned low-light video pairs captured by our dual-camera system, and high-quality multi-object tracking annotations for all videos. Then, we propose a low-light multi-object tracking method, termed as **LTrack**. We introduce the adaptive lowpass downsample module to enhance low-frequency components of images outside the sensor noises. The degradation suppression learning strategy enables the model to learn invariant information under noise disturbance and image quality degradation. These components improve the robustness of multi-object tracking in dark scenes. We conducted a comprehensive analysis of our LMOT dataset and proposed LTrack. Experimental results demonstrate the superiority of the proposed method and its competitiveness in real night low-light scenes



## Dataset


### Construction

LMOT dataset is collected using our dual-camera sysyem, which provide well-aligned low-light and well-lit video pairs (LMOT-dual). We also collect a real low-light MOT dataset to evaluate performance in real night dark scene, which are captured using a single camera with the same camera settings (LMOT-real).

We provide the dataset in both RAW (RGGB) and sRGB format, with 20FPS, 10ms exposure time, and $1800\times1000$ resolution. LMOT dataset contains a variety of city outdoor scenes, including roads, overpasses, pedestrians, and intersection. We annotate six types of moving objects, including car, person, bicycle, motorcycle, bus, and truck. All annotations are carefully reviewed.


### Statistics

Detailed statics and data splits for LMOT dataset
<table>
  <tr>
    <td>Dataset</td>
    <td>Split</td>
    <td>Videos</td>
    <td>Bbox</td>
    <td>Tracks</td>
    <td>Paired Well-lit</td>
  </tr>

  <tr>
    <td rowspan="3">LMOT-dual</td>
    <td>train</td>
    <td>11</td>
    <td>309,466</td>
    <td>1,533</td>
    <td>&#x2714</td>
  </tr>
  <tr>
    <td>val</td>
    <td>4</td>
    <td>131,781</td>
    <td>626</td>
    <td>&#x2714</td>
  </tr>
  <tr>
    <td>test</td>
    <td>11</td>
    <td>312,742</td>
    <td>1,644</td>
    <td>&#x2714</td>
  </tr>

   <tr>
    <td>LMOT-real</td>
    <td>real</td>
    <td>6</td>
    <td>61,561</td>
    <td>287</td>
    <td>&#x2716</td>
  </tr>
</table>



### How to use

LMOT dataset is organized in the form of [MOT Challenge 17](https://motchallenge.net)

```
└── LMOT_release/
    ├── train/
        ├── LMOT-02/
            ├── gt/
            ├── img_dark/
            ├── img_light/
            ├── img_dark_rgb/
            ├── img_light_rgb/
            └── seqinfo.ini
        ├── LMOT-04/
        └── ...
    ├── val/
        └── ...
    ├── test/
        └── ...
    └── real/
        ├── RLMOT-01/
            ├── gt/
            ├── img_real/
            ├── img_real_rgb/
            └── seqinfo.ini
        ├── RLMOT-02/
        └── ...

```

<!-- #### Download

1. RAW videos: [lmot_train_light_raw.zip](), [LMOT_dual_dark_raw.zip]()
2. RGB videos: [LMOT_dual_light_rgb.zip](), [LMOT_dual_dark_rgb.zip]() -->



<!-- #### Evaluation -->




<!-- ## Acknowledgement
 -->







## Citation
If you our dataset or code for research, please cite our paper:
```
@inproceedings{wang2024multi,
  title={Multi-Object Tracking in the Dark},
  author={Wang, Xinzhe and Ma, Kang and Liu, Qiankun and Zou, Yunhao and Fu, Ying},
  booktitle={Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition},
  year={2024}
}
```


