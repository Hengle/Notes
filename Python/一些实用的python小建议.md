# һЩʵ�õ�pythonС����

## ��dict����Ĭ��ֵ

��������������`key`��Ĭ��ֵΪ`[]`�����������`key`

```python
from collections import defaultdict
context = defaultdict(list)
```

`setdefault`һ��ֻ������һ��ֵ�����ô�����ʹ����ʽ�﷨����`defaultdict`����һЩ

```python
context = {}
context.setdefault('name_list', []).append('Fiona')
```

������`fromkeys`���÷�`dict.fromkeys(seq[, value]))`��`value`Ĭ���ǹ��ʹ�����`None`

```python
name_list = ['kevin', 'robin']
context = {}.fromkeys(name_list, 9)
# {'kevin': 9, 'robin': 9}
 
context = dict.fromkeys([1, 2], True)  
# {1: True, 2: True}
```

## �б�ȥ�صĿ��ٷ���

���� set Ҫ�죬���ԣ�http://www.peterbe.com/plog/uniqifiers-benchmark

```python
{}.fromkeys(mylist).keys()
```

## �б����
```python
a = [3, 2, 1]
b = a[:]
```

## �ֵ����
```python
a = {'male':0, 'female': 1}
b = a.copy()
```

## ʱ��ת�����
### ��ȡ�����������ʱ��(date)
```python
from datetime import datetime
 
n_date = datetime.now().date()
n_date = datetime.today().date()
```

### date -> datetime
```python
from datetime import datetime
 
b = datetime.combine(n_date, datetime.min.time())
# datetime.datetime(2015, 9, 8, 0, 0)
```

### datetime -> date
```python
# datetime.datetime(2015, 6, 5, 11, 45, 45, 393548)
a = datetime.datetime()
# datetime.datetime(2016, 6, 5)
b = a.date()
```

### time.struct_time -> datetime
һ��`time.localtime()`������`time.striptime()`�õ��ľ���`time.struct_time`

ʹ��λ�ò���

```python
structTime = time.localtime()
datetime.datetime(*structTime[:6])
# datetime.datetime(2009, 11, 8, 20, 32, 35)
```

����ʹ��`datetime.fromtimestamp`������Ҫע��˴���ʱ�䲻������ 1970-01-01 00:00

```python
from time import mktime
from datetime import datetime
 
dt = datetime.fromtimestamp(mktime(struct))
```

### ��������֮��
```python
from datetime import date
 
d0 = date(2008, 8, 18)
d1 = date(2008, 9, 26)
delta = d0 - d1
print delta.days
```

### ��ȡmilliseconds(13λ����)
```python
import time
from datetime import datetime
 
time.time()  # 1441769033.549239
int(time.time() * 1000)   # 1441769033549
 
# or
def unix_time_milliseconds:
    time_gap = datetime.utcnow() - datetime.utcfromtimestamp(0)
    return int(time_gap.total_seconds() * 1000)   # 1441769033549
```

## ʹ��`map`�� iterator
����`func`����Ϊ`None`ʱ������ iterator �����ã����������ʹ����`zip`��Ψһ��������`map`���԰�����б���չ

python2.x �е�`itertools.zip_longest`��������˴�`map`��ͬ��Ч��

```python
map(None, xrange(3), xrange(10,12))
# [(0, 10), (1, 11), (2, None)]
zip(xrange(3), xrange(10,12))
# [(0, 10), (1, 11)]
```

## �ж�����
��Ȼ��ʹ��λ���������

```python
if a & 1:
    print 'it is even'
```

## dictɾ��key
Ҫɾ����`key`�����϶�(����һ��)�Ļ���������������`dict`������������٣���`pop`��`del`�����Ե�����£�`del`�Կ�һЩ

```python
python -m timeit -s "d = {'f':1,'foo':2,'bar':3}" "d1 = d.copy()" "for k in d1.keys():" "  if k.startswith('f'):" "    del d1[k]"
# 1000000 loops, best of 3: 0.827 usec per loop
```

```python
python -m timeit -s "d = {'f':1,'foo':2,'bar':3}" "d1 = d.copy()" "for k in d1.keys():" "  if k.startswith('f'):" "    d1.pop(k)"
# 1000000 loops, best of 3: 0.96 usec per loop
```