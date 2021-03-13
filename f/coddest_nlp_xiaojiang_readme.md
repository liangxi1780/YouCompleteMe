# nlp_xiaojiang


# AugmentText
    - 回译（效果比较好）
    - EDA（同义词替换、插入、交换和删除）（效果还行）
    - HMM-marko（质量较差）
    - syntax（依存句法、句法、语法书）（简单句还可）
    - seq2seq（深度学习同义句生成，效果不理想，seq2seq代码大都是 [https://github.com/qhduan/just_another_seq2seq] 的，效果不理想）
    
# ChatBot
    - 检索式ChatBot
        - 像ES那样直接检索(如使用fuzzywuzzy)，只能字面匹配
        - 构造句向量，检索问答库，能够检索有同义词的句子
    - 生成式ChatBot（todo）
        - seq2seq
        - GAN

# ClassificationText
    - bert+bi-lstm(keras) approach 0.78~0.79% acc of weBank Intelligent Customer Service Question Matching Competition
    - bert + text-cnn(keras) approach 0.78~0.79% acc of weBank Intelligent Customer Service Question Matching Competition
    - bert + r-cnn(keras) approach 0.78~0.79% acc of weBank Intelligent Customer Service Question Matching Competition
    - bert + avt-cnn(keras) approach 0.78~0.79% acc of weBank Intelligent Customer Service Question Matching Competition

# Ner
    - bert命名实体提取(bert12层embedding + bilstm + crf)
        - args.py(配置一些参数)
        - keras_bert_embedding.py(bert embedding)
        - keras_bert_layer.py(layer层, 主要有CRF和NonMaskingLayer)
        - keras_bert_ner_bi_lstm.py(主函数, 定义模型、数据预处理和训练预测等)
        - layer_crf_bojone.py(CRF层, 未使用)

# FeatureProject
    - bert句向量、文本相似度
        - bert/extract_keras_bert_feature.py:提取bert句向量特征
        - bert/tet_bert_keras_sim.py:测试xlnet句向量cosin相似度
    - xlnet句向量、文本相似度
        - xlnet/extract_keras_xlnet_feature.py:提取bert句向量特征
        - xlnet/tet_xlnet_keras_sim.py:测试bert句向量cosin相似度
    - normalization_util指的是数据归一化
        - 0-1归一化处理
        - 均值归一化
        - sig归一化处理
    - sim feature（ML）
        - distance_text_or_vec:各种计算文本、向量距离等
        - distance_vec_TS_SS：TS_SS计算词向量距离
        - cut_td_idf：将小黄鸡语料和gossip结合
        - sentence_sim_feature：计算两个文本的相似度或者距离，例如qq（问题和问题），或者qa（问题和答案）

# run(可以在win10下,pycharm下运行)
  - 1.创建tf-idf文件等（运行2需要先跑1）:      
                                       ```
                                       python cut_td_idf.py
                                       ```
  - 2.计算两个句子间的各种相似度，先计算一个预定义的，然后可输入自定义的（先跑1）:  
                                       ```
                                       python sentence_sim_feature.py
                                       ```
  - 3.chatbot_1跑起来(fuzzy检索-没)（独立）：    
                                       ```
                                       python chatbot_fuzzy.py
                                       ```
  - 4.chatbot_2跑起来(句向量检索-词)（独立）：    
                                       ```
                                       python chatbot_sentence_vec_by_word.py
                                       ```
  - 5.chatbot_3跑起来(句向量检索-字)（独立）：    
                                       ```
                                       python chatbot_sentence_vec_by_char.py
                                       ```
  - 6.数据增强（eda)：                     python enhance_eda.py
  - 7.数据增强（marko）:                   python enhance_marko.py
  - 8.数据增强（translate_account）:       python translate_tencent_secret.py
  - 9.数据增强（translate_tools）:         python translate_translate.py
  - 10.数据增强（translate_web）:          python translate_google.py
  - 11.数据增强（augment_seq2seq）:        先跑 python extract_char_webank.py生成数据，
                                          再跑 python train_char_anti.py
                                          然后跑 python predict_char_anti.py
  - 12.特征计算(bert)（提取特征、计算相似度）: 
                      ```
                      run extract_keras_bert_feature.py
                      run tet_bert_keras_sim.py
                      ```
                      
# Data
    - chinese_L-12_H-768_A-12（谷歌预训练好的模型）
       github项目中只是上传部分数据，需要的前往链接: https://pan.baidu.com/s/1I3vydhmFEQ9nuPG2fDou8Q 提取码: rket
       解压后就可以啦
    - chinese_xlnet_mid_L-24_H-768_A-12(哈工大训练的中文xlnet, mid, 24层, wiki语料+通用语料)
        - 下载地址[https://github.com/ymcui/Chinese-PreTrained-XLNet](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046237d6264b170e9e9d8eb0bc98a8d058e826963d7ee4e793d104917ad99cda2f83168dfb3c467978ed04df7e4f61800e7) 
    - chinese_vector
        github项目中只是上传部分数据，需要的前往链接: https://pan.baidu.com/s/1I3vydhmFEQ9nuPG2fDou8Q 提取码: rket
        - 截取的部分word2vec训练词向量（自己需要下载全效果才会好）
        - w2v_model_wiki_char.vec、w2v_model_wiki_word.vec都只有部分
    - corpus
        github项目中只是上传部分数据，需要的前往链接: https://pan.baidu.com/s/1I3vydhmFEQ9nuPG2fDou8Q 提取码: rket
        - ner(train、dev、test----人民日报语料)
        - webank(train、dev、test)
        - 小黄鸡和gossip问答预料（数据没清洗）,chicken_and_gossip.txt
        - 微众银行和支付宝文本相似度竞赛数据， sim_webank.csv
    - sentence_vec_encode_char
        - 1.txt（字向量生成的前100000句向量）
    - sentence_vec_encode_word
        - 1.txt（词向量生成的前100000句向量）
    - tf_idf（chicken_and_gossip.txt生成的tf-idf）
    
# requestments.txt
    - python_Levenshtei
        - 调用Levenshtein，我的python是3.6，
        - 打开其源文件: https://www.lfd.uci.edu/~gohlke/pythonlibs/
        - 查找python_Levenshtein-0.12.0-cp36-cp36m-win_amd64.whl下载即可
    - pyemd
    - pyhanlp
        - 下好依赖JPype1-0.6.3-cp36-cp36m-win_amd64.whl
  
# 参考/感谢
* eda_chinese：[https://github.com/zhanlaoban/eda_nlp_for_Chinese](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467a803c6be88034879f7b89d96a74a2752a6b6d0d78093333755cb8f372137a45252a4e32f3d7c2c0498ccff77d9c107e) 
* 主谓宾提取器：[https://github.com/hankcs/MainPartExtractor](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304646eac928f5dd2516037f8f59026ba9fbc0c796e528bc9567bcf10ede18d9f163) 
* HMM生成句子：[https://github.com/takeToDreamLand/SentenceGenerate_byMarkov](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046027f29a86036ae91879dcb9e039e520a87bfb80ddc021a0bcad57ff83aad9a8c5ed122f7bb3e0de53ed2ff57184fc68a) 
* 同义词等：[https://github.com/fighting41love/funNLP/tree/master/data/](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046eb33aab946c49508b86101a0c1ed815eaeefa7c75d56e72274e5e98424edcbfdf4a1e6aaf275a9511a5fc5e5481aed13) 
* 小牛翻译：[http://www.niutrans.com/index.html](http://u.720life.cn/g/032ed7136028703548c53f9e9e6de9486064a1b2ab8756435ffc821f13beef036ac928411b6248807edbc5a962961cee) 
    
# 其他资料
* bert(keras):[https://github.com/CyberZHG/keras-bert](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ec8a60c627aa2d3068593691f80d471a35b88cf7110c1bbe00b01f79d55dd788) 
* NLP数据增强汇总:[https://github.com/quincyliang/nlp-data-augmentation](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466f0bcbaeba3664594eb1c6a0ab78e6c595498b6c9ca2cb29d7b6d1759eead610e8197388268cb5291983a4e0a5d4d0b4) 
* 知乎NLP数据增强话题:[https://www.zhihu.com/question/305256736/answer/550873100](http://u.720life.cn/g/97510b34ada15ed1c53e08f5d6d5775f16b6c04fd0aed95e6893479d5b96b5b1b9c0cff03d7d602a4efff6fc561d9d1aac7f7f0bd6b6f9300fca24c85785f1d3) 
* chatbot_seq2seq_seqGan（比较好用）：[https://github.com/qhduan/just_another_seq2seq](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a0db01ee8775106726f8df498eefb8f3fc2a2f4ea782c0538928118b5ac13c09) 
* 自己动手做聊天机器人教程: [https://github.com/warmheartli/ChatBotCourse](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046058f1f10097ef442298a97ffdea75043f0efa4f765d6ee2b8d3aa83f6e863c85) 




 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)