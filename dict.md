```python
.formkeys() # 使用一组键和默认值创建字典 key都指向后面同一个对象

list_var = ["a","b","c"]
dict_var = {}.fromkeys(list_var,[1,2,3])
print(dict_var)
dict_var["a"].append(4)
print(dict_var)


.pop() # 删除键值对，第一个参数是key，第二个是默认值（防止报错）
.popitem() # 删除Uzi后一个键值对
.clear() # 清空
.update() # 批量更新：1. 传入字典，若之前字典包含key则更新，否则新添
		  #			2. 传入键值对 eg: .update(key1 = value1,key2 = value2)
.get() # 通过key 获取值
.keys() # 获取可循环取得的key的数组 （并非数组，是 dict_keys数组）
.values() # 获取可循环取得的value的数组 （并非数组，是 dict_values数组）
.items() # 取得key value 成对的元祖对数组 (并非数组，是dict_items数组)
```

