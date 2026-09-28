# 4. Dynamic 1D Arrays

Allocate at runtime:

``` cpp
int n;
cin >> n;

int* a = new int[n];
```

Use it like a normal array:

``` cpp
for (int i = 0; i < n; i++)
    cin >> a[i];

for (int i = 0; i < n; i++)
    cout << a[i] << " ";
```

Deallocate an array with `delete[]`:

``` cpp
delete[] a;
a = nullptr;
```

Do not use:

``` cpp
delete a;       // wrong for new[]
```

Rule:

``` cpp
new int       -> delete
new int[n]    -> delete[]
```

### Passing a dynamic array to a function

``` cpp
void printArray(int* a, int size)
{
    for (int i = 0; i < size; i++)
        cout << a[i] << " ";
}
```

``` cpp
int n = 5;
int* a = new int[n];

printArray(a, n);

delete[] a;
```

The size must be passed separately because a raw dynamic array does not
store its length for you.

------------------------------------------------------------------------
