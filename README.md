- 分类交叉熵是分类问题合适的损失函数，它最小化模型输出的概率分布和真实label的概率分布之间的距离。
- 处理多分类中label的两种方法：
  - 通过one-hot编码编码label，并使用categorical_crossentropy作为损失函数；
  - 通过整数张量编码label，并使用sparse_categorical_crossentropy损失函数，对于数据分类的类别较多的情况，应该避免创建较小的中间layer，导致信息瓶颈。