# 16. Static Class Attributes and Methods

A static attribute belongs to the class itself and is shared by all
objects.

``` cpp
class Student
{
private:
    static int count;

public:
    Student()
    {
        count++;
    }

    static int getCount()
    {
        return count;
    }
};
```

The static attribute is defined outside the class:

``` cpp
int Student::count = 0;
```

Then:

``` cpp
Student a;
Student b;
Student c;

cout << Student::getCount();
```

prints:

``` text
3
```

There is one shared `count`, not one count per object.

Static methods can directly access static class data:

``` cpp
static int getCount()
{
    return count;
}
```

Access a static member using the class name:

``` cpp
Student::getCount();
```

------------------------------------------------------------------------
