# Notes for Happy LLM

## Chapter 1 NLP基础概念

### VSM (Vector Space Model)

制作词汇表，每个词对应一个one-hot向量，所以稀疏度很高

### N-gram
通过每个词在前面N-1个词出现时出现的条件概率，求平均，来估计整个句子的概率

### Word2Vec 

> 主要思想就是MLM

主要有两种架构：连续词袋模型CBOW(Continuous Bag of Words),
Skip-Gram模型
| 架构 | 训练时输入 | 训练时预测 |
|---|---|---|
| CBOW | “雍和宫、的、很、美” | “荷花” |
| Skip-Gram | “荷花” | 周围的“雍和宫、的、很、美” |

CBOW适用于小型数据集, 而Skip-Gram在大型语料中表现更好。

基于局部上下文的，无法捕捉到长距离的依赖关系，缺乏整体的词与词之间的关系

### ELMo
提取并组合预训练模型的表示

## Chapter 2 Transformer架构


