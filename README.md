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

