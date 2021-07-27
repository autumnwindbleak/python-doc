```python
# 1字母处理：
.upper()   # 全部大写
.lower()   # 全部小写
.swapcase()   # 大小写互换
.capitalize()   # 首字母大写，其余小写
.title()   # 首字母大写

# 2格式化相关
.ljust(width)    # 获取固定长度，左对齐，右边不够用空格补齐
.rjust(width)    # 获取固定长度，右对齐，左边不够用空格补齐
.center(width) # 获取固定长度，中间对齐，两边不够用空格补齐
.zfill(width)     # 获取固定长度，右对齐，左边不足用0补齐

# 3 字符串搜索相关
.find()   # 搜索指定字符串，没有返回-1
.index()   # 同上，但是找不到会报错
.rfind()   # 从右边开始查找
.count()   # 统计指定的字符串出现的次数
# 上面所有方法都可以用index代替，不同的是使用index查找不到会抛异常，而find返回-1

# 4字符串替换
.replace('old','new')    # 替换old为new
.replace('old','new',次数)    # 替换指定次数的old为new


# 5字符串去空格及去指定字符
.strip()    # 去两边空格
.lstrip()    # 去左边空格
.rstrip()    # 去右边空格
.split()    # 默认按空格分隔
.split('指定字符')    # 按指定字符分割字符串为数组

# 6字符串判断相关
.startswith('start')    # 是否以start开头
.endswith('end')    # 是否以end结尾
.isalnum()    # 是否全为字母或数字
.isalpha()    # 是否全字母
.isdigit()    # 是否全数字
.islower()    # 是否全小写
.isupper()    # 是否全大写
.istitle()    # 判断首字母是否为大写
.isspace()    # 判断字符是否为空格

isdigit()
True:Unicode数字，byte数字（单字节），全角数字（双字节），罗马数字
False: 汉字数字
Error: 无
 
isdecimal()
True:Unicode数字，，全角数字（双字节）
False: 罗马数字，汉字数字
Error: byte数字（单字节）
 
isnumeric()
True:Unicode数字，全角数字（双字节），罗马数字，汉字数字
False: 无
Error: byte数字（单字节）

```

