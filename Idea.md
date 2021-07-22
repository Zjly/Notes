# Idea

### 毕业论文内容

- API推荐 API查询问题->API序列
- 使用RNN encoder-decoder输入问题将其转化为序列
- 使用diverse beam search生成多样化的序列

### API推荐 序列多样性

使用多样beam search，API推荐结果Top-K的序列之间的多样性。

1. 会不会创新性不足？
   - 把DeepAPI的RNN encoder-decoder换成bert的Transformer
   - 使用别人提出的diverse beam search
   - 之外没有找到什么好的适合beam search的用于解决序列多样性的多样化方法

### API序列总体多样性 beam search 流行度偏差 使用GPT/BERT？

在API序列推荐当中，可以在beam search中可以考虑到整体的流行度偏差的问题，去推荐一些非热门的结果，增加推荐的多样性（整体多样性），推荐结果为Top-K的API序列。

1. 通过对每一个推荐结果增加一个权重来惩罚热门API的推荐
    - 在每一步中限制
    - 仅对序列的开头进行流行度限制
2. 保留一定的流行度偏差
    - 组与组之间限制序列多样性， 组内限制流行度
    
    - 组与组之间限制流行度， 组内限制序列多样性
    
3. 提出训练充分度对多样性的影响 在论文后面部分可以研究

### 低训练度模型 beam search 提高准确率

###### 可以作为论文的一部分

低训练度模型的表达能力不够，Top-K如果第一个不准后续就会也很不准。可以考虑到运用到beam search中一些被舍弃的结果来提高最后推荐的信息量，更能够命中真实的结果。

1. 考虑相似度，保留一些不太相似的序列
   - 训练完成后，分支之间相似度太高就舍弃，使用更靠后的序列
   - 在序列开头就进行度量，直接引导一条不同的序列

2. 用模型训练不同训练程度的模型的多样性参数
   - 输入模型 输出最优的多样性参数 可行性？
   - 或者是手动找

### Attention层来促进beam search多样化

- 在生成每个节点时，是否可以通过attention机制给每个word增加一个权重去得到多样化结果？
- 去注意前一个序列的结果
- 这个不知道有没有可行性
