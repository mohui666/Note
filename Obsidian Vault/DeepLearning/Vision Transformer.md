Vision Tranformer提出了一种纯注意力机制的视觉深度学习方法 
**创新:
* 将二维图像通过可学习的embeddding layer转化为一维sequence,加上可学习的一维位置emdding编码
* 在seq的前面加入了可学习的\[class\]embedding patches
* 通过双线性插值在推理时适配不同的输入
**总结:
* 纯注意力的Inductive bias少于卷积层,使得基于注意力机制的模型可以更好的学到更通用的特征,便于模型的迁移,不过这样的代价是需要在大的数据集上进行pretrain
* Vision Transformer的自注意力机制使得在低层中也存在能注意全局的token
* Transformer架构使得模型可以用更少的计算资源实现和Conv相同的效果
* 迁移时,将后两个线性层换成一个以0初始化的线性层,比只换最后一层更好
* 自监督学习时,将50%的patches做修改,其中80%用可学习的\[mask]\embedding替代,10%随机初始化,10%保持原样
* 自监督学习时,predict mean,3bit color获得了best few-shot表现
**可能的改进:
* 将1D pos embedding换成2D rope embedding,增强位置信息表示
