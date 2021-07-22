# Some Tricks

### 离线使用SSH

- 运行程序 nohup python xxx.py & 

- 查看输出 tail -f nohup.out

### ndarray数对形式 

- 给每个位置命名

```python
train_api_array = np.array(train_api, dtype='int32')
train_api_index_array = np.array(train_api_index, dtype=[('length', '<u4'), ('pos', '<u4')])
```

- 保存这个类型的数组到.h5文件

```python
with h5py.File('train.api.h5') as f:
    f['phrases'] = train_api_array
    f['indices'] = train_api_index_array
```

### 可视化模型训练

- 在模型logs的父目录打开CMD
- tensorboard --logdir=logs

### 遍历哈希表

```java
for(HashMap.Entry<String, String> entry : hashmap.entrySet()) {
   System.out.println("Key: " + entry.getKey() + " Value: " + entry.getValue());
}
```

### Latex公式表示

|   名称   |                 Latex表示                  |                    示例                    |
| :------: | :----------------------------------------: | :----------------------------------------: |
| 字母粗体 |                 \mathbf{}                  |                $\mathbf{A}$                |
|  大括号  | \begin{cases} a & b \\\\ c & d \end{cases} | $\begin{cases} a & b \\ c & d \end{cases}$ |
|  无限大  |                   \infty                   |                  $\infty$                  |
|   空格   |                     \                      |                    $\ $                    |

