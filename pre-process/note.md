# 数据预处理

## 练习
删除缺失值最多的列

- 查找：index = inputs.isna().sum().idxmax()
- 删除：inputs.drop(index, axis = 1, inplace = True)