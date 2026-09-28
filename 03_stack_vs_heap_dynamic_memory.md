# 3. Stack vs Heap / Dynamic Memory

Normal local variable:

``` cpp
int x = 10;
```

Conceptually, `x` is automatically managed local storage.

Dynamic variable:

``` cpp
int* p = new int;
```

`p` stores the address of a dynamically allocated `int`.

Initialize immediately:

``` cpp
int* p = new int(10);
```

Access it:

``` cpp
cout << *p;
*p = 50;
```

Release it:

``` cpp
delete p;
p = nullptr;
```

The dynamically allocated object does not have an ordinary variable
name. You access it through its pointer.

``` cpp
int* p = new int(7);

*p = 20;
```

### Why set pointer to `nullptr` after delete?

``` cpp
delete p;
p = nullptr;
```

After `delete`, the old address is no longer valid. Leaving the pointer
holding it creates a **dangling pointer**.

------------------------------------------------------------------------
