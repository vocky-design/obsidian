###### python字典
```python
改：


增：
d = {"one":"1", "two":"2"}		#方法1
d = dict(one = "1", two = "2")  #方法2
d = dict.fromkeys("Vokcy", 250) #方法3

删：
d.pop("one", "没有one")
d.popitem()
d.clear()
del d

改：
d["one"] = 3					#不推荐，因为字典没有会报错
d.update(?)

查：


打印：
d
动态视图对象
d.get('one', "没有one")		
d.setdefault("one", "1")   #如果没有one，则增加one
```