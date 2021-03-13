# Sentiment Analysis with LSTMs

This repository contains the iPython notebook and training data to accompany the [O'Reilly tutorial](http://u.720life.cn/g/76e0e2628032bcb7046a7a4170998121b5f0e8e97106b882dbff44998badcdc89eb9b92f83e18a96ed37729d016fdd39ad40092edf24953cd18c0bae50621ff2f6d6bc6255fd4bf54eab11d140d605a28f61cb98de42a750a22e6d4472fe1f3a)  on sentiment analysis with LSTMs in Tensorflow. See the original tutorial to run this code in a pre-built environment on O'Reilly's servers with cell-by-cell guidance, or run these files on your own machine. There is also another file called `Pre-Trained LSTM.ipynb` which allows you to input your own text, and see the output of the trained network.

## Downloading Data
Before running the notebook, you'll first need to download all data we'll be using. This data is located in the `models.tar.gz` and `training_data.tar.gz` tarballs. We will extract these into the same directory as `Oriole LSTM.ipynb`. As always, the first step is to clone the repository.
   ```bash
   git clone https://github.com/adeshpande3/LSTM-Sentiment-Analysis.git
   ```
Next, we will navigate to the newly created directory and run the following commands.
   ```bash
   tar -xvzf models.tar.gz
   tar -xvzf training_data.tar.gz
   ```

## Requirements and Installation
In order to run [the iPython notebook](Oriole-LSTM.ipynb), you'll need the following libraries.

* **[TensorFlow](http://u.720life.cn/g/de14350178d8232a6828b0e4db6a4d7b3a463afa36e104bb124a0e723d8be729b986bfa050d46eb6d3abfe4ac2f9f10e)  version 1.1 (See below for later versions)**
* [NumPy](http://u.720life.cn/g/9a4c6629f982e64f1eccb20230048513b840e2231ebe822675ff7076cc4d24373e62cbe011385663edf9b2a696a99299ee058aa61b296afa00652b6ae0fd3bd4) 
* [Jupyter](http://u.720life.cn/g/c3362d07b7a78eee8caea376f68778a34db28b9cdc0ba47ab1d7c68fd72beeb4f6a576db4cef869e1d9b4d2777fa207394f4ed3fae786ac0046f03e5dd6f1dba) 
* [matplotlib](http://u.720life.cn/g/45ed8da52b23a4eb3078a6b2c05ed12492ee5911531aba8c7d5dec11af0657ae) 

### TensorFlow 1.2 and later

In order to load the models without errors you need to convert the checkpoints using the converter provided by TensorFlow:

```bash
wget https://raw.githubusercontent.com/tensorflow/tensorflow/master/tensorflow/contrib/rnn/python/tools/checkpoint_convert.py
python checkpoint_convert.py models/pretrained_lstm.ckpt-90000 converted-checkpoints/pretrained_lstm-90000.ckpt
```
You should also replace the original models folder if you don't want to modify the code:
```bash
rm -rf models
mv converted-checkpoints models
```

### Docker
With Docker, you could just mount the repository and exec it.

1. Install Docker. Follow the [docker guide](http://u.720life.cn/g/fe36d46bcf13791bdad89a5e154210d9d1144e1d5c1c3fe1ef8b676ac5be40cf904668903e2327a7a47e54188b9618076421bfa8ca7dca5cfe21c556a52f7dae5d8d546be88706cb1dd68cb2b82d7e62 

2. Build docker image
    ``` bash
    cd LSTM-Sentiment-Analysis
    docker build -t="@yourname/tensorflow_1.1.0_py3" .
    ```

3. Run the container from the image
    ``` bash
    docker run -p 8888:8888 --name=tensorflow_yourname_py3 -v /@YourDir/LSTM-Sentiment-Analysis:/LSTM-Sentiment-Analysis -it @yourname/tensorflow_1.1.0_py3
    ```
    and visit the URL(http://u.720life.cn/g/e71094f6077cb9592da5b56893f0ad14e1ee284d7dd64df76b158f686d8712dd) 

4. Stop and restart the container
    ``` bash
    docker stop tensorflow_yourname_py3
    docker start tensorflow_yourname_py3
    docker attach tensorflow_yourname_py3
    ```

    If jupyter is down, relaunch it by using the command below.
    ``` bash
    cd LSTM-Sentiment-Analysis
    jupyter notebook --ip=0.0.0.0 --allow-root
    ```

### Installing Anaconda Python and TensorFlow
The easiest way to install TensorFlow as well as NumPy, Jupyter, and matplotlib is to start with the Anaconda Python distribution.

1. Follow the [installation instructions for Anaconda Python](http://u.720life.cn/g/d33365b902f7555c1a841a89dbf0471ec9b36f1efd95cf72678f407cac2341f4b63f837d7a75b1852b77ec6a0ad475ae  **We recommend using Python 3.6.**

2. Follow the platform-specific [TensorFlow installation instructions](http://u.720life.cn/g/de14350178d8232a6828b0e4db6a4d7b3a463afa36e104bb124a0e723d8be7292b3faa330cdb1a6840ecf5f68093f78c  Be sure to follow the "Installing with Anaconda" process, and create a Conda environment named `tensorflow`.

3. If you aren't still inside your Conda TensorFlow environment, enter it by opening your terminal and typing
    ```bash
    source activate tensorflow
    ```

4. If you haven't done so already, download and unzip [this entire repository from GitHub](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304620537d060a64a417d2947c0b464ac612caa07c5032e3527b41f75a4bf7a2ba08b94574d0607f290a0fd8e12dd0793f1b  either interactively, or by entering
    ```bash
    git clone https://github.com/adeshpande3/LSTM-Sentiment-Analysis
    ```

5. Use `cd` to navigate into the top directory of the repo on your machine

6. Launch Jupyter by entering
    ```bash
    jupyter notebook
    ```
    and, using your browser, navigate to the URL shown in the terminal output (usually http://localhost:8888/)



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)