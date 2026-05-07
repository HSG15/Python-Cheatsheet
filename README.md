# Python-Cheatsheet

📋 list Cheat Sheet
| Operation      | Syntax               | Description          |
| -------------- | -------------------- | -------------------- |
| Create         | `nums = [1,2,3]`     | Create list          |
| Index          | `nums[0]`            | Access element       |
| Negative index | `nums[-1]`           | Last element         |
| Find index     | `nums.index(2)`      | Index of value       |
| Append         | `nums.append(4)`     | Add to end           |
| Insert         | `nums.insert(0,10)`  | Add at index         |
| Extend         | `nums.extend([5,6])` | Add multiple         |
| Remove value   | `nums.remove(3)`     | Remove first match   |
| Pop            | `nums.pop()`         | Remove & return last |
| Sort           | `nums.sort()`        | In-place sort        |
| Reverse        | `nums.reverse()`     | In-place reverse     |
| Copy           | `nums.copy()`        | Shallow copy         |
| Clear          | `nums.clear()`       | Emptying entire list |
| Length         | `len(nums)`          | Size                 |
| Membership     | `2 in nums`          | Check existence      |

List Slicing
| Pattern                 | Meaning          |
| ----------------------- | ---------------- |
| `nums[start:stop:step]` | Generic slice    |
| `nums[::-1]`            | Reverse list     |
| `nums[1:]`              | From index 1     |
| `nums[:3]`              | First 3 elements |

-----------------------------------------------------------------------

🧮 set Cheat Sheet
| Operation  | Syntax            | Description      |
| ---------- | ----------------- | ---------------- |
| Create     | `s = {1,2,3}`     | Create set       |
| Add        | `s.add(4)`        | Add element      |
| Update     | `s.update([5,6])` | Add multiple     |
| Remove     | `s.remove(3)`     | Error if missing |
| Discard    | `s.discard(3)`    | Safe remove      |
| Pop        | `s.pop()`         | Remove arbitrary |
| Clear      | `s.clear()`       | Remove all       |
| Copy       | `s.copy()`        | Shallow copy     |
| Length     | `len(s)`          | Size             |
| Membership | `1 in s`          | Check existence  |

Set Operations
| Operation      | Syntax     |     |
| -------------- | ---------- | --- |
| Union          | `s1        | s2` |
| Intersection   | `s1 & s2`  |     |
| Difference     | `s1 - s2`  |     |
| Symmetric diff | `s1 ^ s2`  |     |
| Subset         | `s1 <= s2` |     |
| Superset       | `s1 >= s2` |     |

------------------------------------------------------------------------

📦 tuple Cheat Sheet
| Operation      | Syntax        | Description     |
| -------------- | ------------- | --------------- |
| Create         | `t = (1,2,3)` | Create tuple    |
| Single item    | `t = (1,)`    | Trailing comma  |
| Index          | `t[0]`        | Access element  |
| Negative index | `t[-1]`       | Last element    |
| Slice          | `t[1:3]`      | Sub-tuple       |
| Count          | `t.count(2)`  | Occurrences     |
| Index          | `t.index(3)`  | Find index      |
| Length         | `len(t)`      | Size            |
| Membership     | `2 in t`      | Check existence |
| Unpack         | `a,b,c = t`   | Destructure     |

------------------------------------------------------------------------------

🗂 dict Cheat Sheet
| Operation    | Syntax              | Description  |
| ------------ | ------------------- | ------------ |
| Create       | `d = {"a":1}`       | Create dict  |
| Access       | `d["a"]`            | Get value    |
| Safe access  | `d.get("a")`        | No error     |
| Add / Update | `d["b"] = 2`        | Set key      |
| Update many  | `d.update({"c":3})` | Bulk update  |
| Pop          | `d.pop("a")`        | Remove key   |
| Pop last     | `d.popitem()`       | LIFO         |
| Delete       | `del d["b"]`        | Remove key   |
| Clear        | `d.clear()`         | Remove all   |
| Copy         | `d.copy()`          | Shallow copy |
| Length       | `len(d)`            | # of keys    |
| Key check    | `"a" in d`          | Membership   |

Dict Views
| View   | Syntax       |
| ------ | ------------ |
| Keys   | `d.keys()`   |
| Values | `d.values()` |
| Items  | `d.items()`  |

------------------------------------------------------------------------------

🧠 Quick Summary
| Type  | Ordered  | Mutable | Duplicates |
| ----- | -------- | ------- | ---------- |
| list  | ✅        | ✅       | ✅          |
| set   | ❌        | ✅       | ❌          |
| tuple | ✅        | ❌       | ✅          |
| dict  | ✅ (3.7+) | ✅       | ❌ (keys)   |


--------------------------------------------------------------------------------
--------------------------------------------------------------------------------

---

# 🧠 1. List vs Tuple vs Set vs Dictionary

### Key Differences:

| Type  | Ordered | Mutable | Duplicates | Example   |
| ----- | ------- | ------- | ---------- | --------- |
| List  | Yes     | Yes     | Yes        | `[1,2,2]` |
| Tuple | Yes     | No      | Yes        | `(1,2,2)` |
| Set   | No      | Yes     | No         | `{1,2}`   |
| Dict  | Yes*    | Yes     | Keys: No   | `{"a":1}` |

(*Ordered since Python 3.7+)

### Example:

```python
lst = [1,2,2]
tup = (1,2,2)
st = {1,2,2}     # {1,2}
d = {"a":1, "b":2}
```

---

# 🔁 2. Deep Copy vs Shallow Copy

### Shallow Copy:

* Copies only outer object
* Inner objects are shared

### Deep Copy:

* Copies everything recursively

### Example:

```python
import copy

a = [[1,2],[3,4]]

b = copy.copy(a)       # shallow
b[0][0] = 99           # affects 'a'

c = copy.deepcopy(a)   # deep
c[0][0] = 100          # does NOT affect 'a'
```

---

# ⚙️ 3. Mutable vs Immutable

### Mutable:

* Can change after creation
* Examples: list, dict, set

### Immutable:

* Cannot change
* Examples: tuple, string, int

```python
a = [1,2]
a[0] = 10   # allowed

b = (1,2)
# b[0] = 10 ❌ error
```

---

# 🔍 4. `is` vs `==`

* `==` → compares values
* `is` → compares memory location

```python
a = [1,2]
b = [1,2]

print(a == b)  # True
print(a is b)  # False
```

---

# 🎯 5. Decorators

* Modify function behavior without changing code

```python
def my_decorator(func):
    def wrapper():
        print("Before")
        func()
        print("After")
    return wrapper

@my_decorator
def hello():
    print("Hello")

hello()
```

---

# 📦 6. `*args` vs `**kwargs`

* `*args` → multiple positional arguments
* `**kwargs` → multiple keyword arguments

```python
def func(*args, **kwargs):
    print(args)
    print(kwargs)

func(1,2, name="A")
```

---

# ⚡ 7. Lambda Function

* Anonymous one-line function

```python
square = lambda x: x*x
print(square(5))  # 25
```

---

# 🏗️ 8. Instance vs Class vs Static Methods

```python
class A:
    def instance(self):
        print("Instance")

    @classmethod
    def cls_method(cls):
        print("Class")

    @staticmethod
    def static():
        print("Static")
```

* Instance → uses `self`
* Class → uses `cls`
* Static → no access to class/object

---

# 🔗 9. Inheritance

* Reuse code from parent class

```python
class Parent:
    def show(self):
        print("Parent")

class Child(Parent):
    pass

c = Child()
c.show()
```

### Types:

* Single
* Multiple
* Multilevel
* Hierarchical

---

# 🔁 10. Overloading vs Overriding

### Overriding:

```python
class A:
    def show(self):
        print("A")

class B(A):
    def show(self):
        print("B")
```

### Overloading:

(Not direct in Python, use default args)

```python
def add(a, b=0):
    return a + b
```

---

# 🧠 11. Memory Management

* Python uses **private heap**
* Managed by interpreter
* Uses reference counting + garbage collection

---

# 🗑️ 12. Garbage Collection

* Removes unused objects

```python
a = [1,2]
del a  # memory freed
```

---

# 🔒 13. GIL (Global Interpreter Lock)

* Allows only **one thread to execute at a time**
* Affects CPU-bound tasks
* Not an issue for I/O tasks

---

# 🔄 14. Iterators vs Generators

### Iterator:

* Uses `__iter__()` and `__next__()`

### Generator:

* Uses `yield`

```python
def gen():
    yield 1
    yield 2
```

---

# 🔢 15. `range()` vs `xrange()`

* `range()` → returns object (Python 3)
* `xrange()` → only in Python 2 ❌

👉 Interview tip:

> In Python 3, `range()` behaves like `xrange()`.

---

# 🔄 16. map vs filter vs reduce

```python
from functools import reduce

nums = [1,2,3,4]

print(list(map(lambda x: x*2, nums)))
print(list(filter(lambda x: x%2==0, nums)))
print(reduce(lambda x,y: x+y, nums))
```

* map → transform
* filter → condition
* reduce → aggregate

---

# 🧾 17. List Comprehension

* Short way to create lists

```python
squares = [x*x for x in range(5)]
```

---

# 📉 18. Handling Missing Values

```python
import math
import pandas as pd

x = None
y = float('nan')

pd.isna(y)   # True
```

* Use: `None`, `NaN`, `fillna()`, `dropna()`

---

# 📚 19. Data Libraries

Common ones:

* pandas → data handling
* numpy → numerical ops
* pyspark → big data
* sqlalchemy → DB

---

# 📊 20. DataFrame vs Dictionary

| Feature   | DataFrame     | Dictionary |
| --------- | ------------- | ---------- |
| Structure | Tabular       | Key-value  |
| Library   | pandas        | built-in   |
| Use       | Data analysis | general    |

```python
import pandas as pd

df = pd.DataFrame({"a":[1,2]})
```
---







