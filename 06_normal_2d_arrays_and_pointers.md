# 6. Normal 2D Arrays and Pointers

``` cpp
int a[3][4];
```

Access:

``` cpp
a[i][j]
```

For a true built-in 2D array, `a` refers to rows, not individual `int`s.

For:

``` cpp
int a[3][4];
```

a pointer to one row can be written:

``` cpp
int (*p)[4] = a;
```

Then:

``` cpp
p[1][2]
```

accesses the same element as:

``` cpp
a[1][2]
```

Pointer-style expression:

``` cpp
a[i][j]
*(*(a + i) + j)
```

------------------------------------------------------------------------
