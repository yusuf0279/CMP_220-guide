# 5. Dynamic 2D Arrays on the Heap

A common CMP-style method uses `int**`.

Suppose:

``` cpp
int rows = 3;
int cols = 4;
```

First allocate an array of row pointers:

``` cpp
int** a = new int*[rows];
```

Then allocate each row:

``` cpp
for (int i = 0; i < rows; i++)
{
    a[i] = new int[cols];
}
```

Conceptually:

``` text
a
|
v
+-----+       +---+---+---+---+
|  *  | ----> |   |   |   |   |
+-----+       +---+---+---+---+
|  *  | ----> |   |   |   |   |
+-----+       +---+---+---+---+
|  *  | ----> |   |   |   |   |
+-----+       +---+---+---+---+
```

Use it normally:

``` cpp
a[0][0] = 5;
a[1][2] = 10;
```

Input:

``` cpp
for (int i = 0; i < rows; i++)
{
    for (int j = 0; j < cols; j++)
    {
        cin >> a[i][j];
    }
}
```

Output:

``` cpp
for (int i = 0; i < rows; i++)
{
    for (int j = 0; j < cols; j++)
    {
        cout << a[i][j] << " ";
    }

    cout << endl;
}
```

### Deallocating a dynamic 2D array

Reverse the allocation process.

First delete every row:

``` cpp
for (int i = 0; i < rows; i++)
{
    delete[] a[i];
}
```

Then delete the array of pointers:

``` cpp
delete[] a;
a = nullptr;
```

Full pattern:

``` cpp
int** a = new int*[rows];

for (int i = 0; i < rows; i++)
    a[i] = new int[cols];

// use a[i][j]

for (int i = 0; i < rows; i++)
    delete[] a[i];

delete[] a;
a = nullptr;
```

------------------------------------------------------------------------
