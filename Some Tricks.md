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

```
for (int key : hashmap.keySet()) {

}
```



### Latex公式表示

|     名称     |                 Latex表示                  |                    示例                    |
| :----------: | :----------------------------------------: | :----------------------------------------: |
|   粗体字母   |                 \mathbf{}                  |                $\mathbf{A}$                |
|   空心字母   |                 \mathbb{}                  |                $\mathbb{A}$                |
|    大括号    | \begin{cases} a & b \\\\ c & d \end{cases} | $\begin{cases} a & b \\ c & d \end{cases}$ |
|    无限大    |                   \infty                   |                  $\infty$                  |
|     空格     |                     \                      |                    $\ $                    |
|     分数     |                \frac{a}{b}                 |               $\frac{a}{b}$                |
|   求和符号   |              \sum\limits_{a}               |             $\sum\limits_{a}$              |
| 字母上方箭头 |  \overrightarrow{a} 或 \overleftarrow{b}   | $\overrightarrow{a}$或$\overleftarrow{b}$  |
|     圈加     |                   \oplus                   |                  $\oplus$                  |
|     换行     |   \begin{split} &aaa \\ &bb \end{split}    |  $\begin{split} &aaa \\ &bb \end{split}$   |

### Git修改已提交的commit的作者信息

1. 进入Git Bash；

2. 输入指令，查看前n条记录：

   ```
   git rebase -i HEAD~n
   ```
   
3. 使用VIM指令，先按"ESC"，然后按"S"进入插入模式。将需要修改的提交前面的"pick"修改为"edit"；

4. 再次按"ESC"，然后输入":wq"并回车保存文本内容并退出VIM；

5. 输入指令，修改作者信息：

   ```
   git commit --amend --author "Zhang Lei <942471854@qq.com>" --no-edit
   ```

6. 输入指令，进入下一条commit进行修改：

   ```
   git rebase --continue
   ```

7. 重复步骤5/6，直至完成修改出现下述提示信息：

   ```
   Successfully rebased and updated refs/heads/master.
   ```

### Git删除commit

1. 进入Git Bash；

2. 输入指令，跳转到待删除的commit的前一条commit

   ```
   git rebase -i 42ce4f1ed3c4efcbb9456614c1a4a264856048d3
   ```

3. 按“I”进入编辑模式，将需要删除的commit的pick改为drop

4. 按“ESC”退出编辑，输入":wq"并回车保存

### 注册表修改右键新建文件菜单

- 地址：计算机\HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Discardable\PostSetup\ShellNew
- 双击Classes打开文件
- 删除不需要的后缀名

