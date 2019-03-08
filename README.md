### Bert 相关内容请参见https://github.com/google-research/bert
---
\*\*\* 2018/12/29 更新 \*\*\*

主要工作：下载cips-sogou 2018比赛提供的数据
使用事实类和非事实类数据集，将它们转换为SQuAD数据集的格式，基于bert模型的基础上进行测试。
测试结果：
- 模型：bert
- 训练集：cips-sogou unfactoid training set
- 测试集：cipos-sogou unfactoid eval set
- 实验结果：{"exact_match": 0.657786548265088, "f1": 0.8098938569053756}
- {"Total Cnt": 5000
   "average bleu-4": 0.4400
   "average rouge-l": 0.5106}
- 实验细节： 计算各个paragraph的最大start\_logits + end\_logits，取最大值对应的text
- 参数设置：
    - doc_stride = 256
    - max_seq_length = 512
    - max_answer_length = 256
    - n_best_size = 10

---
### 相关资料

#### 语言模型
- Deep contextualized word representations\[[paper](https://arxiv.org/pdf/1802.05365.pdf%C3%82)\]
- BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding\[[paper](https://arxiv.org/pdf/1810.04805.pdf)\]
- Improving Language Understanding by Generative Pre-Training\[[paper](https://s3-us-west-2.amazonaws.com/openai-assets/research-covers/language-unsupervised/language_understanding_paper.pdf)\]
- Language Models are unsupervised Multitask Learners\[[paper](https://d4mucfpksywv.cloudfront.net/better-language-models/language_models_are_unsupervised_multitask_learners.pdf)\]
- Attention Is All You Need\[[paper](https://papers.nips.cc/paper/7181-attention-is-all-you-need.pdf)\]
- Character-Aware Neural Language Models\[[paper](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.718.6564&rep=rep1&type=pdf)\]
- Transformer-XL: Attentive Language Models Beyond A Fixed-Length Context\[[paper](https://arxiv.org/pdf/1901.02860.pdf)\]

#### 问答/机器阅读理解
- Reading Wikipedia to Answer Open-Domain Questions\[[paper](https://arxiv.org/pdf/1704.00051.pdf)\]
- Qanet: Combining local convolution with global self-attention for reading comprehension \[[paper](https://arxiv.org/pdf/1804.09541.pdf)\]
- Bi_Directional Attention Flow for Machine Comprehension\[[paper](https://arxiv.org/pdf/1611.01603.pdf)\]
- Dynamic Co-Attention Networks for Question Answering\[[paper](https://arxiv.org/pdf/1611.01604.pdf)\]
- The Design and Implementation of XiaoIce, an Empathetic Social Chatbot\[[paper](https://arxiv.org/pdf/1812.08989.pdf)\]
- Neural Approaches to Conversational AI\[[paper](http://www.aclweb.org/anthology/P18-5002)\]

#### 多轮对话
- Towards End-to-End Reinforcement Learning of Dialogue Agents for Information Access\[[paper](https://arxiv.org/pdf/1609.00777.pdf)\]

#### 数据集
-
