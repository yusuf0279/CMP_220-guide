# 17. Objects and Pointers

Normal object:

``` cpp
Student s;
s.setAge(20);
```

Pointer to existing object:

``` cpp
Student s;
Student* p = &s;

p->setAge(20);
```

Dynamic object:

``` cpp
Student* p = new Student;

p->setAge(20);
cout << p->getAge();

delete p;
p = nullptr;
```

Remember:

``` cpp
object.member
pointer->member
```

and:

``` cpp
p->member
```

is equivalent to:

``` cpp
(*p).member
```

------------------------------------------------------------------------
