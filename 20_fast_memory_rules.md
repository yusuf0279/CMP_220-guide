# 20. Fast Memory Rules

``` text
&x          address of x
*p          value pointed to by p

int* p      p is a pointer
int& r      r is a reference

new         allocate one dynamic object
delete      release one dynamic object

new[]       allocate dynamic array
delete[]    release dynamic array

.           access through object
->          access through pointer
::          belongs to class/scope

string      dynamically managed text
vector      dynamically managed array

struct      group related members into a type
enum        named set of choices
class       attributes + methods + access control

private     this class
protected   this class + derived classes
public      outside code can access
```

------------------------------------------------------------------------

## Source Scope Note

The core material above follows the uploaded CMP 220 lecture files:

-   `Pointers_references.pdf`
-   `Dynamic_memeory_mamagment.pdf`
-   `Lecture_strings_vectors (1).pdf`
-   `Lecture_struct_enum.pdf`
-   `Lecture5_Classes.pdf`

The `getline` / `cin.ignore` explanation and the detailed pointer form
for a built-in 2D array are standard C++ usage added to make the syntax
sheet complete; they are not presented as extracted lecture wording.
