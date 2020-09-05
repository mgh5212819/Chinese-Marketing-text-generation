# 文件介绍与运行说明

## Files

### data/
 data_utils.py: 用于数据处理的助手函数或类
 process.py: 将原始数据集处理为示例文件
 back_translate.py：将原始数据集翻译为英文并返回中文。
 embed_replace.py: 用嵌入空间（w2v）中类似的另一个字符替换tfidf得分低的字符。
 semi-supervise.py: 使用半监督学习从现有参考生成新的源。

### model/
 config.py: 定义配置参数
 dataset.py: 定义模型中使用的样本格式
 evaluate.py: 评估测试集的损失
 model.py: 定义模型
 predict.py: 生成摘要
 rouge_eval.py: 用ROUGE评分评价模型.
 train.py: 训练模型.
 utils.py: 用于模型的助手函数或类.
 vocal.py: 定义Vocab对象.



## 实验效果

模型     | ROUGE1 | ROUGE2 |ROUGEL
-------- | ----- | ------ | ------
seqseq+att |0.230632 |0.0407 | 0.13037
PGN  | 0.24565 | 0.042663| 0.154976
PGN+converage  | **0.267554** | 0.04647| 0.162138
PGN+weight_tying | 0.248096 | 0.04334|0.15791
PGN+big_samples| 0.25631 | **0.04995**| **0.16245**