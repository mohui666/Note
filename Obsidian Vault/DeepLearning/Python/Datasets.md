**使用 🤗 Datasets 与 Albumentations 的关键点：**

- 在应用转换之前将 PIL 图像转换为 NumPy 数组
- Albumentations 返回一个字典，其中转换后的图像位于“image”键下
- 将转换后的结果转换回 PIL 格式