Machine Learning Notebooks
==========================

This project aims at teaching you the fundamentals of Machine Learning in
python. It contains the example code and solutions to the exercises in the second edition of my O'Reilly book [Hands-on Machine Learning with Scikit-Learn, Keras and TensorFlow](http://u.720life.cn/g/76e0e2628032bcb7046a7a41709981211b2671affcecfc971893866755841ab05172eb3b24b7ac737cfdce71aaa9942510809c9e903ca054015dfc0554ce40667ac301e0af4c94a18654840788ef2411 

 

**Note**: If you are looking for the first edition notebooks, check out [ageron/handson-ml](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304698b55a15d2d9661f79af84ed9f623f957f9de3de4e5b5ff38c0a4253f4d5da03 

## Quick Start

### Want to play with these notebooks online without having to install anything?
Use any of the following services.

**WARNING**: Please be aware that these services provide temporary environments: anything you do will be deleted after a while, so make sure you download any data you care about.

* **Recommended**: open this repository in [Colaboratory](http://u.720life.cn/g/0f77d744095a1b5116b170278fdae062e03aae381068bd64aa436fb90b6db114599e0f78c770370ce4921ed19bf22b5d76dccf8dc2bd04840521828aa928a8cf55d4b630b25158c76e84d860c62f6605 
   

* Or open it in [Binder](http://u.720life.cn/g/229dec2b58c85dece66cc933170f8f995fb66a6518a4db9cc440dbd95bcde1bf752e6b7b9f2f41b765a2fc1357eafa5504e4c1121aa75e6c3331f2de0e365a94 
   

  * _Note_: Most of the time, Binder starts up quickly and works great, but when handson-ml2 is updated, Binder creates a new environment from scratch, and this can take quite some time.

* Or open it in [Deepnote](http://u.720life.cn/g/1664bc7d0285e5a13128558614fb8d5c27d6ff2c5e22eca232437660286407c1ad37d7f0841c1225c5cb6e63dd3d3015c7028b2b85bfbd3d023cd125390c00c427fcea1c11d3b78b7e6f994a608e23f06c3e0c50a509582d636a261b8ba4f6327ff88fae901e9d6707a32f79435589579867ccba411ec9e621942f5729b635fd 
   

### Just want to quickly look at some notebooks, without executing any code?

Browse this repository using [jupyter.org's notebook viewer](http://u.720life.cn/g/fdd36b5587a2cfb4c93a3788524fb8a41956df75d2b9251c9c51d6e2391efdf8134e796d66c8b7a793896b33f80f5a521a998ae20a31fb3927b8daae0f134d676e32594ced34a98aabacb95abeb647c8 
   

_Note_: [github.com's notebook viewer](index.ipynb) also works but it is slower and the math equations are not always displayed correctly.

### Want to run this project using a Docker image?
Read the [Docker instructions](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304698b55a15d2d9661f79af84ed9f623f9576d441db3b83c5e0d64b253ea777c62b493d0f724c657c08ab6ed555a436f72a 

### Want to install this project on your own machine?

Start by installing [Anaconda](http://u.720life.cn/g/8665655309c37f79878334c98bb1f36df2d1dd343638933e9f10ae13354950b3300a9154c7e16ea5769add7abbe38f8d)  (or [Miniconda](http://u.720life.cn/g/0e4e307b9ffc559a03b58a8d1764d889804b1a5ec5f8f53b3fbaee33dd0b98f1073cddf95cb0cc4bfe7dae1c8220080a6e182f4820a8661d96b33ff8bddddf2d  [git](http://u.720life.cn/g/0699e533b96232c5e210af6ab5668134d8ef8f2b48a28e22926fb846669cf5b8  and if you have a TensorFlow-compatible GPU, install the [GPU driver](http://u.720life.cn/g/b63b7eeca5227f5a2e44bcc992111018ef4c5127fa2f52132b9f0dfbba744eee74477c8a2b9dec73c7accb9cb3224241 

Next, clone this project by opening a terminal and typing the following commands (do not type the first `$` signs on each line, they just indicate that these are terminal commands):

    $ git clone https://github.com/ageron/handson-ml2.git
    $ cd handson-ml2

If you want to use a GPU, then edit `environment.yml` (or `environment-windows.yml` on Windows) and replace `tensorflow=2.0.0` with `tensorflow-gpu=2.0.0`. Also replace `tensorflow-serving-api==2.0.0` with `tensorflow-serving-api-gpu==2.0.0`.

Next, run the following commands:

    $ conda env create -f environment.yml # or environment-windows.yml on Windows
    $ conda activate tf2
    $ python -m ipykernel install --user --name=python3

Then if you're on Windows, run the following command:

    $ pip install --no-index -f https://github.com/Kojoley/atari-py/releases atari_py

Finally, start Jupyter:

    $ jupyter notebook

If you need further instructions, read the [detailed installation instructions](INSTALL.md).

## Contributors
I would like to thank everyone who contributed to this project, either by providing useful feedback, filing issues or submitting Pull Requests. Special thanks go to Haesun Park who helped on some of the exercise solutions, and to Steven Bunkley and Ziembla who created the `docker` directory.



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)