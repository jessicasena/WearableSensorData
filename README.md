# WearableSensorData
This repository provides the codes and data used in our paper "Human Activity Recognition Based on Wearable Sensor Data: A Standardization of the State-of-the-Art", where we implement and evaluate several state-of-the-art approaches, ranging from handcrafted-based methods to convolutional neural networks. Also, we standardize a large number of datasets, which vary in terms of sampling rate, number of sensors, activities, and subjects.

## Requirements

- [Scikit-learn](http://scikit-learn.org/stable/)
- [Keras](https://github.com/fchollet/keras) (Recommended version 2.1.2)
- [Tensorflow](https://www.tensorflow.org/) (Recommended version 1.3.0)
- [Python 3](https://www.python.org/)

## Quick Start
1. Clone this repository
2. Run
    ```bash
    python <Catal2015|...|ChenXue2015>.py data/<SNOW|FNOW|LOTO|LOSO>/<MHEALTH|USCHAD|UTD-MHAD1_1s|UTD-MHAD2_1s|WHARF|WISDM>.npz
    ```
	For example
	```bash
    python Catal2015.py data/LOSO/MHEALTH.npz
    ```
	
## Data Format
The raw signal provided by the original dataset was segmented by using a temporal sliding window of 5 seconds. 
Its format is (number of samples, 1, temporal window size, number of sensors)
	
## Contributing
Contributions to this repository are welcome. Examples of things you can contribute:
 * Implementation of other methods. See template_hancrafted.py and template_convNets.py
 * Accuracy Improvements.
 * Reporting bugs.

The table below shows the mean accuracy achieved by the methods using the Leave-One-Subject-Out (LOSO) as validation protocol. The symbol 'x' denotes which was not possible to execute the method on the respective dataset.

| **METHOD** | **MHEALTH** | **PAMAP2** | **USCHAD** | **UTD-MHAD1** | **UTD-MHAD2** | **WHARF** | **WISDM** | **COOK** | **Mean Accuracy** |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| [Ha and Choi](https://ieeexplore.ieee.org/document/7727224/) | 0.9085 [0.8954, 0.9216] | 0.7007 [0.6464, 0.7550] | 0.6997 [0.6823, 0.7171] | 0.1446 [0.1380, 0.1512] | 0.6681 [0.6452, 0.6910] | 0.4502 [0.4191, 0.4813] | 0.7561 [0.7403, 0.7719] | 0.3625 [0.3294, 0.3957] |  |
| [Catal et al.](https://www.sciencedirect.com/science/article/pii/S1568494615000447) | 0.9466 [0.9373, 0.9560] | 0.8537 [0.8279, 0.8796] | 0.7471 [0.7336, 0.7607] | 0.3203 [0.3141, 0.3265] | 0.7444 [0.7242, 0.7646] | 0.4846 [0.4663, 0.5028] | 0.7436 [0.7277, 0.7596] | 0.3297 [0.3047, 0.3548] |  |
| [Kim et al.](https://ieeexplore.ieee.org/document/6411901/) | 0.9336 [0.9231, 0.9441] |  | 0.6401 [0.6241, 0.6562] | 0.3780 [0.3729, 0.3831] | 0.6505 [0.6375, 0.6634] | 0.5205 [0.5022, 0.5387] | 0.4977 [0.4837, 0.5117] |  |  |
| [Chen and Xue](https://ieeexplore.ieee.org/document/7379395/) | 0.9131 [0.9047, 0.9216] | 0.7143 [0.6604, 0.7681] | 0.7810 [0.7677, 0.7942] | x | x | 0.6577 [0.6342, 0.6812] | 0.8384[0.8240, 0.8529] | 0.3633 [0.3334, 0.3933] |  |
| [Jiang and Yin](https://dl.acm.org/citation.cfm?id=2806333) |  | x | 0.7658 [0.7520, 0.7797] | x | x | 0.6591 [0.6393, 0.6789] | 0.8144 [0.7983, 0.8305] | 0.3348 [0.3088, 0.3607] |  |
| [Ha et al.](https://ieeexplore.ieee.org/document/7379657/) | 0.8684 [0.8546, 0.8822] |  | x | x | x | x | x | x |  |
| [Ha and Choi](https://ieeexplore.ieee.org/document/7727224/) |  |  | x | x | x | x | x | x |  |
| DeepSense |  | 0.4764 [0.4502, 0.5025] | 0.5654 [0.5489, 0.5820] |  |  |  |  | x |  |
| Jordao et al. | 0.5778 [0.5542, 0.6013] |  | 0.7427 [0.7256, 0.7597] | 0.4335 [0.4268, 0.4402] | 0.6987 [0.6833, 0.7141] | 0.6156 [0.5909, 0.6404] | 0.8430 [0.8296, 0.8565] | 0.3911 [0.3671, 0.4150] |  |
| KimChoi | 0.2687 [0.2673, 0.2702] |  | 0.4506 [0.4439, 0.4574] | 0.1713 [0.1662, 0.1764] | 0.3018 [0.2985, 0.3050] | 0.4452 [0.4187, 0.4716] | 0.4829 [0.4680, 0.4977] |  |  |
| Panwar et al. | 0.6136 [0.5941, 0.6332] | 0.1278 [0.1123, 0.1433] | 0.6043 [0.5863, 0.6222] | 0.1312 [0.1198, 0.1425] | 0.5882 [0.5707, 0.6057] | 0.1802 [0.1467, 0.2137] | 0.8095 [0.7954, 0.8236] | 0.3543 [0.3345, 0.3741] |  |
| DCNN - ensemble |  |  |  | 0.4535 [0.4474, 0.4597] | 0.7740 [0.7596, 0.7884] | 0.6910 [0.6738, 0.7082] | 0.8510 [0.8356, 0.8664] | x |  |
| MDE |  |  |  | 0.5261 [0.5190, 0.5331] | 0.7707 [0.7577, 0.7837] | 0.6325 [0.6105, 0.6544] | 0.8199 [0.8033, 0.8365] | x |  |
| multi_stream | 0.8372 [0.8229, 0.8515] | 0.7170 [0.6857, 0.7483] | 0.7660 [0.7521, 0.7799] | 0.3673 [0.3595, 0.3750] | 0.6956 [0.6803, 0.7110] | 0.6062 [0.5821, 0.6303] | 0.8583 [0.8480, 0.8686] | x |  |
| Mean Accuracy |  |  |  |  |  |  |  |  | x |

Please cite our paper in your publications if it helps your research.
```bash
@article{Jordao:2018,
author    = {Artur Jordao,
Antonio Carlos Nazare,
Jessica Sena and
William Robson Schwartz},
title     = {Human Activity Recognition Based on Wearable Sensor Data: A Standardization of the State-of-the-Art},
journal   = {arXiv},
year      = {2018},
eprint    = {1806.05226},
}
```
