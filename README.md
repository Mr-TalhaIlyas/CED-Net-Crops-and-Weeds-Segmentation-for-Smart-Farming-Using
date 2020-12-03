# CED-Net-Crops-and-Weeds-Segmentation

The existing architectures for weeds and crops segmentation are quite deep, with millions of parameters that require longer training time. To overcome such limitations, we propose an idea of training small networks in cascade to obtain coarse-to-fine predictions, which are then combined to produce the final results.  Evaluation of the proposed network and comparison with other state-of-the-art networks are conducted using four publicly-available datasets: Rice seeding and weed dataset, BoniRob dataset, Carrot crop vs. weed dataset and paddy–millet dataset. The experimental results and their comparisons proclaim that the proposed network outperforms state-of-the-art architectures, such as U-Net, SegNet, FCN-8s, and DeepLabv3 over IoU, F1-score, sensitivity, true detection rate, and average precision comparison metrics, by utilizing only (1/5.74 × U-Net), (1/5.77 × SegNet), (1/3.04 × FCN-8s), and (1/3.24 × DeepLabv3)  fractions of total parameters. 

## Abstract

Convolutional neural networks (CNNs) have achieved state-of-the-art performance in numerous aspects of human life and the agricultural sector is no exception. One of the main objectives of deep learning for smart farming is to identify the precise location of weeds and crops on farmland. In this paper, we propose a semantic segmentation method based on a cascaded encoder-decoder network, namely CED-Net, to differentiate weeds from crops. The existing architectures for weeds and crops segmentation are quite deep, with millions of parameters that require longer training time. To overcome such limitations, we propose an idea of training small networks in cascade to obtain coarse-to-fine predictions, which are then combined to produce the final results. Evaluation of the proposed network and comparison with other state-of-the-art networks are conducted using four publicly available datasets: rice seeding and weed dataset, BoniRob dataset, carrot crop vs. weed dataset, and a paddy–millet dataset. The experimental results and their comparisons proclaim that the proposed network outperforms state-of-the-art architectures, such as U-Net, SegNet, FCN-8s, and DeepLabv3, over intersection over union (IoU), F1-score, sensitivity, true detection rate, and average precision comparison metrics by utilizing only (1/5.74 × U-Net), (1/5.77 × SegNet), (1/3.04 × FCN-8s), and (1/3.24 × DeepLabv3) fractions of total parameters.


You can access the [**_full paper here_**](https://www.mdpi.com/2079-9292/9/10/1602)

## Network Architecture

The proposed network architecture is shown in Figure below. The overall model training is performed
coarse weed prediction and Model-3 for crop prediction. The predictions of Model-1 and Model-3
are up-sampled, concatenated with corresponding input image size, and used as inputs by Model-2
and Model-4, respectively. Two cascaded networks (Model-1, Model-2) are thus trained for weed
predictions, and the other two (Model-3, Model-4) for crop predictions. In total, then, we have four
such small networks. The section that follows explains the network architecture and training details.

![Picture2](https://user-images.githubusercontent.com/56618776/98434177-c6985f00-2110-11eb-8104-25e618f122c3.png)
## Visual Results and Comparisons
### Rice Seeding and Weed Segmentation Dataset

![Figure_4](https://user-images.githubusercontent.com/56618776/98434314-e54b2580-2111-11eb-98bd-268b92bba7c6.png)

### BoniRob Dataset

![Figure_5](https://user-images.githubusercontent.com/56618776/98434315-e7ad7f80-2111-11eb-946d-d73e8c72b588.png)

### Carrot Crop and Weed

![Figure_6](https://user-images.githubusercontent.com/56618776/98434317-e9774300-2111-11eb-9640-6e1fd8d85e02.png)

### Paddy-Millet Datase

![Figure_7](https://user-images.githubusercontent.com/56618776/98434321-ebd99d00-2111-11eb-827b-9f06aa6f62b9.png)


# Citation Request

If you use CED-Net in your project, please cite the following paper
```
@article{khan2020ced,
  title={CED-Net: Crops and Weeds Segmentation for Smart Farming Using a Small Cascaded Encoder-Decoder Architecture},
  author={Khan, Abbas and Ilyas, Talha and Umraiz, Muhammad and Mannan, Zubaer Ibna and Kim, Hyongsuk},
  journal={Electronics},
  volume={9},
  number={10},
  pages={1602},
  year={2020},
  publisher={Multidisciplinary Digital Publishing Institute}
}
```
OR via [google scholar](https://scholar.google.com/citations?hl=en&user=HYNOyyAAAAAJ)
