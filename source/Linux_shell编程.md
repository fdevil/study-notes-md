# Linux shell编程

# Linux变量与字符串的删除、替换、替代等处理


## 变量的处理

### 获取变量的长度

```shell
# 一、获取变量内容的长度
[root@temp ~]# url=www.sina.com.cn
[root@temp ~]# echo ${#url}    # 获取变量的长度
15
[root@temp ~]# echo ${url}
www.sina.com.cn
[root@temp ~]# echo ${url#www.}    # "#"删除头部的"www." 只能是头部
sina.com.cn
[root@temp ~]# echo ${url#*.}    # "#"从头删除第一个"www." 使用通配符"*"替代"www"
sina.com.cn
[root@temp ~]# echo 

```
### 变量内容的删除
```

```

