# Siamese Neural Networks
### A Siamese Network consists of two identical networks accepting different inputs and having bound weights to ensure that similar images are mapped close in the feature space
---
# Triplet Networks
### The model is composed of three identical networks, having shared parameters, which are trained by triplets composed of anchor, positive and negative samples
***DTNet: two triplet networks for learning visual-semantic mapping: one focuses on negative attribute features, and the other on the negative visual features***

---
# Matching Networks
### 对 support 集中所有样本的标签按相似度加权求和，从而得到 query 的类别概率分布