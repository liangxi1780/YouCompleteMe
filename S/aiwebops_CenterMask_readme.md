# [CenterMask](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa05754f5df8d9f0edddee67b4dbe8bc7196104)  : Real-Time Anchor-Free Instance Segmentation


![architecture](figures/architecture.png)

## Abstract

We propose a simple yet efficient anchor-free instance segmentation, called **CenterMask**, that adds a novel spatial attention-guided mask (SAG-Mask) branch to anchor-free one stage object detector (FCOS) in the same vein with Mask R-CNN. Plugged into the FCOS object detector, the SAG-Mask branch predicts a segmentation mask on each box with the spatial attention map that helps to focus on informative pixels and suppress noise. We also present an improved **VoVNetV2** backbone networks with two effective strategies: (1) residual connection for alleviating the saturation problem of larger VoVNet and (2) effective Squeeze-Excitation (eSE) dealing with the information loss problem of original SE. With SAG-Mask and VoVNetV2, we deign CenterMask and CenterMask-Lite that are targeted to large and small models, respectively. CenterMask outperforms all previous state-of-the-art models at a much faster speed. CenterMask-Lite also achieves 33.4% mask AP / 38.0% box AP, outperforming YOLACT by 2.6 / 7.0 AP gain, respectively, at over 35fps on Titan Xp. We hope that CenterMask and VoVNetV2 can serve as a solid baseline of real-time instance segmentation and backbone network for various vision tasks, respectively. 

## Highlights
- ***First* anchor-free one-stage instance segmentation.** To the best of our knowledge, **CenterMask** is the first instance segmentation on top of anchor-free object detection (15/11/2019).
- **Toward Real-Time: CenterMask-Lite.**  This works provide not only large-scale CenterMask but also lightweight CenterMask-Lite that can run at real-time speed (> 30 fps).
- **State-of-the-art performance.**  CenterMask outperforms Mask R-CNN, TensorMask, and ShapeMask at much faster speed and CenterMask-Lite models also surpass YOLACT or YOLACT++ by large margins.
- **Well balanced (speed/accuracy) backbone network, VoVNetV2.**  VoVNetV2 shows better performance and faster speed than ResNe(X)t or HRNet.

## Updates
- Open the official repo and code will be released after refactoring. (05/12/2019)
- Release code and MobileNetV2 & ResNet backbone models shown in the [[`paper`]](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa05754f5df8d9f0edddee67b4dbe8bc7196104ab8bd829ca1b3ed9885b6a0bdacc94f9  (10/12/2019)
- Upload the VoVNetV2 backbone models. (02/01/2020)
- Open VoVNetV2 backbone for [Detectron2](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a0e50a90cce0abf558678bb0e474dbaeaa002b601f0bcebdb6a5963c5103d1a7dcdc8c08615d2aa852b18e12f57146d92646d9b0335e4f29b648a7f48382de87)  --> [vovnet-detectron2](http://u.720life.cn/g/54145d0471d91890860f7f8463c030469277ca11f4d4db818162ec1e2ca2c26039a9c945a6263e6b36d1c0b01a4468ce7fe845dafea085e2c58fe068c0deec3f  (08/01/2020)
- Upload CenterMask-Lite models trained for 48 epochs outperforming [YOLACT](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa05754f06e9f45e852ed91687ef49e4592dfa1)  or [YOLACT++](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa057547de5c069a4092ac57a6250f7c06508efb5e21d89daf38a5cfceed44e065dabf4  (14/01/2020)
- [centermask2](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462d6e07e8df517466695f48fa798f613e4e7f6f50dcaafabd132d27935ec07fb1)  has been released. (20/02/2020)
## Models
### Environment
- V100 or Titan Xp GPU
- CUDA 10.0 
- cuDNN7.3 
- pytorch1.1
- Implemented on [fcos](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462cc4fcbd193e46b97ce94be291de32068e32776aaf173932c0ae6f27f7c25740)  and [maskrcn-benchmark](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304697d9ece9d0ba791376c04b68e0cd9a5bc2f03f0f0b3f69be7bb7e1fe06be0d6a97eccd6a9a977588887154b29137b070)  
- [GoogleDrive weight download](http://u.720life.cn/g/3a38f42308c8ee71aa166c0591609e00180f4b51c3f0e4d083b64b9277a25882ea98159aa2a1475c015a590e5316f27120f6bd6b9d4737d937293a487eee0e79a6364efa14adb4229710ecea6461307b9ce9ee9fe8c029f5270db95c87e3deef) 
### coco test-dev results

|Detector | Backbone |  epoch |   Mask AP (AP/APs/APm/APl) | Box AP (AP/APs/APm/APl) |  Time (ms) | GPU |Weight |
|----------|----------|:--------------:|:-------------------:|:------------------------:|:--------------------------:| :---:|:---:|
| [ShapeMask](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa057545d83aa27f721cb345a3c4cb399ce018d)      | R-101-FPN   |N/A |            37.4/16.1/40.1/53.8                  | 42.2/24.9/45.2/52.7      | 125| V100| - |
 | [TensorMask](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa05754b5f955f668c484de66a574aac2e6ff2c)      | R-101-FPN  | 72 |  37.1/17.4/39.1/51.6         | -                  | 380      |V100| - |
 [RetinaMask](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa05754654a03a1e25fdaf8ac516726702be572)     | R-101-FPN   |  24 |    34.7/14.3/36.7/50.5     | 41.4/23.0/44.5/53.0                  | 98  |V100| - |
| [Mask R-CNN](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa05754571ec4657e43edbc42b8006e121daca2)      | R-101-FPN   | 24 |   37.9/18.1/40.3/53.3       | 42.2/24.9/45.2/52.7                  |  94     |V100| -                          |[link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00fac0def52cd77c258805613ccc733a008426a4f0dacdea3cde02d507f3460a936072473f956fce8bc87919f6ceb886c0e98230cb43ae643ec468efb7a2e8281e2 
| **CenterMask**    | R-101-FPN   |    24 |   38.3/17.7/40.8/54.5|     43.1/25.2/46.1/54.4              | **72**      |V100| [link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00fd2dac5228e6079e25980fce139aa195b812847bb10cfd1e5bbfacfce6b4d6711c9d40c64a511e77efd45e9eba40090ca71ee68f5bd3cbae58d8eca8c54e7db3a 
| **CenterMask**    | X-101-FPN   |    36 |   39.6/19.7/42.0/55.2|     44.6/27.1/47.2/55.2              | 123      |V100| [link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00f4adc90ef8239304fdabe2bf4bc3a9c362c6a032b3123e4face412902b1fc7723e0d3a7f532ad0ecf2806f4f67255e2c451e2b4577fba4f15ce03b2b533e6324a 
| **CenterMask**    | V2-99-FPN |    36 |   40.6/20.1/42.8/57.0|     45.8/27.8/48.3/57.6              | 84      |V100| [link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00ff5451f98823bf2a957ffc42a92e4447d826e28061579479501ed23243d5e4c09fd74bcf108635c199351e2b09f9122bde45d2155ef40fe52ad8ac5e16f572bd6 
||
| [YOLACT-400](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa05754f06e9f45e852ed91687ef49e4592dfa1)      | R-101-FPN   |    48 |    24.9/5.0/25.3/45.0    |         28.4/10.7/28.9/43.1          |  22   | Xp |-|
| **CenterMask-Lite**    | MV2-FPN   |   48 |  26.7/9.0/27.0/40.9     |    30.2/14.2/31.9/40.9          | **20**      | Xp |[link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00ff83f03e12cd811186d106eb40867d16c1bef80fdb0ba89c7fdd118a1574c74a2831a17d830bbcd75a3164a46e2325b6729801e2408618d5ef6c9068e8a454f3b2de58d1b1428a2bf50d3e4a04e92c9d3 
||
| [YOLACT-550](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa05754f06e9f45e852ed91687ef49e4592dfa1)      | R-50-FPN   |   48 |    28.2/9.2/29.3/44.8    | 30.3/14.0/31.2/43.0|23|Xp|-|
| **CenterMask-Lite**    | V2-19-FPN   |   48 |   32.4/13.6/33.8/47.2    |    35.9/19.6/38.0/45.9         | **23**      | Xp |[link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00fc851134937153f1dceffd081556ff9eba872fde5365613dce81b7becc36d6c54c145a11c7a7b00cd16bd15e1a476e2dc584167e42d1da46cb08c6213bb5e133ad22c03140458e66d4b98b9bbb5bca913 
||
| [YOLACT-550](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa05754f06e9f45e852ed91687ef49e4592dfa1)      | R-101-FPN   |   48 |     29.8/9.9/31.3/47.7   | 31.0/14.4/31.8/43.7| 30 | Xp| - |
| [YOLACT-550++](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa057547de5c069a4092ac57a6250f7c06508ef)      | R-50-FPN   |   48 |    34.1/11.7/36.1/53.6    | - |29|Xp|-|
| [YOLACT-550++](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa057547de5c069a4092ac57a6250f7c06508ef)      | R-101-FPN   |   48 |     34.6/11.9/36.8/55.1   | - | 36 | Xp| - |
| **CenterMask-Lite**     | R-50-FPN   |   48 |     32.9/12.9/34.7/48.7   | 36.7/18.7/39.4/48.2                  |   29    | Xp         |[link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00f7c359e57aedafbc2eff1c213dc8f51a2aa7a79587579a18eddf77141018dcac05bfd8f5e2513ed6dab56bbc161c41fca1c4b086aa703d956fd001095f017dc2cee9a41a58de85c71c6f8cb381a3225ce 
| **CenterMask-Lite**     | V2-39-FPN   |   48 |     36.3/15.6/38.1/53.1   |         40.7/22.4/43.2/53.5          |   **28**    | Xp         |[link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00fae3fe84ad92f82402c23b32313c864bd4ca3ee99da416f80d5c4a6a63bc289f30cef759e40251a5ce5a51cd07769facd63c31a508d112b86b0a0c201d8b172807f0778b2ac66a0b83fe9caf0f23e2fd0 


*Note that RetinaMask, Mask R-CNN, and CenterMask are implemented by using same baseline code([maskrcnn-benchmark](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304697d9ece9d0ba791376c04b68e0cd9a5bc2f03f0f0b3f69be7bb7e1fe06be0d6a97eccd6a9a977588887154b29137b070)  and all models are trained using multi-scale training augmentation.*\
*We expect that if we implement our CenterMask based on [detectron2](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304697d9ece9d0ba791376c04b68e0cd9a5b64bfd256c5e50bfa356e6c3f1bc98f76  it will get better performance.*\
*24/36/48/72 epoch are same as 2x/3x/4x/6x training schedule in [detectron](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304697d9ece9d0ba791376c04b68e0cd9a5b9590140d252352a35ac202c5cf94ad3b  respectively.*\
*Training CenterMask-Lite models longer (24 --> 48 epochs same as YOLACT) boosts ther performance, widening the performance gap from YOLACT and even YOLACT++.*


### coco val2017 results
|Detector | Backbone |  epoch |   Mask AP (AP/APs/APm/APl) | Box AP (AP/APs/APm/APl) |  Time (ms) | Weight |
|----------|----------|:--------------:|:-------------------:|:------------------------:| :---:|:---:|
| **CenterMask**    | MV2-FPN   |    36 | 31.2/14.5/32.8/46.3  |       35.5/20.6/38.0/46.8            | **56**      | [link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00fe61b93b257dfa723bb424ab434931a94d30c31cf341533559c07338c140d1ab78f5d915e16c253f02f5ccaa680b34ee39645d41f2354a62f17f0a42a5ccbb394 
| **CenterMask**    | **V2-19-FPN**    |    36 |  34.7/17.3/37.5/49.6 |       39.7/24.6/42.7/50.8            | 59      | [link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00f42b14319bab68712e086d05649be3c878e7ad9fa212fe97be7c6b24eae12d0f2ae543e9f37debaf42a3f34d6edd607ee39a8e8468947bdc6f88fd7ba435780a3b1c3b4310ca86b858b4fad852d9bcf54 
||
| Mask R-CNN    | R-50-FPN   |    24 |   35.9/17.1/38.9/52.0 |     39.7/24.0/43.0/50.8              | 77      | [link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00f08708eb69c82709e2a9d1d33d01a1306c9f684e28e3d671ca85a0ac658d2334e9e3a61d806044a412564b57022221e9885bd23fb831642ce018e2d8ff5378774 
| **CenterMask**    | R-50-FPN   |    24 | 36.4/17.3/39.5/52.7  |       41.2/24.9/45.1/53.0            | 72      | [link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00f72fba6efd12505cd7a241f6620af939ff966bfcc3d7865d676de65905759cf87d5e8eaa3f18719214f7470b2ae1c2c0f436c1c6107e1cf76cac4c67516c2ea1d 
| **CenterMask**    | **V2-39-FPN**   |    24 | 37.7/17.9/40.8/54.3   |         42.6/25.3/46.3/55.2          | **70**      | [link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00fb89809151993e92828142491284ce01645a1cd3d43b38f47a0a73894aefd9053660e6f4ee08f3c955e99bfdb5846da0ada06c45242c9738a52641d67be1adb98 
| Mask R-CNN    | R-50-FPN   |    36 |   36.5/17.9/39.2/52.5|     40.5/24.7/43.7/52.2              | 77      | [link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00f23e30d9008ea4cc74d4acaa491a1d8c591f9def4b8d99ced55bb55fc3d9b58ee08e06386b328cd2730e9b792575960bbce531ee999f386d4e2d0d61779fa5b54 
| **CenterMask**    | R-50-FPN   |    36 | 37.0/17.6/39.7/53.8  |       41.7/24.8/45.1/54.5            | 72      | [link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00f532d6b4fe9f4d8c83b6c8e72b81754b765a4de3029c61197398ea8656feda6a96d2f3b2ca1cbea6d869be7f8f6e5f5a24552a21fd496e213151f5bf77b4b47c9 
| **CenterMask**    | **V2-39-FPN**   |    36 |  38.5/19.0/41.5/54.7 |      43.5/27.1/46.9/55.9           | **70**      | [link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00f561c2331d24bc19343931450dee10ad46bb83cff70e7ef7a573189655fb801522a3d289a3d6b2e5f48cbe16d4bcd30978eac780f2e093e6de8e904f861ff0e80 
||
| Mask R-CNN    | R-101-FPN   |    24 |  37.8/18.5/40.7/54.9  |         42.2/25.8/45.8/54.0          | 94      | [link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00f8a9d63414f523c8c783267980644aa36798fc12ab63534af0e9d5f2d3b98c567a1079c4d7a1aaa5e7f9801bb2a84213c249e039447b6a73204f583c8c0bfab03 
| **CenterMask**    | R-101-FPN   |    24 | 38.0/18.2/41.3/55.2  |       43.1/25.7/47.0/55.6            | 91      | [link](http://u.720life.cn/g/34b4ecd80399a6e34dfced8e4f014f167a8ebc2a440553dc718da98a668b6a2f58776ceb62ec1a00f8921da5a876884c393bfb6318bf2239fbe6f7dfcdcd9ca8bf11f8870f5328f8792e80d7e552d1c6 
| **CenterMask**    | **V2-57-FPN**   |    24 | 38.5/18.6/41.9/56.2  |      43.8/26.7/47.4/57.1             | **76**      | [link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00f00bd7a9b2b0aec09d0df52c6307e9add0a7dcc59e4c655b4514757dfb153dedabf51a1de35eb39dfc6a00c26f0b4defb8308352cd1cb919e3223cd0e1eec110c 
| Mask R-CNN    | R-101-FPN   |    36 | 38.0/18.4/40.8/55.2  |      42.4/25.4/45.5/55.2             |   94    | [link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00f4efe6f22fc9f93580284f6d2f42e26e41d9e9ba44324b8c82ecbe61e3ae43974ef8a3d167e926d8302883c9d3578d95e7a99de18923155d0c12abeae0a7bddbe 
| **CenterMask**    | R-101-FPN   |    36 | 38.6/19.2/42.0/56.1 |   43.7/27.2/47.6/56.7    | 91      | [link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00fb2ad56d4e8dd56e401037235242d0195350364934df32048b2188f6de549d26271f8af21db1af2a533afc6379456598bec4f680b1af6c4fc96bd2ad9ac7c1dc0 
| **CenterMask**    | **V2-57-FPN**   |    36 |   39.4/19.6/42.9/55.9  |      44.6/27.7/48.3/57.3 | **76**      | [link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00f91003ba4de6d86eb64358108895bbd1e5dff237b98d959512af4af47e935f5cba3c746f304768d257cf8063126e3da219093ebe24559acef277b3b90fc4c3753 
||
| Mask R-CNN    | X-101-32x8d-FPN   |    24 |   38.9/19.6/41.6/55.7    |   43.7/27.6/46.9/55.9       |   165    | [link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00fa60b690c0fdd53aa969e4b712f08b70b2dcc0087897573cee0b83c85e54b8a1534338210fede2ac3d7f39196d907c77ed32370a9b651f55a2bcc43f6bb4f2f9d 
| **CenterMask**    | X-101-32x8d-FPN  |    24 | 39.1/19.6/42.5/56.1  |        44.3/26.9/48.5/57.0      | 157      | [link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00fc8714dad34b106b87bbd5a1b6337c2c16e40b2dfc4a2d4726afd174fc99208bb3f5b9a03c44b8c1ff7d847c33ea6a84a4d6574a65aa3c4c6ed294b34661f7fd8 
| **CenterMask**    | **V2-99-FPN**   |    24 | 39.6/19.6/43.1/56.9  |      44.8/27.6/49.0/57.7        |  **106**     | [link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00f82b15da4f1d93131ca51d7e16bf26a5f8d93b91d1d882501193ae1dafcac6cf7c94a319e28da768525193df19658bdd31dd1ae5aeb0effb990b9999ffd181ef6 
| Mask R-CNN    | X-101-32x8d-FPN   |    36 | 38.6/19.7/41.1/55.2  |    43.6/27.3/46.7/55.6          |   165    | [link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00fe1836bb0349e57eee191b83bcc299af561f760be4c57578042633cbace1a1baae6efb483efe67f22dd8ec538ae891e0235ca9714b266fff77deee7daa60cd6ea 
| **CenterMask**    |X-101-32x8d-FPN   |    36 | 39.1/18.5/42.3/56.4  |     44.4/26.7/47.7/57.1         | 157      |[link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00f4adc90ef8239304fdabe2bf4bc3a9c362c6a032b3123e4face412902b1fc7723e0d3a7f532ad0ecf2806f4f67255e2c451e2b4577fba4f15ce03b2b533e6324a 
| **CenterMask**    | **V2-99-FPN**   |    36 | 40.2/20.6/43.5/57.3  |      45.6/29.2/49.3/58.8       | **106**      | [link](http://u.720life.cn/g/84e90b04f4f1039df6d6739ea9cbe00ff5451f98823bf2a957ffc42a92e4447d826e28061579479501ed23243d5e4c09fd74bcf108635c199351e2b09f9122bde45d2155ef40fe52ad8ac5e16f572bd6 

*Note that the all models are trained using **train-time augmentation (multi-scale)**.*\
*The inference time of all models is measured on **Titan Xp** GPU.*\
*24/36 epoch are same as x2/x3 training schedule in [detectron](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304697d9ece9d0ba791376c04b68e0cd9a5b9590140d252352a35ac202c5cf94ad3b  respectively.*


## Installation
Check [INSTALL.md](INSTALL.md) for installation instructions which is orginate from [maskrcnn-benchmark](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304697d9ece9d0ba791376c04b68e0cd9a5bc2f03f0f0b3f69be7bb7e1fe06be0d6a3e9e0b7f9bb39e18f204ee8b3abd6db3 

## Training
Follow [the instructions](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304697d9ece9d0ba791376c04b68e0cd9a5bc2f03f0f0b3f69be7bb7e1fe06be0d6ad89fa46f26c3bd0281ed6f4d8ceaf1081d0ccf31f39d91b0a58cfadedbbbc5e1)  of  [maskrcnn-benchmark](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304697d9ece9d0ba791376c04b68e0cd9a5bc2f03f0f0b3f69be7bb7e1fe06be0d6a97eccd6a9a977588887154b29137b070)  guides.

If you want multi-gpu (e.g.,8) training,

```bash
export NGPUS=8
python -m torch.distributed.launch --nproc_per_node=$NGPUS tools/train_net.py --config-file "configs/centermask/centermask_R_50_FPN_1x.yaml" 
```


## Evaluation

Follow [the instruction](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304697d9ece9d0ba791376c04b68e0cd9a5bc2f03f0f0b3f69be7bb7e1fe06be0d6a929e31ad2f50c4afebf4156e6bb1d0bd53e1bbf468c3aa5338c4b3d94190249d)  of [maskrcnn-benchmark](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304697d9ece9d0ba791376c04b68e0cd9a5bc2f03f0f0b3f69be7bb7e1fe06be0d6a97eccd6a9a977588887154b29137b070) 

First of all, you have to download the weight file you want to inference.

For examaple (CenterMask-Lite-R-50),
##### multi-gpu evaluation & test batch size 16,
```bash
wget https://www.dropbox.com/s/2enqxenccz4xy6l/centermask-lite-R-50-ms-bs32-1x.pth
export NGPUS=8
python -m torch.distributed.launch --nproc_per_node=$NGPUS tools/test_net.py --config-file "configs/centermask/centermask_R_50_FPN_lite_res600_ms_bs32_1x.yaml"   TEST.IMS_PER_BATCH 16 MODEL.WEIGHT centermask-lite-R-50-ms-bs32-1x.pth
```

##### For single-gpu evaluation & test batch size 1,
```bash
wget https://www.dropbox.com/s/2enqxenccz4xy6l/centermask-lite-R-50-ms-bs32-1x.pth
CUDA_VISIBLE_DEVICES=0
python tools/test_net.py --config-file "configs/centermask/centermask_R_50_FPN_lite_res600_ms_bs32_1x.yaml" TEST.IMS_PER_BATCH 1 MODEL.WEIGHT centermask-lite-R-50-ms-bs32-1x.pth
```


## TODO
 - [x] train-time augmentation + 3x schedule for comparing with detectron2 models
 - [x] ResNet-50 & ResNeXt-101-32x8d
 - [x] VoVNetV2 backbones
 - [x] VoVNetV2 backbones for [Detectron2](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a0e50a90cce0abf558678bb0e474dbaeaa002b601f0bcebdb6a5963c5103d1a7dcdc8c08615d2aa852b18e12f57146d92646d9b0335e4f29b648a7f48382de87) 
 - [x] CenterMask in [Detectron2](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a0e50a90cce0abf558678bb0e474dbaeaa002b601f0bcebdb6a5963c5103d1a7dcdc8c08615d2aa852b18e12f57146d92646d9b0335e4f29b648a7f48382de87) 
 - [ ] quick-demo
 - [ ] arxiv paper update




## Performance
![vizualization](figures/quality.png)
![results_table](figures/results.png)

## Citing CenterMask

Please cite our paper in your publications if it helps your research:

```BibTeX
@article{lee2019centermask,
  title={CenterMask: Real-Time Anchor-Free Instance Segmentation},
  author={Lee, Youngwan and Park, Jongyoul},
  booktitle={CVPR},
  year={2020}
} 
```



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)