 
   
 

**`Documentation`** |
------------------- |
[![Documentation](https://img.shields.io/badge/api-reference-blue.svg)](https://www.tensorflow.org/api_docs/) |

[TensorFlow](http://u.720life.cn/g/de14350178d8232a6828b0e4db6a4d7b53fae64cc9d0d2b052b654c5bd21da24)  is an end-to-end open source platform
for machine learning. It has a comprehensive, flexible ecosystem of
[tools](http://u.720life.cn/g/de14350178d8232a6828b0e4db6a4d7ba72e98f324db1003c2ade1e3ad35a5657f9b074c458374c019fdce42200dc60e 
[libraries](http://u.720life.cn/g/de14350178d8232a6828b0e4db6a4d7ba72e98f324db1003c2ade1e3ad35a5656abb335c02d9cebe02e88c57497003ed28101ad95f0c346f2723222b09187804  and
[community](http://u.720life.cn/g/de14350178d8232a6828b0e4db6a4d7b87f646000f92fd61f8deadd29d13fdf87072f8e17d895c444527c7d222713f72)  resources that lets
researchers push the state-of-the-art in ML and developers easily build and
deploy ML-powered applications.

TensorFlow was originally developed by researchers and engineers working on the
Google Brain team within Google's Machine Intelligence Research organization to
conduct machine learning and deep neural networks research. The system is
general enough to be applicable in a wide variety of other domains, as well.

TensorFlow provides stable [Python](http://u.720life.cn/g/de14350178d8232a6828b0e4db6a4d7bd42b497a8a2dffc720caa51cef7ce07a367b310f3980c21d924b23f98473a146) 
and [C++](http://u.720life.cn/g/de14350178d8232a6828b0e4db6a4d7bd42b497a8a2dffc720caa51cef7ce07a952081e73f7eaa5014301185061a7c13)  APIs, as well as
non-guaranteed backward compatible API for
[other languages](http://u.720life.cn/g/de14350178d8232a6828b0e4db6a4d7bd42b497a8a2dffc720caa51cef7ce07af64d7ac1601a879ca78cdc192904cbb9 

Keep up-to-date with release announcements and security updates by subscribing
to
[announce@tensorflow.org](http://u.720life.cn/g/941693b557d072bb769494a6a61fcd97f556421062bed7fcd8b7003c725011a0206239d0c1ec1b29f47f07c010eaa4597b792b289ac3cda8af53e3aa9608b18cd8c5fc304efa467cd8ec902dd07ab7bc 
See all the [mailing lists](http://u.720life.cn/g/de14350178d8232a6828b0e4db6a4d7b87f646000f92fd61f8deadd29d13fdf8ce1f3fd92d2614c075be5623bb0c77d1 

## Feature Prioritization Survey

The TensorFlow team is working on building/improving features, and understands
that it is very important to prioritize these efforts based on what TF users
need.

The goal of this short,  >> import tensorflow as tf
>>> tf.add(1, 2).numpy()
3
>>> hello = tf.constant('Hello, TensorFlow!')
>>> hello.numpy()
'Hello, TensorFlow!'
```

For more examples, see the
[TensorFlow tutorials](http://u.720life.cn/g/de14350178d8232a6828b0e4db6a4d7befb8841595000e17c544a9b7303f9ffec3b5c1cbe752ad556f6d4b75f9c0c68f 

## Contribution guidelines

**If you want to contribute to TensorFlow, be sure to review the
[contribution guidelines](CONTRIBUTING.md). This project adheres to TensorFlow's
[code of conduct](CODE_OF_CONDUCT.md). By participating, you are expected to
uphold this code.**

**We use [GitHub issues](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046522d1d8bb7c04f5a31a717fad17fa39813da1404c623665fcf1c132279791faa)  for
tracking requests and bugs, please see
[TensorFlow Discuss](http://u.720life.cn/g/941693b557d072bb769494a6a61fcd97f556421062bed7fcd8b7003c725011a0206239d0c1ec1b29f47f07c010eaa4591ef97b448cbf231f09a50ca98121576f) 
for general questions and discussion, and please direct specific questions to
[Stack Overflow](http://u.720life.cn/g/87bbd50441ad714fa4b3a92b06a39057c99d561856c3866c7b363085c26fdd7b9e3249bb493b588deb2c18945d53d031f01ae7a7adf646ddf8b8efe5c6b5680f 

The TensorFlow project strives to abide by generally accepted best practices in
open-source software development:

[![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/1486/badge)](https://bestpractices.coreinfrastructure.org/projects/1486)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-v1.4%20adopted-ff69b4.svg)](CODE_OF_CONDUCT.md)

## Continuous build status

### Official Builds

Build Type               | Status                                                                                                                                                                                                                                                                                                                                        | Artifacts
------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------
**Linux CPU**            | [![Status](https://storage.googleapis.com/tensorflow-kokoro-build-badges/ubuntu-cc.svg)](https://storage.googleapis.com/tensorflow-kokoro-build-badges/ubuntu-cc.html)                                                                                                                                                                        | [PyPI](https://pypi.org/project/tf-nightly/)
**Linux GPU**            | [![Status](https://storage.googleapis.com/tensorflow-kokoro-build-badges/ubuntu-gpu-py3.svg)](https://storage.googleapis.com/tensorflow-kokoro-build-badges/ubuntu-gpu-py3.html)                                                                                                                                                              | [PyPI](https://pypi.org/project/tf-nightly-gpu/)
**Linux XLA**            | [![Status](https://storage.googleapis.com/tensorflow-kokoro-build-badges/ubuntu-xla.svg)](https://storage.googleapis.com/tensorflow-kokoro-build-badges/ubuntu-xla.html)                                                                                                                                                                      | TBA
**macOS**                | [![Status](https://storage.googleapis.com/tensorflow-kokoro-build-badges/macos-py2-cc.svg)](https://storage.googleapis.com/tensorflow-kokoro-build-badges/macos-py2-cc.html)                                                                                                                                                                  | [PyPI](https://pypi.org/project/tf-nightly/)
**Windows CPU**          | [![Status](https://storage.googleapis.com/tensorflow-kokoro-build-badges/windows-cpu.svg)](https://storage.googleapis.com/tensorflow-kokoro-build-badges/windows-cpu.html)                                                                                                                                                                    | [PyPI](https://pypi.org/project/tf-nightly/)
**Windows GPU**          | [![Status](https://storage.googleapis.com/tensorflow-kokoro-build-badges/windows-gpu.svg)](https://storage.googleapis.com/tensorflow-kokoro-build-badges/windows-gpu.html)                                                                                                                                                                    | [PyPI](https://pypi.org/project/tf-nightly-gpu/)
**Android**              | [![Status](https://storage.googleapis.com/tensorflow-kokoro-build-badges/android.svg)](https://storage.googleapis.com/tensorflow-kokoro-build-badges/android.html)                                                                                                                                                                            | [![Download](https://api.bintray.com/packages/google/tensorflow/tensorflow/images/download.svg)](https://bintray.com/google/tensorflow/tensorflow/_latestVersion)
**Raspberry Pi 0 and 1** | [![Status](https://storage.googleapis.com/tensorflow-kokoro-build-badges/rpi01-py2.svg)](https://storage.googleapis.com/tensorflow-kokoro-build-badges/rpi01-py2.html) [![Status](https://storage.googleapis.com/tensorflow-kokoro-build-badges/rpi01-py3.svg)](https://storage.googleapis.com/tensorflow-kokoro-build-badges/rpi01-py3.html) | [Py2](https://storage.googleapis.com/tensorflow-nightly/tensorflow-1.10.0-cp27-none-linux_armv6l.whl) [Py3](https://storage.googleapis.com/tensorflow-nightly/tensorflow-1.10.0-cp34-none-linux_armv6l.whl)
**Raspberry Pi 2 and 3** | [![Status](https://storage.googleapis.com/tensorflow-kokoro-build-badges/rpi23-py2.svg)](https://storage.googleapis.com/tensorflow-kokoro-build-badges/rpi23-py2.html) [![Status](https://storage.googleapis.com/tensorflow-kokoro-build-badges/rpi23-py3.svg)](https://storage.googleapis.com/tensorflow-kokoro-build-badges/rpi23-py3.html) | [Py2](https://storage.googleapis.com/tensorflow-nightly/tensorflow-1.10.0-cp27-none-linux_armv7l.whl) [Py3](https://storage.googleapis.com/tensorflow-nightly/tensorflow-1.10.0-cp34-none-linux_armv7l.whl)

### Community Supported Builds

Build Type                                                        | Status                                                                                                                                                                                        | Artifacts
----------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------
**Linux AMD ROCm GPU** Nightly                                    | [![Build Status](http://ml-ci.amd.com:21096/job/tensorflow-rocm-nightly/badge/icon)](http://ml-ci.amd.com:21096/job/tensorflow-rocm-nightly)                                                  | [Nightly](http://ml-ci.amd.com:21096/job/tensorflow-rocm-nightly/lastSuccessfulBuild/)
**Linux AMD ROCm GPU** Stable Release                             | [![Build Status](http://ml-ci.amd.com:21096/job/tensorflow-rocm-release/badge/icon)](http://ml-ci.amd.com:21096/job/tensorflow-rocm-release/)                                                 | Release [1.15](http://ml-ci.amd.com:21096/job/tensorflow-rocm-release/lastSuccessfulBuild/) / [2.x](http://ml-ci.amd.com:21096/job/tensorflow-rocm-v2-release/lastSuccessfulBuild/)
**Linux s390x** Nightly                                           | [![Build Status](http://ibmz-ci.osuosl.org/job/TensorFlow_IBMZ_CI/badge/icon)](http://ibmz-ci.osuosl.org/job/TensorFlow_IBMZ_CI/)                                                             | [Nightly](http://ibmz-ci.osuosl.org/job/TensorFlow_IBMZ_CI/)
**Linux s390x CPU** Stable Release                                | [![Build Status](http://ibmz-ci.osuosl.org/job/TensorFlow_IBMZ_Release_Build/badge/icon)](https://ibmz-ci.osuosl.org/job/TensorFlow_IBMZ_Release_Build/)                                      | [Release](https://ibmz-ci.osuosl.org/job/TensorFlow_IBMZ_Release_Build/)
**Linux ppc64le CPU** Nightly                                     | [![Build Status](https://powerci.osuosl.org/job/TensorFlow_PPC64LE_CPU_Build/badge/icon)](https://powerci.osuosl.org/job/TensorFlow_PPC64LE_CPU_Build/)                                       | [Nightly](https://powerci.osuosl.org/job/TensorFlow_PPC64LE_CPU_Nightly_Artifact/)
**Linux ppc64le CPU** Stable Release                              | [![Build Status](https://powerci.osuosl.org/job/TensorFlow_PPC64LE_CPU_Release_Build/badge/icon)](https://powerci.osuosl.org/job/TensorFlow_PPC64LE_CPU_Release_Build/)                       | Release [1.15](https://powerci.osuosl.org/job/TensorFlow_PPC64LE_CPU_Release_Build/) / [2.x](https://powerci.osuosl.org/job/TensorFlow2_PPC64LE_CPU_Release_Build/)
**Linux ppc64le GPU** Nightly                                     | [![Build Status](https://powerci.osuosl.org/job/TensorFlow_PPC64LE_GPU_Build/badge/icon)](https://powerci.osuosl.org/job/TensorFlow_PPC64LE_GPU_Build/)                                       | [Nightly](https://powerci.osuosl.org/job/TensorFlow_PPC64LE_GPU_Nightly_Artifact/)
**Linux ppc64le GPU** Stable Release                              | [![Build Status](https://powerci.osuosl.org/job/TensorFlow_PPC64LE_GPU_Release_Build/badge/icon)](https://powerci.osuosl.org/job/TensorFlow_PPC64LE_GPU_Release_Build/)                       | Release [1.15](https://powerci.osuosl.org/job/TensorFlow_PPC64LE_GPU_Release_Build/) / [2.x](https://powerci.osuosl.org/job/TensorFlow2_PPC64LE_GPU_Release_Build/)
**Linux CPU with Intel® MKL-DNN** Nightly                         | [![Build Status](https://tensorflow-ci.intel.com/job/tensorflow-mkl-build-whl-nightly/badge/icon)](https://tensorflow-ci.intel.com/job/tensorflow-mkl-build-whl-nightly/)                     | [Nightly](https://tensorflow-ci.intel.com/job/tensorflow-mkl-build-whl-nightly/)
**Linux CPU with Intel® MKL-DNN** Stable Release                  | ![Build Status](https://tensorflow-ci.intel.com/job/tensorflow-mkl-build-release-whl/badge/icon)                                                                                              | Release [1.15](https://pypi.org/project/intel-tensorflow/1.15.0/) / [2.x](https://pypi.org/project/intel-tensorflow/)
**Red Hat® Enterprise Linux® 7.6 CPU & GPU**   Python 2.7, 3.6 | [![Build Status](https://jenkins-tensorflow.apps.ci.centos.org/buildStatus/icon?job=tensorflow-rhel7-3.6&build=2)](https://jenkins-tensorflow.apps.ci.centos.org/job/tensorflow-rhel7-3.6/2/) | [1.13.1 PyPI](https://tensorflow.pypi.thoth-station.ninja/index/)

## Resources

*   [TensorFlow.org](http://u.720life.cn/g/de14350178d8232a6828b0e4db6a4d7b7682acdb903d4a3e37e8d612836c7f8f) 
*   [TensorFlow tutorials](http://u.720life.cn/g/de14350178d8232a6828b0e4db6a4d7befb8841595000e17c544a9b7303f9ffef882a1ec1f94e22f8bc33f1574f48106) 
*   [TensorFlow official models](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461d663bc79af264d139e12fdb905edb0cd84a5a5e237639f31fe07659f29aad8fd07d803d1b63e1de424a7d37567dc842) 
*   [TensorFlow examples](http://u.720life.cn/g/54145d0471d91890860f7f8463c030468e565edc2ee8280fb354650bd76642c156e95eebc28d4c2c9a5d0f088abf3eb7) 
*   [TensorFlow in Practice from Coursera](http://u.720life.cn/g/bb1367b0c5f2568475c4f37831908c966a3ce8e976c5d89e13b2e93603a699cb0a71060568ff4ed238ab70daf0d27bb6f1d8fb781b8b671e92c1acf0def8e232) 
*   [Intro to TensorFlow for Deep Learning from Udacity](http://u.720life.cn/g/1af031bcb2b743cc087576e721b82699036ed4ab87d30a1d047aea8097d02188797b1a189d1c60c9e694aed564583fb196da21245b81acdbce9375175ad93c4afb4178aa4aa1fa1e168e483f821077fd) 
*   [Introduction to TensorFlow Lite from Udacity](http://u.720life.cn/g/1af031bcb2b743cc087576e721b82699036ed4ab87d30a1d047aea8097d02188797b1a189d1c60c9e694aed564583fb18cd8c80ab76e5ec4df6fb062ba5ae9e3) 
*   [TensorFlow blog](http://u.720life.cn/g/ee27a2253ab75a3a11810aac4d9aa1e72ba7a8e292fb414e5347cbb95c47f1a1) 
*   [TensorFlow Twitter](http://u.720life.cn/g/5ea88169c4a0fbd169233d52478d54fe7bd40b7458acafea518bf2e7905dc77c) 
*   [TensorFlow YouTube](http://u.720life.cn/g/2bc656cc69a0e9056dae2ced9f817b90e4824d906f042ec069e1bc943de38830353b9c5759ea26dd0e251f067cd12845206aa1d424107c76b88715ce4a7ed128) 
*   [TensorFlow roadmap](http://u.720life.cn/g/de14350178d8232a6828b0e4db6a4d7b87f646000f92fd61f8deadd29d13fdf807e439ca9d05aad2d048a08c0f389a8f) 
*   [TensorFlow white papers](http://u.720life.cn/g/de14350178d8232a6828b0e4db6a4d7b77da0ae8d55aee62f2ea1f573af961fccfb477d12c2a894e1075769a3ddcb6c6) 
*   [TensorBoard visualization toolkit](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046522d1d8bb7c04f5a31a717fad17fa39813bd654f8c26f68dea9f39a367c5da89) 

Learn more about the
[TensorFlow community](http://u.720life.cn/g/de14350178d8232a6828b0e4db6a4d7b87f646000f92fd61f8deadd29d13fdf87072f8e17d895c444527c7d222713f72)  and how to
[contribute](http://u.720life.cn/g/de14350178d8232a6828b0e4db6a4d7b87f646000f92fd61f8deadd29d13fdf8a8d47b1b489e108be0a14322ef91457dbbf35e1f2a529e1fe8b9f8eb2b3293c0 

## License

[Apache License 2.0](LICENSE)




 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)