# 10. Structs

A `struct` creates a new type containing multiple members, which can
have different types.

``` cpp
struct Student
{
    string name;
    int id;
    double gpa;
};
```

Create objects:

``` cpp
Student s1;
Student s2;
```

Access members with `.`:

``` cpp
s1.name = "Ali";
s1.id = 123;
s1.gpa = 3.8;
```

### Initialize a struct

``` cpp
Student s = {"Ali", 123, 3.8};
```

### Copy structs

``` cpp
Student a = {"Ali", 1, 3.5};
Student b;

b = a;
```

For comparisons, compare relevant members:

``` cpp
if (a.id == b.id)
{
    // ...
}
```

### Array of structs

``` cpp
Student students[5];

students[0].name = "Ali";
students[0].id = 100;
```

### Struct containing an array

``` cpp
struct Student
{
    string name;
    int grades[5];
};
```

``` cpp
Student s;
s.grades[0] = 90;
```

### Nested structs

``` cpp
struct Date
{
    int day;
    int month;
    int year;
};

struct Student
{
    string name;
    Date birthday;
};
```

Access:

``` cpp
Student s;

s.birthday.day = 10;
s.birthday.month = 5;
```

Pattern:

``` cpp
object.member
object.inner.member
array[i].member
```

### Pointer as a struct member

``` cpp
struct Node
{
    int value;
    Node* next;
};
```

Self-reference must be through a pointer, not a direct object:

``` cpp
struct Node
{
    Node next;       // invalid: infinitely sized
};
```

Valid:

``` cpp
struct Node
{
    Node* next;
};
```

### Dynamic struct

``` cpp
Student* p = new Student;
```

Access members:

``` cpp
p->name = "Ali";
p->id = 123;
```

Deallocate:

``` cpp
delete p;
p = nullptr;
```

------------------------------------------------------------------------
