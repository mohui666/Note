通过学习生成同类的伪样本或伪特征来扩增支持集，从而直接缓解少样本带来的类内信息不足，实现对新任务的快速提升。
# Hallucinating with Intra-class Analogies
### 在meta-training时,联合训练hallucinator和classification algorithm,在meta-test时,用hallucinator生成fake support集合,和原集合并起来作为最终的support集