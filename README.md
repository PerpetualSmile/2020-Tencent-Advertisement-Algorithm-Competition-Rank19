队伍：此心安处是吾乡

队员：[JackDong](<https://github.com/PerpetualSmile>)、[fengli](<https://github.com/fenglicui>)、[zhang](http://iip.nju.edu.cn/index.php/Yi_Zhang_@_IIP,_NJU-CS)

## 运行环境

- jupyter notebook
- gensim
- pytorch 1.5.1

## 代码和模型说明

- 本次比赛使用到的所有代码都写在jupyter notebook中了，解压完训练和测试数据之后，可以在TI-ONE平台上直接运行。运行顺序是按照notebook的命名编号从小到大依次运行。

- 各个notebook的输入、输出以及主要功能说明如下：

| notebook                               | 功能                           | 输入文件               | 输出文件             |
| -------------------------------------- | ------------------------------ | ---------------------- | -------------------- |
| 1_Preprocess_Data.ipynb                | 数据预处理                     | 原始训练数据和测试数据 | 预处理完的数据       |
| 2_Word_Embedding.ipynb                 | 生成Word Embedding             | 预处理完的数据         | embedding            |
| 3_LSTM_v1_win10_300size_1.4721.ipynb   | 搭建和训练模型，生成预测结结构 | embedding              | 用于后处理的预测结果 |
| 4_Attention_LSTM_v1_128_128_1470.ipynb | 搭建和训练模型，生成预测结结构 | embedding              | 用于后处理的预测结果 |
| 5_Process_Result                       | 结果后处理                     | 3和4生成的预测结果     | submission.csv       |



- 特征只使用了不同窗口大小和不同维度大小的word embedding，模型使用了双层BiLSTM
- 6和7的notebook里使用了Transformer的模型，但单模分数只有1.464，最终没有使用，放在这里仅供参考

- 最后一共为3和4版本的12个模型的融合，不同的参数设置都已经写在每个notebook中了，每个notebook命名的最后分数代表单模五折的线上分数。

- 最后融合结果的B榜得分为1.478，最终排名TOP19。

