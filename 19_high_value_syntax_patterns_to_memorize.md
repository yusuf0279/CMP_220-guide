# 19. High-Value Syntax Patterns to Memorize

``` cpp
// POINTER
int x = 10;
int* p = &x;
*p = 20;

// REFERENCE
int& r = x;

// PASS BY REFERENCE
void func(int& x);

// PASS BY POINTER
void func(int* p);
func(&x);

// DYNAMIC VARIABLE
int* p = new int(10);
delete p;
p = nullptr;

// DYNAMIC ARRAY
int* a = new int[n];
delete[] a;

// DYNAMIC 2D ARRAY
int** a = new int*[rows];

for (int i = 0; i < rows; i++)
    a[i] = new int[cols];

for (int i = 0; i < rows; i++)
    delete[] a[i];

delete[] a;

// STRING
string s = "Hello";
s[i];
s.at(i);
s.length();
s.size();
s.empty();
s.substr(pos, len);
s.insert(pos, text);

// FULL-LINE INPUT
getline(cin, s);

// AFTER cin >> BEFORE getline
cin >> x;
cin.ignore();
getline(cin, s);

// VECTOR
vector<int> v;
v.push_back(x);
v.pop_back();
v[i];
v.size();
v.empty();
v.erase(v.begin() + i);

// STRUCT
struct Student
{
    string name;
    int id;
};

Student s;
s.name = "Ali";

// ENUM
enum Day
{
    MONDAY,
    TUESDAY,
    WEDNESDAY
};

Day d = MONDAY;

// CLASS
class Student
{
private:
    int age;

public:
    void setAge(int a);
    int getAge();
};

void Student::setAge(int a)
{
    age = a;
}

int Student::getAge()
{
    return age;
}

// OBJECT
Student s;
s.setAge(20);

// OBJECT POINTER
Student* p = &s;
p->setAge(20);
```

------------------------------------------------------------------------
