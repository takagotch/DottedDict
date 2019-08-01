### dotteddict
---
https://github.com/carlosescri/DottedDict

```py
from dotted.collection import DottedCollection, DottedDict, DottedList
obj = DottedCollection.factory(dict_or_list)
obj = DottedCollection.load_json(json_value)
obj = DottedDict(a_dict)
obj = DottedList(a_list)

from dotted.utils import dot, dot_json

obj = dot(dict_or_list)
obj = dot_json(json_value)

obj = DottedList([0, 1, 2, 3, [4, 5, 6], 7, 8, [9, 10]])

obj[0] == 0
obj['1'] == 1
obj['4.0'] == 4
obj['4.2'] == 6
obj[5] == 7
obj['7.1'] == 10

obj.append(12)

obj[8] = 11

obj = DottedDict({'hello': {'world': {'wide': 'web'}}})

from dotted.utils import dot, dot_json
obj = dot({'hello': 'world'})
obj = dot_json('{"hello": "world"}')

from dotted.utils import dot, dot_json
obj = dot({"hello\.world": "Hello!"})
obj = dot_json('{"hello\\\\.world": "Hello!"}')
value = obj["hello\.world"] 
```

```sh
python -m dotted.test.test_collection
```

```
```


