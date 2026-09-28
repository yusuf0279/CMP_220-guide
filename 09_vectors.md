# 9. Vectors

Include:

``` cpp
#include <vector>
```

A vector is a dynamic array managed by the STL.

Declaration:

``` cpp
vector<int> nums;
vector<double> prices;
vector<string> names;
```

### Initialization

Empty:

``` cpp
vector<int> v;
```

With values:

``` cpp
vector<int> v = {10, 20, 30};
```

Create 5 integers initialized to `0`:

``` cpp
vector<int> v(5);
```

Create 5 integers each containing `7`:

``` cpp
vector<int> v(5, 7);
```

Copy another vector:

``` cpp
vector<int> a = {1, 2, 3};
vector<int> b(a);
```

or:

``` cpp
vector<int> b = a;
```

### `.push_back()`

Adds an element to the end:

``` cpp
vector<int> v;

v.push_back(10);
v.push_back(20);
v.push_back(30);
```

Now:

``` text
{10, 20, 30}
```

### Access

``` cpp
cout << v[0];
v[1] = 100;
```

Important:

``` cpp
vector<int> v;
v[0] = 5;       // WRONG: size is still 0
```

Instead:

``` cpp
v.push_back(5);
```

or create elements first:

``` cpp
vector<int> v(5);
v[0] = 5;
```

### `.size()`

``` cpp
cout << v.size();
```

Number of existing elements.

### `.empty()`

``` cpp
if (v.empty())
{
    cout << "Vector is empty";
}
```

### `.pop_back()`

Removes the last element:

``` cpp
vector<int> v = {10, 20, 30};

v.pop_back();
```

Now:

``` text
{10, 20}
```

### `.erase()`

Remove the element at index `i`:

``` cpp
v.erase(v.begin() + i);
```

Example:

``` cpp
vector<int> v = {10, 20, 30, 40};

v.erase(v.begin() + 1);
```

Result:

``` text
{10, 30, 40}
```

### Loop through vector

``` cpp
for (int i = 0; i < v.size(); i++)
{
    cout << v[i] << " ";
}
```

### Vector memory idea

The vector object manages its own dynamic storage. You do not manually
use `new[]` and `delete[]` for its elements.

``` cpp
vector<int> v;

v.push_back(10);
v.push_back(20);
```

The vector automatically obtains more storage when necessary and
releases its owned storage when the vector is destroyed.

------------------------------------------------------------------------
