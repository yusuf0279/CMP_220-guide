# 14. Setters and Getters

Attributes are commonly made private and accessed through public
methods.

``` cpp
class Student
{
private:
    string name;
    int age;

public:
    void setName(string n)
    {
        name = n;
    }

    string getName()
    {
        return name;
    }

    void setAge(int a)
    {
        age = a;
    }

    int getAge()
    {
        return age;
    }
};
```

Use:

``` cpp
Student s;

s.setName("Ali");
s.setAge(19);

cout << s.getName();
cout << s.getAge();
```

A **setter / mutator** modifies an attribute:

``` cpp
void setAge(int a)
{
    age = a;
}
```

A **getter / accessor** returns an attribute:

``` cpp
int getAge()
{
    return age;
}
```

Setters can validate data:

``` cpp
void setAge(int a)
{
    if (a >= 0)
        age = a;
}
```

------------------------------------------------------------------------
