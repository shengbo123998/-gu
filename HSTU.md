受 Transformer 在语言与视觉领域取得成功的启发，作者重新审视了现代推荐系统中的基础设计选择。作者观察到，在处理亿级用户规模的推荐系统时，需克服三大挑战:

首先，推荐系统中的特征缺乏显式结构。尽管在小规模场景下已探索了序列化表达，但在工业级 DLRM 中，异质特征，如高基数 ID、交叉特征、计数器、比率等，扮演着关键角色。

其次，推荐系统采用的词表量达数十亿，且持续变化。与语言模型中使用的 10 万级静态词表相比，亿级动态词表带来了训练难题，并因需以 Target-aware 方式评估数万候选 Item，导致推理成本高昂。

最后，计算成本成为实现大规模序列模型的主要瓶颈。GPT-3 在数千块 GPU 上历经 1-2 个月，处理了总计 300B 个 Token。这一规模看似惊人，但与用户行为规模相比则相形见绌。最大的互联网平台每日服务数十亿活跃用户，这些用户每日与数十亿帖子、图片和视频互动。用户序列长度可达 10 的五次方。因此，推荐系统每日需处理的 Token 量，远超语言模型在 1-2 个月内处理的数量级。

<img width="562" height="166" alt="image" src="https://github.com/user-attachments/assets/88e3da1e-d6bd-4d29-bc00-f9a3ca560b39" />
<img width="1266" height="1466" alt="image" src="https://github.com/user-attachments/assets/26fcc6a4-2cc9-4eac-a83a-f6d08c4845ba" />
加了一个U()的gate，对最后的attention后的value做gate.


HLLM是late fusion，速度快，但是交互是在最后才交互。
<img width="2146" height="562" alt="image" src="https://github.com/user-attachments/assets/73a116ed-599a-4c9b-82a3-bcae2b69fd9a" />
M-FALCON: candidate跟序列一起作为输入，然后candidate用对角线的mask。


优化计算量： 1. 去掉FFN. 2.


#在rank任务上，输入可以做item-action交叉的形式。
#HSTU会用到user profile特征，但是不知道怎么用
