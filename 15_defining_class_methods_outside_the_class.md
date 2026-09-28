# 15. Defining Class Methods Outside the Class

Declaration inside:

``` cpp
class Student
{
private:
    int age;

public:
    void setAge(int a);
    int getAge();
};
```

Definitions outside:

``` cpp
void Student::setAge(int a)
{
    age = a;
}

int Student::getAge()
{
    return age;
}
```

`::` is the scope-resolution operator.

``` cpp
Student::setAge
```

means `setAge` belongs to `Student`.

Call the method on an object using `.`:

``` cpp
Student s;
s.setAge(20);
```

So:

``` text
::   belongs to class/scope
.    member of an object
->   member through a pointer
```

------------------------------------------------------------------------
