# IndexArrayList
一种列表型的数据结构，适用于大数据集，可加快 增、查、改 的速度，用300万测试集测，速度是 LinkedList的 两百多倍

## 算法说明

- 本算法只适用于 增加(或修改 `put()` )、查找 ( `get()` )，这几个操作速度非常快；但是删除操作就非常非常慢，所以本人没有实现删除方法.

- 算法的思想是使用了二级索引的方式来构建列表，同时列表的每个结点又是一个数组( 因为这个原因删除时就必须要移动后面的所有元素，导致删除速度特别慢)

- 本算法构建的数据结构，本质上是一个列表，所以凡是能用列表，并且需要频繁增、改、查的地方，都适用

- 若在大数据集上速率还不满意，可以通过适当增大 `BLOCK_SIZE = xxx` 和 `BUFFER_SIZE = xxx` 这两个参数来调节
