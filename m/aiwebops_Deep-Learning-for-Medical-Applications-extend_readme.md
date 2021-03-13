# Deep Learning Papers on Medical Image Analysis

## Background
To the best of our knowledge, this is the first list of deep learning papers on medical applications. There are couple of lists for deep learning papers in general, or computer vision, for example [Awesome Deep Learning Papers](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046075d0ae380a4db3495b0abacc45cdc9550899402a5f93ee9ea856380ffe0e8994f6cfa317e6b9f10dac943999e6c5094  In this list, I try to classify the papers based on their deep learning techniques and learning methodology. I believe this list could be a good starting point for DL researchers on Medical Applications. 

## Criteria

1. A list of **top deep learning papers** published since 2015.
2. Papers are collected from peer-reviewed journals and high reputed conferences. However, it may have recent papers on arXiv. 
3. A meta-data is required along with the paper, i.e. Deep Learning technique, Imaging Modality, Area of Interest, Clinical Database (DB). 

*List of Journals / Conferences (J/C):*

- **[Medical Image Analysis (MedIA)](http://u.720life.cn/g/08e1a5f989e3123ed633af2ae433eb355362aa8f8a68cc2293c3346703791fc0c5df815144ff6cf0645de1890a0ba4c5e724e5053d1539158008889c065feb48 
- **[IEEE Transaction on Medical Imaging (IEEE-TMI)](http://u.720life.cn/g/d671cb6b57e5bdacd0875d477d60c81a1efa914c239d1a2452bca221313b92cc 
- **[IEEE Transaction on Biomedical Engineering (IEEE-TBME)](http://u.720life.cn/g/849033b5ddf52c94aaa0b2a1f556f960fd80b3b86769fdc6767602f2ee0f2bfb 
- **[IEEE Journal of Biomedical and Health Informatics (IEEE-JBHI)](http://u.720life.cn/g/8368d2c061e39f76bfedf0b8053d4a235004f7947c1ee5bea03f8c63459ffc59 
- **[International Journal on Computer Assisted Radiology and Surgery (IJCARS)](http://u.720life.cn/g/a50b704f804c379c2fdcea5b9d5061ef9cf8c6b9e5919c0da571c7a805d1a4d831758680d03fbea7c0e821d5cf60846f3f72b0a6444379641b5f5f71703538d2 
- **International Conference on Information Processing in Medical Imaging (IPMI)**
- **International Conference on Medical Image Computing and Computer Assisted Intervention (MICCAI)**
- **International Conference on Information Processing in Computer-Assisted Interventions (IPCAI)**
- **IEEE International Symposium on Biomedical Imaging (ISBI)**

## Shortcuts

*Deep Learning Techniques:*

- NN: Neural Networks 
- MLP: Multilayer Perceptron 
- RBM: Restricted Boltzmann Machine
- SAE: Stacked Auto-Encoders
- CAE: Convolutional Auto-Encoders
- CNN: Convolutional Neural Networks 
- RNN: Recurrent Neural Networks
- LSTM: Long Short Term Memory
- M-CNN: Multi-Scale/View/Stream CNN
- MIL-CNN: Multi-instance Learning CNN
- FCN: Fully Convolutional Networks

*Imaging Modality:*

- US: Ultrasound 
- MR/MRI: Magnetic Resonance Imaging 
- PET: Positron Emission Tomography
- MG: Mammography
- CT: Computed Tompgraphy
- H&E: Hematoxylin & Eosin Histology Images
- RGB: Optical Images 


## Table of Contents
### Deep Learning Techniques 
* [AutoEncoders/ Stacked AutoEncoders](#autoencoders--stacked-autoencoders)
* [Convolutional Neural Networks](#convolutional-neural-networks)
* [Recurrent Neural Networks](#recurrent-neural-networks)
* [Generative Adversarial Networks](#generative-adversarial-networks)

### Medical Applications 
* [Annotation](#annotation)
* [Classification](#classification)
* [Detection/ Localization](#detection--localization)
* [Segmentation](#segmentation)
* [Registration](#registration)
* [Regression](#regression)
* [Image Reconstruction and Post-Processing](#https://arxiv.org/abs/1707.05927)
* [Other tasks](#other-tasks)

* * * 
### Deep Learning Techniques 
#### Auto-Encoders/ Stacked Auto-Encoders
- 

#### Convolutional Neural Networks
- [AggNet: Deep Learning From Crowds for Mitosis Detection in Breast Cancer Histology Images](http://u.720life.cn/g/9e82bf4a493e96d7a7f3c02f5e1db3ea9ce877e15b61806e47f568f689d6ef0fdcd5ada9c4b926697f6c4eeab69ac8f6) 
- [Fast Convolutional Neural Network Training Using Selective Data Sampling: Application to Hemorrhage Detection in Color Fundus Images](http://u.720life.cn/g/9e82bf4a493e96d7a7f3c02f5e1db3ea9ce877e15b61806e47f568f689d6ef0f0eabbdcdf9ab8a23a326c4563ec42ad5346e5e3870e38934c79b5a5460db0130) 

#### Recurrent Neural Networks
- 

#### Generative Adversarial Networks
- [Adversarial Deep Structured Nets for Mass Segmentation from Mammograms](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa0575478f41a19eb4b8308d2f0f4a520b3f082) 

### Medical Applications 

#### Annotation 
| Technique | Modality | Area | Paper Title| DB | J/C | Year |
| ------ | ----------- | ----------- | ----------- |---|----------- | ---- |
| NN | H&E | N/A | Deep learning of feature representation with multiple instance learning for medical image analysis [[pdf]]() | | ICASSP| 2014|
| M-CNN   | H&E | Breast | AggNet: Deep Learning From Crowds for Mitosis Detection in Breast Cancer Histology Images [[pdf]](http://u.720life.cn/g/9e82bf4a493e96d7a7f3c02f5e1db3ea9ce877e15b61806e47f568f689d6ef0fdcd5ada9c4b926697f6c4eeab69ac8f6)  | [AMIDA](amida13.isi.uu.nl)| IEEE-TMI | 2016| 
| FCN | H&E | N/A | Suggestive Annotation: A Deep Active Learning Framework for Biomedical Image Segmentation [pdf](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa05754d6c815f6e3bf01809a0ec9c3798157326286037ed59dbbd44441b31b2685e8e0  | MICCAI | 2017 |
#### Classification

| Technique | Modality | Area | Paper Title| DB | J/C | Year |
| ------ | ----------- | ----------- | ----------- |---|----------- | ---- |
| M-CNN | CT | Lung | Multi-scale Convolutional Neural Networks for Lung Nodule Classification [[pdf]](http://u.720life.cn/g/24f2960c49deba8586ef581bef533f8d674955e8848a82c0e5cb15970db99d05bd8d556d30f06afdfd1313436ad074a8ebf3d229b1b7adc21aa256635e56a5b2)  | [LIDC-IDRI](http://u.720life.cn/g/1247f0847702b3f85b74c8eea606e44e20d1fe7ab0c20a4f7e1ec66375ee3e9bf7d244d51460f06b56dcecb2aee5a934900238d9c0d252b8c1334a479f4a6c34  IPMI| 2015|
| 3D-CNN | MRI | Brain | Predicting Alzheimer's disease: a neuroimaging study with 3D convolutional neural networks [[pdf]](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa0575473551c9ad715264cdff48bd3019a984a)  | [ADNI](adni.loni.usc.edu)| arXiv | 2015 |
| CNN+RNN| RGB | Eye | Automatic Feature Learning to Grade Nuclear Cataracts Based on Deep Learning [[pdf]](http://u.720life.cn/g/77dd4627150412db1373212325c25dcbf511382eb1be134b8d10e9f4e43dd535c03232e7778c5907ff52a60a146cdb63e4116f35f54676fea840112e575652950ddae0fdfc08d60a376fc064fbdb8f99  | IEEE-TBME | 2015|
| CNN   | X-ray | Knee | Quantifying Radiographic Knee Osteoarthritis Severity using Deep Convolutional Neural Networks [[pdf]](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa0575445c1612a5e53224cff0c0f0eee30ed7f)  | [O.E.1](http://u.720life.cn/g/32dcf924535e62ea2a25f065a5f8bbcdacd29d2f15f9e9b941fa6852ee22cfc089f64252373be6a2b97a36efdbb05b65  arXiv | 2016|
| CNN | H&E | Thyroid | A Deep Semantic Mobile Application for Thyroid Cytopathology [[pdf]](http://u.720life.cn/g/79d49ed2813b56eefe1a9e42a9c41f06aa1ffc79eeb690946d308f68d7efa910446a569b458860400282a8c1847ccac8cd867ab448738c8b235de23758ee22ab0f5e215b02fa99ce0c3a89c4196d8204)  | | SPIE | 2016|
| 3D-CNN, 3D-CAE | MRI | Brain | Alzheimer's Disease Diagnostics by a Deeply Supervised Adaptable 3D Convolutional Network [[pdf]](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa05754c0516df817b85976d54d76d762b6f4dd161462fb84c2552e586717622008f22e)  | [ADNI](adni.loni.usc.edu) | arXiv| 2016
| M-CNN | RGB | Skin| Multi-resolution-tract CNN with hybrid pretrained and skin-lesion trained layers [[pdf]](http://u.720life.cn/g/fbf0b36b196a890cc7656a55fea682452214d652fec077d2167d06791dc34e3336a965e7e1ecc2cf59d0d022bb76aab57f0798dac0941ee940bc68abbd62e593eaa223e11591d43eeb0e917c2e1e685f271e895e35e109f91d9d24041b653e36f316717fb0266b13bb227a9dded3672849c74230e49c4be52a6dcce5487ff5e7b700efde8fd3d374393e7bee94443ecb  MLMI | 2016|
| CNN | RGB | Skin, Eye | Towards Automated Melanoma Screening: Exploring Transfer Learning Schemes [[pdf]](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa05754c30508749c861e9fe1bbeb5f27bb83a238979313e41ba5ba58bd2a4c358c7cb6  [EDRA](http://u.720life.cn/g/e4516278455144fc9cd8766e28136e1b4ad9094bff79504b5b0f212c57ad2db0  [DRD](http://u.720life.cn/g/9d2b711779a11e1354812b33245e7526fdf224bda7de164e8b2134a83caf0bb02903b41a493a2408684be14c82b50b0dede80d8351be60cdc6aa2370da9930af)  | arXiv | 2016|
| M-CNN | CT | Lung | Pulmonary Nodule Detection in CT Images: False Positive Reduction Using Multi-View Convolutional Networks [[pdf]](http://u.720life.cn/g/96d7600848be4b856c9e8e2b4a026e4c47b8999bf27eb13fe9cfe090749efcc7331f43cd11f6d4def69b2ad8dd09b046fc6a6c63220f8794bfeb2690a1ae542a4cbeda8212665f978f1d7084a13cc0437f8c27e8d4817ef56a37742e0fe66824e4a5c3174f5e6f5ba51023c52a85857eea2fd7e2710cc08381d23924bb242fd2b7787838cb267ea5d82a38a778a4f95dee0e256946ffad044246354fc7e7b75fda6edb107eadb469d51bee658cb74bd6026ec3b5542fd1e9541e5482177d9f14db3ab2200c7f86c3c627f92e6103ea0697cd04829118df3c915402bad81651bd)  |  [LIDC-IDRI](http://u.720life.cn/g/1247f0847702b3f85b74c8eea606e44e20d1fe7ab0c20a4f7e1ec66375ee3e9bf7d244d51460f06b56dcecb2aee5a934939dff65e851d07854a48d28d69047b3  [ANODE09](http://u.720life.cn/g/5892d8b03ec20efef351d59f5631a656daa4493fc3324ee4b4bb4cdf8641a7f6322f20eb69e2fa60edc5cfbbd9f2552d  [DLCST](http://u.720life.cn/g/6e3f2817f08226630087e520796bbf9d48b460bf57c97047bbd6a9da1e7447bf070c295422c1049a18a6e555d69d320bf4a617842464b65cbc075fdba368c58d)  | IEEE-TMI | 2016|
| 3D-CNN | CT | Lung | DeepLung: Deep 3D Dual Path Nets for Automated Pulmonary Nodule Detection and Classification [[pdf]](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa057542a36fd1c8fe451711b6b108a85af8efe)  |  [LIDC-IDRI](http://u.720life.cn/g/1247f0847702b3f85b74c8eea606e44e20d1fe7ab0c20a4f7e1ec66375ee3e9bf7d244d51460f06b56dcecb2aee5a934939dff65e851d07854a48d28d69047b3  [LUNA16](http://u.720life.cn/g/775c34a279cd1136861de8bede59fe733ef259d5f74ac563ef6772dec8c526e1f862a47d1be52f7704bb6afc5c4ab5b6)  | IEEE-WACV | 2018|
| 3D-CNN | MRI | Brain | 3D Deep Learning for Multi-modal Imaging-Guided Survival Time Prediction of Brain Tumor Patients [[pdf]](http://u.720life.cn/g/d552b4456d1f9c75523de2df686688309ab612bce571a49ae176e48f6d2f94c11242bd899b8ee32262c66226bfd2d6b4023ae3d807b47afcfbcf51144df658f3  |MICCAI | 2016|
| SAE | US, CT | Breast, Lung | Computer-Aided Diagnosis with Deep Learning Architecture: Applications to Breast Lesions in US Images and Pulmonary Nodules in CT Scans [[pdf]](http://u.720life.cn/g/f6caaaec179b2316e231f5c3dc65aeda01444dc11ff473f75b59a22d687230f5804a636d795be9c39ef96a3a72503ab4dbb31cbd663e2f42077f8692579a76ee3892db74c5d7259c3f90c97848e81d68)  | [LIDC-IDRI](http://u.720life.cn/g/1247f0847702b3f85b74c8eea606e44e20d1fe7ab0c20a4f7e1ec66375ee3e9bf7d244d51460f06b56dcecb2aee5a934900238d9c0d252b8c1334a479f4a6c34  Nature | 2016| 
| CAE | MG | Breast |Unsupervised deep learning applied to breast density segmentation and mammographic risk scoring [[pdf]](http://u.720life.cn/g/2c4fb3daa48f7300ed998f90e52a5fd259b69638184cc2a5b72cf2b9a66da909a1db6de9d3e8042986b23b84e98442f6)  | | IEEE-TMI | 2016| 
| MIL-CNN | MG | Breast |Deep multi-instance networks with sparse label assignment for whole mammogram classification [[pdf]](http://u.720life.cn/g/24f2960c49deba8586ef581bef533f8d674955e8848a82c0e5cb15970db99d05bd8d556d30f06afdfd1313436ad074a8defde451046b97a15437340465d7aa26)  | [INbreast](http://u.720life.cn/g/88be3b970053c54b5fd1dc0fadc82276f8dfb9662c15726424e366b1c608741ddd010936cfef642ce3f3e12ce8cb162ab8659e2ba993429ba351911b4157b1edc3eeda4e21b6ec05400909f425f3f087e4110f6e7d5b38a3a453c977ac88ee46)  | MICCAI | 2017| 
| GCN | MRI | Brain | Spectral Graph Convolutions for Population-based Disease Prediction [[pdf]](http://u.720life.cn/g/bcadecbe8a851bdefeb338f9021d9ccdbd556de4e325b87d73da91cfb137d02c)  | [ADNI](http://u.720life.cn/g/cca132c4c53efcb25d1022fb74e3fc363f709158bda11562b58923f084cb0237  [ABIDE](http://u.720life.cn/g/21a7c37d1864be1bb1826edca7adbf9e4758320b9149fc9c8d14e5b3be090ff333604a81e0961136b81956c1adf48538aaf6d62fd998788559192a4f1bea5f02)  | arXiv | 2017| 
| CNN | RGB | Skin | Dermatologist-level classification of skin cancer with deep neural networks | | Nature | 2017 |
| FCN + CNN  | MRI | Liver-Liver Tumor | SurvivalNet: Predicting patient survival from diffusion weighted magnetic resonance images using cascaded fully convolutional and 3D convolutional neural networks [[pdf]](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa057546d83902df3029b7a0b6cb8a87be20512)  | | ISBI | 2017 |




#### Detection / Localization

| Technique | Modality | Area | Paper Title| DB | J/C | Year |
| ------ | ----------- | ----------- | ----------- |---|----------- | ---- |
| MLP   | CT | Head-Neck | 3D Deep Learning for Efficient and Robust Landmark Detection in Volumetric Data [[pdf]](http://u.720life.cn/g/77dd4627150412db1373212325c25dcbf511382eb1be134b8d10e9f4e43dd53591bdc36b56aabe437684ef65d1e40af11fb020b2f60a96f35dd3478bc1438b264ef7f1218d1e6aa3a8ca7fdffd27a52f)  | | MICCAI | 2015|
| CNN   | US | Fetal | Standard Plane Localization in Fetal Ultrasound via Domain Transferred Deep Neural Networks [[pdf]](http://u.720life.cn/g/9e82bf4a493e96d7a7f3c02f5e1db3eafd7f7e9ef9646f27c6ac43de054b540acf7d8fe1c7aca4ef82d145ea155e81fc19844ee6b9c7ca0953f775e076ec6993)  | | IEEE-JBHI | 2015|
| 2.5D-CNN   | MRI | Femur | Automated anatomical landmark detection ondistal femur surface using convolutional neural network [[pdf]](http://u.720life.cn/g/077a8b15a851ba34a1350a4f5046d7dad7e3d4a6e28fcde90a9128bd26876bca4f19b11fad474a9f500ea748ad82cb27a4670c3aa9abfe34ef187953ffeb4f6c)  | [OAI](http://u.720life.cn/g/32dcf924535e62ea2a25f065a5f8bbcdacd29d2f15f9e9b941fa6852ee22cfc089f64252373be6a2b97a36efdbb05b65  ISBI | 2015|
| LSTM   | US | Fetal | Automatic Fetal Ultrasound Standard Plane Detection Using Knowledge Transferred Recurrent Neural Networks [[pdf]](http://u.720life.cn/g/24f2960c49deba8586ef581bef533f8d674955e8848a82c0e5cb15970db99d05bd8d556d30f06afdfd1313436ad074a8560f94835285548bb822034f23609e17)  | | MICCAI | 2015|
| CNN   | X-ray, MRI | Hand | Regressing Heatmaps for Multiple Landmark Localization using CNNs [[pdf]](http://u.720life.cn/g/71de71290132de39a663b16ccd0fc85a937c0b3d069f9fbabd9586fd8a8e11905e7f2b793181d403b05fcc34d5c76956fb467c2d12bc8fe6eb5f2549e69367db44dbdf4e4eb6f27dee32aaf5217bbf1554a85f28ddeabc4ecf29a74437fdd4d0c735c6ffb37b097466cffba73c8cfcebe41f20173a719a8ed4f0c77211341f20)  | [DHADS](http://u.720life.cn/g/ae4501107caa61c1ecba7dccc5be0d7a105a80e1267fca77cc1768b5cedf5287  MICCAI | 2016|
| CNN   | MRI, US, CT | - | An artificial agent for anatomical landmark detection in medical images [[pdf]](http://u.720life.cn/g/8d4d98268284f28afb6356e16e20bf16b31fa9f7522c7f16e786c4016feb9a68fa313866165f7ab79f15f501f2b5bd0487302d6b2479c4d0deb10661d96ba6d80dbdada50f11a9bf8de34a2d059601eb43ca086b85f354ddf18ce6b58b7c45b2)  | [SATCOM](http://u.720life.cn/g/7c4d81b0d44ea842e98f06aa48d8d0e9ae8a35cd4e04246f38f6047a3e4f470f1569337ee49fc76ff8238cbc8ba653fa473905170b79fbc8658f8d2a46e35d07acb16c18baa765f70e24300ae6d01a80  MICCAI | 2016|
| FCN   | US | Fetal | Real-time Standard Scan Plane Detection and Localisation in Fetal Ultrasound using Fully Convolutional Neural Networks [[pdf]](http://u.720life.cn/g/70a18f579b91bdc155e99647d42ee04993a76feddd19de4e7397fc9525e5ce83f6244e01e0eca9dcc594534a8bcea6c2ddec5b73f42698cdcce13396b87377786dcb135f9d4ff61dc2a03d3bdba78c95)  | | MICCAI | 2016|
| CNN+LSTM   | MRI | Heart | Recognizing end-diastole and end-systole frames via deep temporal regression network [[pdf]](http://u.720life.cn/g/24f2960c49deba8586ef581bef533f8d674955e8848a82c0e5cb15970db99d05bd8d556d30f06afdfd1313436ad074a84702486b0a049e225588187d6116b25e)  | | MICCAI | 2016|
| M-CNN  | MRI | Heart | Improving Computer-Aided Detection Using Convolutional Neural Networks and Random View Aggregation Neural Networks [[pdf]](http://u.720life.cn/g/dd049506d401118eaa05312995cb028869e3f589714be5980994352babd3924b6a827bb7a06d88c5c9fc4fcc32311b98a314c5f6aab3464df4c630e07bd2837e)  | | IEEE-TMI | 2016|
| CNN  | PET/CT | Heart | Automated detection of pulmonary nodules in PET/CT images: Ensemble false-positive reduction using a convolutional neural network technique Neural Networks [[pdf]](http://u.720life.cn/g/f11313a71c49da40b1647be5a711b61bfa465b46092db8bfc4b0ed974d14e5b23433d0e1fe7d8d6275d2b1362a027c755dc6f26d00244dac4d850b1430ff8447)  | | MP | 2016|
| 3D-CNN  | MRI | Brain | Automatic Detection of Cerebral Microbleeds From MR Images via 3D Convolutional Neural Networks [[pdf]](http://u.720life.cn/g/9e82bf4a493e96d7a7f3c02f5e1db3ea9ce877e15b61806e47f568f689d6ef0fa5e30debf6dfece88d40d9e527e62f00214690bdc38ee63da163d6288373ec7f)  | | IEEE-TMI | 2016|
| CNN  | X-ray, MG | - | Self-Transfer Learning for Fully Weakly Supervised Lesion Localization [[pdf]](http://u.720life.cn/g/24f2960c49deba8586ef581bef533f8d674955e8848a82c0e5cb15970db99d05bd8d556d30f06afdfd1313436ad074a85799811a685bd1cfc39984f6e1d65852)  | [NIH,China](http://u.720life.cn/g/9e82bf4a493e96d7a7f3c02f5e1db3eafd7f7e9ef9646f27c6ac43de054b540acf7d8fe1c7aca4ef82d145ea155e81fc49630adca3352f763229934028f31274  [DDSM,MIAS](http://u.720life.cn/g/6937566f5980030ac8a1b4a4999782260ed9598613ad7146983d4df16ec4a8b73a67e6ba4815f78d59e06d8291644eb5)   | MICCAI | 2016|
| CNN  | RGB | Eye | Fast Convolutional Neural Network Training Using Selective Data Sampling: Application to Hemorrhage Detection in Color Fundus Images [[pdf]](http://u.720life.cn/g/9e82bf4a493e96d7a7f3c02f5e1db3ea9ce877e15b61806e47f568f689d6ef0f0eabbdcdf9ab8a23a326c4563ec42ad5346e5e3870e38934c79b5a5460db0130)  | [DRD](http://u.720life.cn/g/9d2b711779a11e1354812b33245e7526fdf224bda7de164e8b2134a83caf0bb02903b41a493a2408684be14c82b50b0d8fb8a9b636a40df860ceb710a546bafb  [MESSIDOR](http://u.720life.cn/g/c0eacde6282fea3a9ed300796330be49e15ca707ec8366556a65be244b96cd47a743e8ac7a7dc480bb8301e703c75f9d8148aeb119c9c2d1c83861f4b5853491)   | MICCAI | 2016|
| GAN  | - | - | Unsupervised Anomaly Detection with Generative Adversarial Networks to Guide Marker Discovery | | IPMI | 2017|
| FCN | X-ray | Cardiac | CathNets: Detection and Single-View Depth Prediction of Catheter Electrodes | | MIAR | 2016|
| 3D-CNN | CT | Lung | DeepLung: Deep 3D Dual Path Nets for Automated Pulmonary Nodule Detection and Classification [[pdf]](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa057542a36fd1c8fe451711b6b108a85af8efe)  |  [LIDC-IDRI](http://u.720life.cn/g/1247f0847702b3f85b74c8eea606e44e20d1fe7ab0c20a4f7e1ec66375ee3e9bf7d244d51460f06b56dcecb2aee5a934939dff65e851d07854a48d28d69047b3  [LUNA16](http://u.720life.cn/g/775c34a279cd1136861de8bede59fe733ef259d5f74ac563ef6772dec8c526e1f862a47d1be52f7704bb6afc5c4ab5b6)  | IEEE-WACV | 2018|
| 3D-CNN | CT | Lung | DeepEM: Deep 3D ConvNets with EM for weakly supervised pulmonary nodule detection [[pdf]](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa05754f772f9da7575badf5294a2a10319620a4c78992155ab81fdf4d252be6630ab2f)  |  [LIDC-IDRI](http://u.720life.cn/g/1247f0847702b3f85b74c8eea606e44e20d1fe7ab0c20a4f7e1ec66375ee3e9bf7d244d51460f06b56dcecb2aee5a934939dff65e851d07854a48d28d69047b3  [LUNA16](http://u.720life.cn/g/775c34a279cd1136861de8bede59fe733ef259d5f74ac563ef6772dec8c526e1f862a47d1be52f7704bb6afc5c4ab5b6)  | MICCAI | 2018|

#### Segmentation
| Technique | Modality | Area | Paper Title| DB | J/C | Year |
| ------ | ----------- | ----------- | ----------- |---|----------- | ---- |
| U-Net  | - | - | U-net: Convolutional networks for biomedical image segmentation | | MICCAI | 2015|
| FCN   | MRI | Head-Neck | Efficient multi-scale 3D CNN with fully connected CRF for accurate brain lesion segmentation [[pdf]](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa057541afdb33c0042b9a6a61a6a8b3a1cf3c5)  | | arXiv | 2016 |
| U-Net   | CT | Head-Neck | AnatomyNet: Deep learning for fast and fully automated whole‐volume segmentation of head and neck anatomy [[pdf]](http://u.720life.cn/g/96d7600848be4b856c9e8e2b4a026e4c47b8999bf27eb13fe9cfe090749efcc77c8b84b15a87410e826e70bbb5c34d4c9166543bf7031b5ebdc2eda48de6e03757893bcecaef8940393d64979a22a793fe563fd35c3bed24a2efcafd20230da693e6f45116b1365f75d32e00d34ef4a1aa9af840247009130c3cc7775626d793602ab543e8c195651057fdaf36b7a65a2da2178bb9ec148a6e340ebb90dbb629aa48610efabc2ffcf635865cdd9a2bb1bc2a918e74ba5ce640cd8c981414c1ae74e679339fd357c0efb1ebbb5a98c50cf5a5a6b3d4dc1b9350cfb0fe057bf4855706406264ba3f474d86fa2121e1c101275b63cdd1a6ffe0dff1ceaa0afed1f1b37c4a447f557d24e5e5e9098880a522a566673ab8cb15af3970dd936bc88bb48b8ba358b4d1228f6e99d1d777b89c8f2182fc21818744a276ac93ac1d597570)  | | Medical Physics | 2018 |
| FCN   | CT | Liver-Liver Tumor | Automatic Liver and Lesion Segmentation in CT Using Cascaded Fully Convolutional Neural Networks and 3D Conditional Random Fields  [[pdf]](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa057546e8c2ab38fe283136a1123b38c614a1f)  | | MICCAI | 2016 |
| 3D-CNN | MRI | Spine | Model-Based Segmentation of Vertebral Bodies from MR Images with 3D CNNs | | MICCAI | 2016 |
| FCN   | CT | Liver-Liver Tumor | Automatic Liver and Tumor Segmentation of CT and MRI Volumes using Cascaded Fully Convolutional Neural Networks [[pdf]](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa05754f637f384490c81fcbe5c0e0f164a425b)  | | arXiv | 2017 |
| FCN   | MRI | Liver-Liver Tumor | SurvivalNet: Predicting patient survival from diffusion weighted magnetic resonance images using cascaded fully convolutional and 3D convolutional neural networks [[pdf]](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa057546d83902df3029b7a0b6cb8a87be20512)  | | ISBI | 2017 |
| 3D-CNN | Diffusion MRI | Brain | q-Space Deep Learning: Twelve-Fold Shorter and Model-Free Diffusion MRI [[pdf]](http://u.720life.cn/g/9e82bf4a493e96d7a7f3c02f5e1db3ea9ce877e15b61806e47f568f689d6ef0fd9035801b47ecd54b6313e5401ec0120)  (Section II.B.2) | | IEEE-TMI | 2016 |
| GAN   | MG | Breast Mass | Adversarial Deep Structured Nets for Mass Segmentation from Mammograms [[pdf]](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa0575478f41a19eb4b8308d2f0f4a520b3f082)  | [INbreast](http://u.720life.cn/g/88be3b970053c54b5fd1dc0fadc82276f8dfb9662c15726424e366b1c608741ddd010936cfef642ce3f3e12ce8cb162ab8659e2ba993429ba351911b4157b1edc3eeda4e21b6ec05400909f425f3f0872f6c2cb2fec05887c6a4ed61b82f62e8  [DDSM-BCRP](http://u.720life.cn/g/a469d290d551ddef31d1c1345d1af66fcaef33d60aa553860d6c99dc2f89c145a0e975859b39373d6c733356e9684090cc8f7941a23266f46be045064a914fc7)  | ISBI | 2018 |
| 3D-CNN | CT | Liver | 3D Deeply Supervised Network for Automatic Liver Segmentation from CT Volumes [pdf](http://u.720life.cn/g/24f2960c49deba8586ef581bef533f8d1ff8a51503494a5dfc3515808ebbb2a70962547975719ac2adb5273f704d5ca76e5ff33daf1f814962c23a4eb9c9859ac200d41f85663ad37aa41874ff39e72b)  | | MICCAI | 2017 |
| 3D-CNN | MRI | Brain | Unsupervised domain adaptation in brain lesion segmentation with adversarial networks [pdf](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa057542b17f93f2b7856a940758e28886ad48f63e935a1118d9004e0dfb804d9834f71  ) | | IPMI | 2017
| FCN | FUNDUS | Retina | A Fully Convolutional Neural Network based Structured Prediction Approach Towards the Retinal Vessel Segmentation [pdf](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa057540ef1cbbbf1aec72fae7bfb8ee44416c6)  | | ISBI | 2017

#### Registration
| Technique | Modality | Area | Paper Title| DB | J/C | Year |
| ------ | ----------- | ----------- | ----------- |---|----------- | ---- |
| 3D-CNN | CT | Spine | An Artificial Agent for Robust Image Registration [[pdf]](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa0575455c0417f0e6f50c144c8dc0e03e47c68203f8007eb50c98482c8f4e13921ca6f)  | | | 2016 |

#### Regression

| Technique | Modality | Area | Paper Title| DB | J/C | Year |
| ------ | ----------- | ----------- | ----------- |---|----------- | ---- |
| 2.5D-CNN   | MRI | | Automated anatomical landmark detection ondistal femur surface using convolutional neural network [[pdf]](http://u.720life.cn/g/077a8b15a851ba34a1350a4f5046d7dad7e3d4a6e28fcde90a9128bd26876bca4f19b11fad474a9f500ea748ad82cb27a4670c3aa9abfe34ef187953ffeb4f6c)  | [OAI](http://u.720life.cn/g/32dcf924535e62ea2a25f065a5f8bbcdacd29d2f15f9e9b941fa6852ee22cfc089f64252373be6a2b97a36efdbb05b65  ISBI | 2015|
| 3D-CNN | Diffusion MRI | Brain | q-Space Deep Learning: Twelve-Fold Shorter and Model-Free Diffusion MRI [[pdf]](http://u.720life.cn/g/9e82bf4a493e96d7a7f3c02f5e1db3ea9ce877e15b61806e47f568f689d6ef0fd9035801b47ecd54b6313e5401ec0120)  (Section II.B.1) | [[HCP]](http://u.720life.cn/g/0b32dd526643b1895db5abe2b92bc799329d7a0f34ec71ef3230fc76df60f874)  and other | IEEE-TMI | 2016 |

#### Image Reconstruction and Post Processing
| Technique | Modality | Area | Paper Title| DB | J/C | Year |
| ------ | ----------- | ----------- | ----------- |---|----------- | ---- |
| CNN | CS-MRI | | A Deep Cascade of Convolutional Neural Networks for Dynamic MR Image Reconstruction [pdf](http://u.720life.cn/g/9e82bf4a493e96d7a7f3c02f5e1db3eafd7f7e9ef9646f27c6ac43de054b540aeb1643764e442238018dc9a3d33dcdceae415871536b7ebe96fc7829526c075c)  | | IEEE-TMI | 2017 |
| GAN | CS-MRI | | Deep Generative Adversarial Networks for Compressed Sensing Automates MRI [pdf](http://u.720life.cn/g/70a18f579b91bdc155e99647d42ee04946e3c1f8a6d58ac17f2ebad4ab9c606cfe8f3700a278b99c6a4493411321a85cd0baa6b58fd63b369205d0a2f0bbfd7514e002e3fe9a1a76f0c6f148129304d1)  | | NIPS | 2017 |

#### Image synthesis for data augmentation
| Technique | Modality | Area | Paper Title| DB | J/C | Year |
| ------ | ----------- | ----------- | ----------- |---|----------- | ---- |
| GAN | RGB (Microscopy) | Red Blood Cells | Red blood cell image generation for data augmentation using Conditional Generative Adversarial Networks [[pdf]](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa057547382f29ddbbe3e34eaeba9d06716ef6c)  | | arXiv | 2019 |
| GAN | MRI | Brain | Learning Data Augmentation for Brain Tumor Segmentation with Coarse-to-Fine Generative Adversarial Networks [[pdf]](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa05754d63260da8b954cf191784e5a311de81eedf310fc45a75d70a271654bd04ca098)  | | arXiv | 2018 |
| GAN | MRI | Brain | Medical Image Synthesis for Data Augmentation and Anonymization using Generative Adversarial Networks [[pdf]](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa05754f8c4c861c9bd8aba819c367509015c4cde9a4d420817ceb27b77ff53e4d84ce2)  | | arXiv | 2018 |
| GAN | CT, MRI | Brain | GAN Augmentation: Augmenting Training Data using Generative Adversarial Networks [[pdf]](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa0575474f4eef3bbf5c2c1177f0d608eebf26b62e295b87c977106f1252cbfc9129285)  | | arXiv | 2018 |
| GAN | CT | Liver | GAN-based Synthetic Medical Image Augmentation for increased CNN Performance in Liver Lesion Classification [[pdf]](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa05754cb3104d3307bd76c7d16e9d97c80e0f52ff9865752321ee0177877af99b32b41)  | | arXiv | 2018 |


#### Other tasks
- 


## References 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)