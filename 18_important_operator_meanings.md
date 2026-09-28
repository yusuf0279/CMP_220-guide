# 18. Important Operator Meanings

The same symbols can mean different things depending on context.

## `&`

Address-of:

``` cpp
int* p = &x;
```

Reference declaration:

``` cpp
int& r = x;
```

## `*`

Pointer declaration:

``` cpp
int* p;
```

Dereference:

``` cpp
cout << *p;
```

Multiplication:

``` cpp
x = a * b;
```

Context determines the meaning.

## `.`

Member through an object:

``` cpp
s.name
s.print()
```

## `->`

Member through a pointer:

``` cpp
p->name
p->print()
```

## `::`

Member belonging to a class/scope:

``` cpp
Student::getCount()
Student::setAge
```

------------------------------------------------------------------------
