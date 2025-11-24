学习一个嵌入空间和距离度量，使得新任务只需在该空间中用少量 support 做最近邻/原型分类。
# Siamese Neural Networks
### A Siamese Network consists of two identical networks accepting different inputs and having bound weights to ensure that similar images are mapped close in the feature space
---
# Triplet Networks
### The model is composed of three identical networks, having shared parameters, which are trained by triplets composed of anchor, positive and negative samples
***DTNet: two triplet networks for learning visual-semantic mapping: one focuses on negative attribute features, and the other on the negative visual features***

---
# Matching Networks
### 对 support 集中所有样本的标签按相似度加权求和，从而得到 query 的类别概率分布

---
# Prototypical Networks
### 训练一个f,Given a class c, the prototypes are computed by averaging the embeddings of the support samples belonging to each class.用x作为f的输入,将结果与c的距离做softmax
### 在 ZSL 中，Prototypical Networks 不再依赖 support 图像来计算原型，而是直接将类别的语义向量（meta-data vector）通过一个 embedding 网络映射成原型。

---
# Relation Networks
### 训练一个 relation module，将 support 与 query 的特征图在通道维度拼接后输入该模块，由 relation module 输出相似度分数。相似度由网络学习而不是预定义距离。
