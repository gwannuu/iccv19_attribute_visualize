# What I did

I visualize the result of "spatial transformer network" module of "Improving Pedestrian Attribute Recognition With Weakly-Supervised Multi-Scale Attribute-Specific Localization". I follows visualization method of original paper. 

see model/inception.py -> class inceptionnet -> def visualization

# How to visualize?

- First download rap directory (root 디렉토리에 rap dataset 위치시킴)
- make named "visualization" empty directory in project directory. (root 디렉토리에 visualization이란 이름의 디렉토리 생성)
- After finishing training, you can make visualized input pictures by giving "--visualization=true" option. (training 이후에 model이 'saved_model.pt'라는 이름으로 root 디렉토리에 자동 저장됨. visualization 시에는 저장된 모델을 불러와서 시각화된 이미지파일들을 visualization 디렉토리에 저장함)

Visualization=True option may fill your empty named "visualization" directory

```
python main.py --approach=inception_iccv --experiment=rap --visualization=True
```

Below is the description of original code of ICCV19, Improving pedestrian Attribute Recognition with Weakly-Supervised Multi-Scale Attribute-Specific-Localization"
Yu can find original code in here (https://github.com/chufengt/iccv19_attribute)

--------------------

## Improving Pedestrian Attribute Recognition With Weakly-Supervised Multi-Scale Attribute-Specific Localization

Code for the paper "Improving Pedestrian Attribute Recognition With Weakly-Supervised Multi-Scale Attribute-Specific Localization", ICCV 2019, Seoul.

[[Paper]](https://arxiv.org/abs/1910.04562) [[Poster]](https://chufengt.github.io/publication/pedestrian-attribute/iccv_poster_id2029.pdf)

Contact: chufeng.t@foxmail.com or tcf18@mails.tsinghua.edu.cn

### Environment

- Python 3.6+
- PyTorch 0.4+

### Datasets

- RAP: http://rap.idealtest.org/
- PETA: http://mmlab.ie.cuhk.edu.hk/projects/PETA.html
- PA-100K: https://github.com/xh-liu/HydraPlus-Net

The original datasets should be processed to match the DataLoader.

We provide the label lists for training and testing.

### Training and Testing

```
python main.py --approach=inception_iccv --experiment=rap
```

```
python main.py --approach=inception_iccv --experiment=rap -e --resume='model_path'
```

### Pretrained Models

We provide the pretrained models for reference, the results may slightly different with the values reported in our paper.

| Dataset | mA    | Link                                                         |
| ------- | ----- | ------------------------------------------------------------ |
| PETA    | 86.34 | [Model](https://drive.google.com/file/d/1cvX43Qn_vydzT_jnmgwYUUe9hIA161PH/view?usp=sharing) |
| RAP     | 81.86 | [Model](https://drive.google.com/file/d/15paMK0-rKDsuzptDPK5kH2JuL8QO0HyS/view?usp=sharing) |
| PA-100K | 80.45 | [Model](https://drive.google.com/file/d/1xIw3jpvE1pDC3U464kcFJ58iSKCRNQ63/view?usp=sharing) |

### Reference

If this work is useful to your research, please cite:

```
@inproceedings{tang2019improving,
  title={Improving Pedestrian Attribute Recognition With Weakly-Supervised Multi-Scale Attribute-Specific Localization},
  author={Tang, Chufeng and Sheng, Lu and Zhang, Zhaoxiang and Hu, Xiaolin},
  booktitle={Proceedings of the IEEE International Conference on Computer Vision},
  pages={4997--5006},
  year={2019}
}
```
