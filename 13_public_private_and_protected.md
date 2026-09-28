# 13. `public`, `private`, and `protected`

## `private`

Accessible from member functions of the class, but not directly from
outside code.

``` cpp
class Student
{
private:
    int id;
};
```

This is invalid from `main`:

``` cpp
Student s;
s.id = 5;       // error
```

Class members are `private` by default.

## `public`

Accessible from outside the class:

``` cpp
class Student
{
public:
    void print()
    {
        cout << "Hello";
    }
};
```

``` cpp
Student s;
s.print();
```

## `protected`

`protected` is similar to `private` for ordinary outside code, but
derived/child classes can access it.

``` cpp
class Person
{
protected:
    string name;
};

class Student : public Person
{
public:
    void setName(string n)
    {
        name = n;       // allowed in derived class
    }
};
```

Outside code still cannot directly do:

``` cpp
Student s;
s.name = "Ali";        // error
```

Quick idea:

``` text
public      -> accessible from outside
private     -> accessible inside this class
protected   -> accessible inside this class and derived classes
```

------------------------------------------------------------------------
