# 12. Classes

A class is a user-defined type containing **attributes** and
**methods**.

``` cpp
class Student
{
private:
    string name;
    int id;

public:
    void print()
    {
        cout << name << " " << id;
    }
};
```

Do not forget the semicolon after the class:

``` cpp
};
```

Create objects:

``` cpp
Student s1;
Student s2;
```

Call public methods with `.`:

``` cpp
s1.print();
```

------------------------------------------------------------------------
