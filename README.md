# 代码和模型说明

本次比赛使用到的代码都写在src目录下的jupyter notebook中了，解压完训练和测试数据之后，可以在TI-ONE平台上直接运行。运行顺序是按照notebook的命名编号从小到大依次运行。



| notebook                               | 功能                           | 输入文件               | 输出文件             |
| -------------------------------------- | ------------------------------ | ---------------------- | -------------------- |
| 1_Preprocess_Data.ipynb                | 数据预处理                     | 原始训练数据和测试数据 | 预处理完的数据       |
| 2_Word_Embedding.ipynb                 | 生成Word Embedding             | 预处理完的数据         | embedding            |
| 3_LSTM_v1_win10_300size_1.4721.ipynb   | 搭建和训练模型，生成预测结结构 | embedding              | 用于后处理的预测结果 |
| 4_Attention_LSTM_v1_128_128_1470.ipynb | 搭建和训练模型，生成预测结结构 | embedding              | 用于后处理的预测结果 |
| 5_Process_Result                       | 结果后处理                     | 3和4生成的预测结果     | submission.csv       |



最后一共为12个模型的融合，不同的参数设置都已经写在每个notebook中，每个notebook命名的最后分数代表单模五折的线上分数。notebook运行使用的虚拟环境为conda_pytorch_py3，需要注意将版本升级到pytorch1.5.1，其他环境都与TI-ONE的默认配置一样，可以直接运行复现结果。

