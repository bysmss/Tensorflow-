1## Tensorflow-

这是什么？
答 ： 一个聊天机器人。个人能力有限，暂且不能做到 ”智能“， 它好像自认为是女生，所以你大可调戏她，或是闲得无聊时候找它唠两句。

什么原理呢？
答： 严谨的说叫 ”基于深度学习的开放域生成对话模型“，框架为Keras（Tensorflow的高层包装），方案为主流的RNN（循环神经网络）的变种LSTM（长短期记忆网络）+seq2seq（序列到序列模型），外加算法Attention Mechanism（注意力机制），分词工具为jieba，UI为Tkinter，基于”青云“语料（10万+闲聊对话）训练。

”必要“是什么意思？
答：程序分为数据清洗，模型训练与模型预测三个部分，以及大量固化的二进制文件等。但你运行它只需要其中一小部分，包括预测程序、部分二进制文件和一个训练好的模型。

我该怎么运行它？
答： 因为没有打包exe，所以你直接运行main.py就好了。 python .\main.py

自己训练的话需要多久？
答：首先建议你有一张性能好的显卡。我在Google Colaboratory用GPU + 12GRAM（中途会爆内存1~2次）训练大概200个epoch，单次350s（不采用注意力机制的话为500s），中途大概两次降低学习率。

需要联网么？
答： 可以在联网状态下查某地天气，不过比较无脑（调用别人的api），所以我就去掉了。现在纯单机即可运行。

需要的运行环境是什么？
答：python3.6以上，Tensorflow（上面提到我用的keras了）。直接pip install tensorflow，不出意外的话是可以安装成功的。