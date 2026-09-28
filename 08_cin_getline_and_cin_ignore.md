# 8. `cin`, `getline`, and `cin.ignore`

These are standard C++ input patterns used alongside the lecture's
string material.

## `cin >>`

``` cpp
string name;
cin >> name;
```

Reads only until whitespace.

Input:

``` text
Yusuf Sabuwala
```

`name` receives only:

``` text
Yusuf
```

Use `cin >>` for simple single-token input:

``` cpp
int age;
double gpa;
string word;

cin >> age;
cin >> gpa;
cin >> word;
```

## `getline`

``` cpp
string name;
getline(cin, name);
```

Reads the entire line including spaces.

Input:

``` text
Yusuf Sabuwala
```

Result:

``` text
Yusuf Sabuwala
```

## The common `cin >>` + `getline` problem

``` cpp
int age;
string name;

cin >> age;
getline(cin, name);
```

Suppose input is:

``` text
19 ENTER
Yusuf Sabuwala ENTER
```

After:

``` cpp
cin >> age;
```

the newline from pressing Enter remains in the input stream.

Then:

``` cpp
getline(cin, name);
```

sees that newline immediately and reads an empty line.

## Fix using `cin.ignore()`

``` cpp
int age;
string name;

cin >> age;
cin.ignore();
getline(cin, name);
```

For simple classroom input, this removes the leftover newline.

A more robust version is:

``` cpp
#include <limits>

cin.ignore(numeric_limits<streamsize>::max(), '\n');
```

Example:

``` cpp
int age;
string fullName;

cout << "Age: ";
cin >> age;

cin.ignore(numeric_limits<streamsize>::max(), '\n');

cout << "Full name: ";
getline(cin, fullName);
```

### When should you use `cin.ignore()`?

Main pattern to remember:

``` cpp
cin >> something;
cin.ignore();
getline(cin, stringVariable);
```

You usually do **not** need it between two `getline`s:

``` cpp
getline(cin, firstName);
getline(cin, address);
```

And normally not between ordinary `cin >>` operations:

``` cpp
cin >> age;
cin >> gpa;
```

------------------------------------------------------------------------
