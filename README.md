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









