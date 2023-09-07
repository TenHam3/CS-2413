# CS-2413

## Pointers

Each declared variable is stored in the computer's memory at some address. A pointer is a variable which holds that address. Itself is a special "integer"

![image](https://github.com/TenHam3/CS-2413/assets/109705811/ae3e94f9-ee55-4c86-abf8-01f73b7e549d)

### Declare and Assign Pointer

![image](https://github.com/TenHam3/CS-2413/assets/109705811/7e97d309-c6c8-446e-bf47-000ce1ec302f)

![image](https://github.com/TenHam3/CS-2413/assets/109705811/4588bf7c-86da-4b25-ad1b-2566ba2eebf3)

### Access Data through Pointer

![image](https://github.com/TenHam3/CS-2413/assets/109705811/ec24d0fe-e871-47f0-a492-78873b132aae)

- The * operator is a dereference operator that lets you access the data at the address the pointer points at

![image](https://github.com/TenHam3/CS-2413/assets/109705811/8acc5fbc-e70d-4bf4-80f6-210e84368070)

- Modifying data through a pointer also modifies the same data pointed at by any variable pointing to what the pointer points to

- Incrementing a pointer increments the address by however many bytes it takes to store what the pointer points to
    - Incrementing comes before dereferencing a pointer

### Access Array through Pointer

![image](https://github.com/TenHam3/CS-2413/assets/109705811/4a9b53df-e920-4da3-974f-79fcf871d405)

![image](https://github.com/TenHam3/CS-2413/assets/109705811/14905e08-f435-46b3-bac3-99feb31b275d)

![image](https://github.com/TenHam3/CS-2413/assets/109705811/464a3d0f-5e25-414f-b2b0-d24b0ec48427)

### Pass Variable to Function through Pointer

![image](https://github.com/TenHam3/CS-2413/assets/109705811/c3a08500-a32e-434e-88cf-51f96ee2bd55)

![image](https://github.com/TenHam3/CS-2413/assets/109705811/f8f4aea6-a9ab-4ec4-98e5-23e407452e72)

![image](https://github.com/TenHam3/CS-2413/assets/109705811/49d51759-6ad0-4699-9962-fd1f3f6c5f31)

#### Pass Array to Function through Pointer

![image](https://github.com/TenHam3/CS-2413/assets/109705811/5eb2f0c1-3fbb-466e-9e04-c1ab8459d318)

![image](https://github.com/TenHam3/CS-2413/assets/109705811/080fede9-13a2-46ec-ae4d-d3912dcd8965)

![image](https://github.com/TenHam3/CS-2413/assets/109705811/2877e471-8011-4151-a5ed-08ad32ebf972)

### Pointer and Class Object

![image](https://github.com/TenHam3/CS-2413/assets/109705811/e522050c-79ac-41f9-8144-d0a69fa4ceab)

- If you want to access class members through a pointer, you have to use the "->" operator
- Accessing members through an object uses the "." operator

![image](https://github.com/TenHam3/CS-2413/assets/109705811/6b92ba3f-0484-48e0-b133-bd93451ee29c)

## Dynamic Memory Allocation and Vectors in C++

### Memory Allocation

#### Static Memory Allocation

When variables are declared in a program (based on regular syntaxes), a set of memory chunks are allocated for them at the compile time, before the program runs. These chunks are also fixed when the program runs.

This partly explains why the array size must be specified during declaration, since the number of memory chunks must be fixed at compile time. Not allowed to specify array size when the program runs.

#### Dynamic Memory Allocation

C++ reserves a large blocks of memory called free store or heap, which can be dynamically allocated (for new variables) when the program runs. It is crucial to hold the address of this chunk using a pointer so we can access it in the future. You can use and perform operations on the pointer in the same way as statically allocated chunks.

Dynamically allocated memory can be deleted when the program runs, to free space for new allocations. "delete" really means "free" so this chunk of memory can be overwritten for other purposes. 
- delete p; means to free the allocated space (at the address in "p"). After that, no data can be retrieved through "p"

"delete" can only be used to free dynamically allocated space. Statically allocated space cannot be freed manually. It is automatically freed when its program (or function) lifecycle ends. Dynamically allocated memory (even if declared locally) stays in heap forever, until freed by "delete" or main program ends. If not deleted properly, they can quickly take up heap and cause memory leak. Need to free a dynamically allocated chunk before its current pointer is reassigned because you will lose track of the dynamically allocated space and cannot access it again, thus not being able to be freed and causing a memory leak. Otherwise, we will lose track of this chunk adn it will stay in the heap forever (until main dies). We can also dynamically allocate consecutive chunks for an array. Used in the same way as statically allocated space for an array. Delete using "delete []" followed by the array name.

### Vector

A vector is an array-like abstract data type that supports operations like size, empty, set, erase, etc. You have to include the vector library to use vectors. All entries are auto-initialized to zero.

![image](https://github.com/TenHam3/CS-2413/assets/109705811/c9954f1f-c818-4bdd-b469-5692e617e408)

- Method 2 specifies the size first, then the shared values so vector y would have 4 elements, each of which have the value 2

The resize() function resizes the vector. Two scenarios:
1. If the original vector is shorter,a ppend 0's to its tail
2. If the original vector is longer, remove last entries
The size() function returns the vector size. You can use the "." operator to access member functions of the vectors, treating it as an object.

Push_back() adds an element to the end of the vector. This increases the size by 1. Pop_back() removes the last element from the end of teh vector. This reduces size by 1. We can add an element to a position that is outside the vector. This will automatically increase vector size to the position, and fill other added positions with zeros.

We can directly assign values to a declared vector ( not allowed in array). If the assigned value number differs from the vector size, vector size will automatically adapt to that number. We can also directly assign a vector to another vector (not allowed in arrays) even if they have different dimensions. This creates a copy of the input vector. 

#### Iterator

An iterator to a vector is like ap ointer to array. It holds the address of the vector (element). 

#### Insert and Erase

The insert() function inserts a new value into a vector at a specific poisiton (described by an iterator). Old elements on or after this position are all shifted backwards. The erase() function removes an existing element at a specific position. 

## Linked List

A linked list is an ADT that links a set of objects to form a list (looks like a virtual array). Importantly, these objects can be separately stored in the memory fragments, improving efficiency of memory usage.

We can travel from one node to another through directional links (and only through these links). We will stick to the understanding that all links are directional (a bidirectional link = two directed links)

![image](https://github.com/TenHam3/CS-2413/assets/109705811/7c5a5e00-f042-49d5-b85f-ac6fbb6b9ccf)

### Basic Operations

- Traverse: travel from head to tail (base).
- Enumerate: enumerate all elements in the list
- Size: count the number of elements in the list
- Find: find an element in the list
- Insert: add an element to the list
- Remove: remove an element from the list
- Clear: remove all elements in the list

You need an iterator to access nodes. Iterators are similar to pointers in that you can use the * operator to access the data that the iterator is pointing at. 

![image](https://github.com/TenHam3/CS-2413/assets/109705811/93911b0c-da7a-4415-bd82-d5f1559c5fd3)

