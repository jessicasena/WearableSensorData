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
| [Ha and Choi](https://ieeexplore.ieee.org/document/7727224/) | <nobr>0.9085 [0.8954, 0.9216]<nobr/> | <nobr>0.7007 [0.6464, 0.7550]<nobr/> | <nobr>0.6997 [0.6823, 0.7171]<nobr/> | <nobr>0.1446 [0.1380, 0.1512]<nobr/> | <nobr>0.6681 [0.6452, 0.6910]<nobr/> | <nobr>0.4502 [0.4191, 0.4813]<nobr/> | <nobr>0.7561 [0.7403, 0.7719]<nobr/> | <nobr>0.3625 [0.3294, 0.3957]<nobr/> |  |
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


| **METHOD** 	| **MHEALTH** 	| **PAMAP2** 	| **USCHAD** 	| **UTD-MHAD1** 	| **UTD-MHAD2** 	| **WHARF** 	| **WISDM** 	| **COOK** 	| **Mean Recall** 	|
|:-:	|:-:	|:-:	|:-:	|:-:	|:-:	|:-:	|:-:	|:-:	|:-:	|
| [Ha and Choi](https://ieeexplore.ieee.org/document/7727224/) 	| <nobr>0.9090 [0.8965, 0.9214]<nobr/> 	| <nobr>0.6546 [0.6050, 0.7043]<nobr/> 	| <nobr>0.6488 [0.6318, 0.6658]<nobr/> 	| <nobr>0.1343 [0.1272, 0.1414]<nobr/> 	| <nobr>0.6637 [0.6393, 0.6880]<nobr/> 	| <nobr>0.2452 [0.2238, 0.2666]<nobr/> 	| <nobr>0.6172 [0.6002, 0.6341]<nobr/> 	| <nobr>0.3503 [0.3190, 0.3817]<nobr/> 	|  	|
| [Catal et al.](https://www.sciencedirect.com/science/article/pii/S1568494615000447) 	| 0.9492 [0.9403, 0.9581] 	| 0.8138 [0.7886, 0.8389] 	| 0.7058 [0.6932, 0.7183] 	| 0.3161 [0.3099, 0.3224] 	| 0.7398 [0.7185, 0.7611] 	| 0.2856 [0.2620, 0.3092] 	| 0.6118 [0.5946, 0.6291] 	| 0.3142 [0.2902, 0.3383] 	|  	|
| [Kim et al.](https://ieeexplore.ieee.org/document/6411901/) 	| 0.9347 [0.9248, 0.9446] 	|  	| 0.5679 [0.5548, 0.5809] 	| 0.3693 [0.3648, 0.3739] 	| 0.6578 [0.6450, 0.6707] 	| 0.2563 [0.2391, 0.2735] 	| 0.3418 [0.3296, 0.3540] 	|  	|  	|
| [Chen and Xue](https://ieeexplore.ieee.org/document/7379395/) 	| 0.9028 [0.8934, 0.9121] 	| 0.6566 [0.6025, 0.7107] 	| 0.7056 [0.6928, 0.7184] 	| x 	| x 	| 0.4283 [0.4006, 0.4561] 	| 0.7237 [0.7053, 0.7421] 	| 0.3633 [0.3334, 0.3933] 	|  	|
| [Jiang and Yin](https://dl.acm.org/citation.cfm?id=2806333) 	|  	| x 	|  	| x 	| x 	| 0.4078 [0.3840, 0.4316] 	| 0.7138 [0.6954, 0.7321] 	| 0.3226 [0.2991, 0.3461] 	|  	|
| [Ha et al.](https://ieeexplore.ieee.org/document/7379657/) 	| 0.8641 [0.8511, 0.8771] 	|  	| x 	| x 	| x 	| x 	| x 	| x 	|  	|
| [Ha and Choi](https://ieeexplore.ieee.org/document/7727224/) 	|  	|  	| x 	| x 	| x 	| x 	| x 	| x 	|  	|
| DeepSense 	|  	| 0.4109 [0.3846, 0.4372] 	| 0.5343 [0.5180, 0.5506] 	|  	|  	|  	|  	| x 	|  	|
| Jordao et al. 	| 0.5732 [0.5497, 0.5966] 	|  	| 0.7169 [0.6998, 0.7340] 	| 0.4342 [0.4282, 0.4402] 	| 0.7008 [0.6853, 0.7164] 	| 0.4179 [0.3884, 0.4474] 	| 0.7331 [0.7143, 0.7520] 	| 0.3667 [0.3429, 0.3906] 	|  	|
| KimChoi 	| 0.2500 [nan, nan] 	|  	| 0.3114 [0.3063, 0.3165] 	| 0.1685 [0.1633, 0.1737] 	| 0.2838 [0.2790, 0.2887] 	| 0.2395 [0.2236, 0.2554] 	| 0.3327 [0.3213, 0.3441] 	|  	|  	|
| Panwar et al. 	| 0.5801 [0.5616, 0.5986] 	| 0.1092 [0.0959, 0.1225] 	| 0.5461 [0.5293, 0.5628] 	| 0.1285 [0.1171, 0.1399] 	| 0.5907 [0.5731, 0.6083] 	| 0.1223 [0.0983, 0.1462] 	| 0.6932 [0.6762, 0.7102] 	| 0.3417 [0.3221, 0.3614] 	|  	|
| DCNN - ensemble 	|  	|  	|  	| 0.4503 [0.4455, 0.4552] 	| 0.7731 [0.7580, 0.7881] 	| 0.4397 [0.4133, 0.4660] 	| 0.7566 [0.7367, 0.7765] 	| x 	|  	|
| MDE 	|  	|  	|  	| 0.5238 [0.5184, 0.5292] 	| 0.7756 [0.7629, 0.7882] 	| 0.4110 [0.3825, 0.4394] 	| 0.8199 [0.8033, 0.8365] 	| x 	|  	|
| multi_stream 	| 0.8284 [0.8134, 0.8435] 	| 0.6310 [0.5935, 0.6684] 	| 0.7299 [0.7174, 0.7424] 	| 0.3617 [0.3542, 0.3692] 	| 0.6938 [0.6777, 0.7098] 	| 0.4119 [0.3824, 0.4413] 	| 0.7533 [0.7359, 0.7708] 	| x 	|  	|
| Mean Recall 	|  	|  	|  	|  	|  	|  	|  	|  	| x 	|


| **METHOD** 	| **MHEALTH** 	| **PAMAP2** 	| **USCHAD** 	| **UTD-MHAD1** 	| **UTD-MHAD2** 	| **WHARF** 	| **WISDM** 	| **COOK** 	| **Mean F1** 	|
|:-:	|:-:	|:-:	|:-:	|:-:	|:-:	|:-:	|:-:	|:-:	|:-:	|
| [Ha and Choi](https://ieeexplore.ieee.org/document/7727224/) 	| <nobr>0.8896 [0.8740, 0.9051]<nobr/> 	| <nobr>0.6351 [0.5845, 0.6856]<nobr/> 	| <nobr>0.6122 [0.5939, 0.6305]<nobr/> 	| <nobr>0.1030 [0.0949, 0.1110]<nobr/> 	| <nobr>0.6527 [0.6271, 0.6784]<nobr/> 	| <nobr>0.2129 [0.1942, 0.2316]<nobr/> 	| <nobr>0.6021 [0.5856, 0.6186]<nobr/> 	| <nobr>0.3439 [0.3118, 0.3759]<nobr/> 	|  	|
| [Catal et al.](https://www.sciencedirect.com/science/article/pii/S1568494615000447) 	| 0.9371 [0.9257, 0.9485] 	| 0.7939 [0.7636, 0.8242] 	| 0.6735 [0.6597, 0.6872] 	| <nobr>0.3085 [0.3022, 0.3149]<nobr/> 	| 0.7340 [0.7117, 0.7563] 	| 0.2818 [0.2602, 0.3035] 	| 0.6076 [0.5908, 0.6245] 	| <nobr>0.3049 [0.2813, 0.3285]<nobr/> 	|  	|
| [Kim et al.](https://ieeexplore.ieee.org/document/6411901/) 	| 0.9264 [0.9154, 0.9373] 	|  	| 0.5416 [0.5268, 0.5564] 	| 0.3606 [0.3559, 0.3653] 	| 0.6456 [0.6321, 0.6592] 	| 0.2492 [0.2338, 0.2645] 	| 0.3337 [0.3220, 0.3453] 	|  	|  	|
| [Chen and Xue](https://ieeexplore.ieee.org/document/7379395/) 	| 0.8961 [0.8850, 0.9071] 	| 0.6427 [0.5856, 0.6998] 	| 0.7052 [0.6909, 0.7196] 	| x 	| x 	| 0.4241 [0.3959, 0.4522] 	| 0.7237 [0.7059, 0.7415] 	| 0.3633 [0.3334, 0.3933] 	|  	|
| [Jiang and Yin](https://dl.acm.org/citation.cfm?id=2806333) 	|  	| x 	| 0.6792 [0.6653, 0.6931] 	| x 	| x 	| 0.4053 [0.3822, 0.4284] 	| 0.7068 [0.6886, 0.7250] 	| 0.3087 [0.2846, 0.3327] 	|  	|
| [Ha et al.](https://ieeexplore.ieee.org/document/7379657/) 	| 0.8442 [0.8282, 0.8602] 	|  	| x 	| x 	| x 	| x 	| x 	| x 	|  	|
| [Ha and Choi](https://ieeexplore.ieee.org/document/7727224/) 	|  	|  	| x 	| x 	| x 	| x 	| x 	| x 	|  	|
| DeepSense 	|  	| 0.3719 [0.3470, 0.3968] 	| 0.5008 [0.4840, 0.5176] 	|  	|  	|  	|  	| x 	| x 	|
| Jordao et al. 	| 0.4980 [0.4730, 0.5231] 	|  	| 0.6689 [0.6502, 0.6877] 	| 0.4223 [0.4164, 0.4283] 	| 0.7688 [0.7535, 0.7840] 	| 0.4159 [0.3870, 0.4447] 	| 0.7288 [0.7102, 0.7474] 	| 0.3633 [0.3394, 0.3872] 	|  	|
| KimChoi 	| 0.1488 [0.1472, 0.1503] 	|  	| 0.2397 [0.2353, 0.2440] 	| 0.1457 [0.1399, 0.1516] 	| 0.1938 [0.1881, 0.1996] 	| 0.2194 [0.2057, 0.2332] 	| 0.3079 [0.2970, 0.3189] 	|  	|  	|
| Panwar et al. 	| 0.4942 [0.4729, 0.5155] 	| 0.0434 [0.0339, 0.0530] 	| 0.4917 [0.4720, 0.5113] 	| 0.1050 [0.0923, 0.1177] 	| 0.5773 [0.5596, 0.5950] 	| 0.0801 [0.0573, 0.1030] 	| 0.6870 [0.6704, 0.7036] 	| 0.3260 [0.3061, 0.3458] 	|  	|
| DCNN - ensemble 	|  	|  	|  	| 0.4358 [0.4307, 0.4408] 	| 0.6947 [0.6795, 0.7099] 	|  0.4368 [0.4113, 0.4624] 	| 0.7597 [0.7405, 0.7788] 	| x 	|  	|
| MDE 	|  	|  	|  	| 0.5082 [0.5021, 0.5143] 	| 0.7641 [0.7503, 0.7778] 	| 0.4060 [0.3786, 0.4334] 	| 0.7014 [0.6816, 0.7212] 	| x 	|  	|
| multi_stream 	| 0.8070 [0.7899, 0.8241] 	| 0.6258 [0.5890, 0.6626] 	| 0.6944 [0.6801, 0.7086] 	| 0.3467 [0.3391, 0.3544] 	| 0.6842 [0.6677, 0.7007] 	| 0.4119 [0.3830, 0.4408] 	| 0.7462 [0.7294, 0.7629] 	| x 	|  	|
| Mean F1 	|  	|  	|  	|  	|  	|  	|  	|  	|  	|

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
