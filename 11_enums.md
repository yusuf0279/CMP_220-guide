# 11. Enums

An enum creates a type consisting of named constant choices.

``` cpp
enum Day
{
    MONDAY,
    TUESDAY,
    WEDNESDAY
};
```

Declare:

``` cpp
Day d = MONDAY;
```

By default, values start from `0` and increase:

``` text
MONDAY    -> 0
TUESDAY   -> 1
WEDNESDAY -> 2
```

You can explicitly assign values:

``` cpp
enum Status
{
    FAILED = 0,
    PASSED = 1,
    PENDING = 5
};
```

Then:

``` cpp
Status s = PASSED;
```

General pattern:

``` cpp
enum TypeName
{
    VALUE1,
    VALUE2,
    VALUE3
};

TypeName variable = VALUE1;
```

Enums are useful when a variable should represent one choice from a
known set instead of using unexplained numeric values.

------------------------------------------------------------------------
