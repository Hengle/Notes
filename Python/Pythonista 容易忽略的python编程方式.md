# Pythonista ���׺��Ե�python��̷�ʽ
## Python ֮��
> The Zen of Python, by Tim Peters

> Beautiful is better than ugly.

> ����ʤ�ڳ�ª��Python�Ա�д�����Ĵ���ΪĿ�꣩

> Explicit is better than implicit.

> ����ʤ�ڻ�ɬ�������Ĵ���Ӧ�������˵ģ������淶��������ƣ�

> Simple is better than complex.

> ���ʤ�ڸ��ӣ������Ĵ���Ӧ���Ǽ��ģ���Ҫ�и��ӵ��ڲ�ʵ�֣�

> Complex is better than complicated.

> ����ʤ�����ң�������Ӳ��ɱ��⣬�Ǵ����Ҳ�������Ѷ��Ĺ�ϵ��Ҫ���ֽӿڼ�ࣩ

> Flat is better than nested.

> ��ƽʤ��Ƕ�ף������Ĵ���Ӧ���Ǳ�ƽ�ģ�������̫���Ƕ�ף�

> Sparse is better than dense.

> ���ʤ�ڽ��գ������Ĵ������ʵ��ļ������Ҫ����һ�д��������⣩

> Readability counts.

> �ɶ��Ժ���Ҫ�������Ĵ����ǿɶ��ģ�

> Special cases aren��t special enough to break the rules.

> Although practicality beats purity.

> ����ٽ�������ʵ����֮����Ҳ����Υ����Щ������Щ�����������ϣ�

> Errors should never pass silently.

> Unless explicitly silenced.

> ��Ҫ�������д��󣬳�����ȷ����Ҫ����������׼�ز����쳣����дexcept:pass���Ĵ��룩

> In the face of ambiguity, refuse the temptation to guess.

> �����ڶ��ֿ��ܣ���Ҫ����ȥ�²�

> There should be one�C and preferably only one �Cobvious way to do it.

> ���Ǿ�����һ�֣������Ψһһ�����ԵĽ�������������ȷ����������ٷ���

> Although that way may not be obvious at first unless you��re Dutch.

> ��Ȼ�Ⲣ�����ף���Ϊ�㲻�� Python ֮���������Dutch��ָGuido��

> Now is better than never.

> Although never is often better than right now.

> ��Ҳ��ù�������������˼���Ͷ��ֻ����粻��������֮ǰҪϸ˼����

> If the implementation is hard to explain, it��s a bad idea.

> If the implementation is easy to explain, it may be a good idea.

> ������޷�����������ķ������ǿ϶�����һ���÷�������֮��Ȼ������������׼��

> Namespaces are one honking great idea �� let��s do more of those!

> �����ռ���һ�־�����������Ӧ��������ã���������٣�

## python��̿ո������
1. ÿ������ʹ��4���ո�

2. ��Ҫʹ��Tab������ҪTab�Ϳո����

3. ��������֮��ʹ��һ�����У�����Class֮��ʹ����������

4. ���һ���ո����ֵ䡢�б����С������б��еġ��������Լ����ֵ��еġ�����֮�󣬶�����֮ǰ

5. �ڸ�ֵ�ͱȽ����߷���һ���ո񣨲����б��г��⣩

6. �������ź�����߲����б�ǰһ���ַ���Ҫ���ڿո�

## ʹ�����·�ʽ����pyhton��ֵ
```python
b, a = a, b
 
# ��������
 
In [1]: people = ["David", "Pythonista", "15145551234"]
In [2]: name, title, phone = people
In [3]: name
Out[3]: "David"
In [4]: title
Out[4]: "Pythonista"
In [5]: phone
Out[5]: "15145551234"
 
�����﷨��Forѭ���зǳ�ʵ�ã�
 
In [6]: people = [["David", "Pythonista", "15145551234"], ["Wu", "Student", "15101365547"]]
In [7]: for name, title, phone in people:
...: print name, phone
...:
David 15145551234
Wu 15101365547

PS����ʹ�������﷨ʱ����Ҫȷ����ߵı����������ұ�tuple�ĸ���һ�£�����Python���׳�ValueError�쳣��
```

## �ϲ��ַ�����ֵ
```python
result = ��,��.join(colors)
```

������Ч��Ҫ��ʹ��forѭ������ƴ�ӵ�Ч�ʸߣ���listԪ��Խ���ʱ��Խ����

## ʹ�ùؼ���`in`
��Ҫ�ж�һ��key�Ƿ����ֵ��е�ʱ��

```python
d = {"a": 1, "b": 2}
if "c" in d:
print True
# DO NOT USE
if d.has_key("c"):
print True
for key in d:
print key
# DO NOT USE
for key in d.keys():
print key
```

Python��`dict`�����Ƕ�KEY����`hash`�ģ���`keys()`�����Ὣ`dict`�����е�KEY��Ϊһ��`list`�������ԣ�ֱ��ʹ��in��ʱ��ִ��Ч�ʻ�ȽϿ죬����Ҳ�����

## �ֵ�
`dict`��Python���õ����ݽṹ����дPython����ʱ�ᾭ���õ����������һ������`get`������`defaultdict`����

1. `get`

	�ڻ�ȡ`dict`�е�����ʱ������һ��ʹ��index�ķ�ʽ���������KEY�����ڵ�ʱ����׳�`KeyError`����ʱ�������ʹ��`get`������ʹ�÷�����`dict.get(key, default=None)`�����Ա����쳣�����磺
	
	```python
	d = {"a": 1, "b": 2}
	print d.get("c") # None
	print d.get("c", 14) # 14
	```
	
2. `fromkeys`

	dict�����и�`fromkeys`����������ͨ��һ��`list`����һ��`dict`���������ṩĬ�ϵ�`value`�����磺
	
	```python
	# ?������ key,���ṩĬ��value
	>>> dict.fromkeys(["a", "b", "c"], 1)
	# {"a": 1, "c": 1, "b": 1}���������
	```

3. ��Щ����£�������Ҫ��dict��KEYһ��Ĭ��ֵ�����������д��

	```python
	equities = {}
	for (portfolio, equity) in data:
	equities.setdefault(portfolio, []).append(equity)
	```
	
	`setdefault`�����൱��"get, or set & get"�������൱��"set if necessary, then get"
	
## defaultdict
`defaultdict()`��`namedtuple()`��`collections`ģ������2����ʵ�õ���չ���͡�һ���̳���`dict`ϵͳ��������,һ���̳���`tuple`ϵͳ��������

## �ֵ����
��Python�У������ʹ��`zip`����������`list`��װ��һ��`dict`������һ��`list`��ֵ��ΪKEY������һ��`list`��ֵ��ΪVALUE��

```python
>>> given = ["John", "Eric", "Terry", "Michael"]
>>> family = ["Cleese", "Idle", "Gilliam", "Palin"]
>>> pythons = dict(zip(given, family))
>>> print pythons
{"John": "Cleese", "Michael": "Palin", "Eric": "Idle", "Terry": "Gilliam"}
```

�෴�ģ������ʹ��dict��`keys()`��`values()`��������ȡKEY��VALUE���б�

```python
>>> pythons.keys()
["John", "Michael", "Eric", "Terry"]
>>> pythons.values()
["Cleese", "Palin", "Idle", "Gilliam"]
```

## python��`True`
��Python�У��ж�һ�������Ƿ�Ϊ`True`��ʱ���������������

> False True

> False (== 0) True (== 1)

> "" (���ַ���) �� "" ֮����ַ���("", "anything")

> 0, 0.0 �� 0 ֮�������(1, 0.1, -1, 3.14)

> [], (), {}, set() �ǿյ�list��tuple��set��dict ([0], (None,), [""])

> None �󲿷ֵĶ��󣬳�����ȷָ��ΪFalse�Ķ���

�����Լ�������class�����������ȷ��ָ������ʵ����`True`��`False`��������Լ�ʵ��class��`nonzero`��`len`�����������class��һ��`container`ʱ�������ʵ��`len`���������£�

```python
class MyContainer(object):
    def __init__(self, data):
        self.data = data
    def __len__(self):
    """ Return my length. """
        return len(self.data)
```

������class����`container`�������ʵ��`nonzero`���������£�

```python
class MyClass(object):
    def __init__(self, value):
        self.value = value
    def __nonzero__(self):
    """ Return my truth value (True or False). """
        # This could be arbitrarily complex:
        return bool(self.value)
```

��Python 3.x�У�`nonzero`������`bool`������������ǵ������ԣ��������class�����м������µĴ��룺

```python
__bool__ = __nonzero__
```