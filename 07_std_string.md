# 7. `std::string`

Include:

``` cpp
#include <string>
```

Declaration:

``` cpp
string s;
string s = "Hello";
string s("Hello");
```

### Assignment

``` cpp
string a = "Hello";
string b;

b = a;
```

Using `assign`:

``` cpp
b.assign(a);
```

Copy part of another string:

``` cpp
string s1 = "ABCDEFG";
string s2;

s2.assign(s1, 2, 3);
```

Result:

``` text
CDE
```

because it starts at index `2` and copies `3` characters.

### Access characters with `[]`

``` cpp
string s = "Hello";

cout << s[0];     // H
s[0] = 'Y';       // Yello
```

### `.at()`

``` cpp
cout << s.at(1);
s.at(1) = 'a';
```

Difference:

``` cpp
s[i]
s.at(i)
```

`.at()` performs bounds checking and can throw an out-of-range exception
for an invalid index.

### Concatenation `+`

``` cpp
string first = "Hello";
string second = " World";

string result = first + second;
```

### `+=`

``` cpp
string s = "Hello";

s += " World";
s += '!';
```

### `.length()` / `.size()`

``` cpp
string s = "Hello";

cout << s.length();    // 5
cout << s.size();      // 5
```

For `string`, these give the same character count.

### `.empty()`

``` cpp
if (s.empty())
{
    cout << "Empty";
}
```

Returns `true` when the string has no characters.

### `.substr()`

``` cpp
string s = "ABCDEFG";

string x = s.substr(2, 3);
```

Result:

``` text
CDE
```

Syntax:

``` cpp
s.substr(start, length)
```

From a position to the end:

``` cpp
string x = s.substr(2);
```

Result:

``` text
CDEFG
```

### `.insert()`

``` cpp
string s = "Helo";

s.insert(3, "l");
```

Result:

``` text
Hello
```

General idea:

``` cpp
s.insert(position, anotherString);
```

### String comparisons

``` cpp
if (a == b)
if (a != b)
if (a < b)
if (a <= b)
if (a > b)
if (a >= b)
```

Strings are compared lexicographically/alphabetically.

------------------------------------------------------------------------
