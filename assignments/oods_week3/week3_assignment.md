# Week 3 Challenge

1. A class called Pair has already been declared, but the constructors have not been implemented yet. Pair has two public member variables:

```c++
int *pa, *pb;
```

These two "pointers to int" are inteded to point to heap memory locations that store integeres. The remaineder of the Pair class expects the following functionality.

- A single constructor Pair(int a, int b): This should set up pa and pb to point to newly allocated memory locations on the heap. The integers at those memory locations should be assigned values according to the constructor's integer arguments a and b.

- A copy constructor Pair(const Pair& other): This takes as its argument a read-only reference to another Pair. It should set up the newly constructed Pair as a "deep copy", that is, it should create a new Pair that is equivalent to the other Pair based on de-referenced values but does not reuse any of the same memory locations. In other words, the copy constructor should set up its own instance's member variables pa and pb to point to newly allocated memory locations for integers on the heap; those memory locations must be new, not the same locations pointed to by the other Pair, but the integers at these new locations should be assigned values according to the integers that the other Pair is pointing to.

- A destructor ~Pair() that de-allocates all of the heap memory that had previously been allocated for this Pair's members.

The types of these member functions have already been declared in the declaration of Pair. Now you need to provide the implementation of each of thsee three member functions.

(Note: The function declarations shown in the code comment below do not include parameter names for the arguments. They show only the types of the arguments. This is allowed for a declaration, but when you define the implementation of those functions, you should give names to the parameters so that you can refer to them.)

```c++
/* Class Pair has already been declared
 * as shown in the following comments:
 *
 * class Pair {
 * public:
 *   int *pa,*pb;
 *   Pair(int, int);
 *   Pair(const Pair &);
 *  ~Pair();
 * };
 *
 * Implement its member functions below.
 */



 /* Here is a main() function you can use
  * to check your implementation of the
  * class Pair member functions.
  */

int main() {
  Pair p(15,16);
  Pair q(p);
  Pair *hp = new Pair(23,42);
  delete hp;

  std::cout << "If this message is printed,"
    << " at least the program hasn't crashed yet!\n"
    << "But you may want to print other diagnostic messages too." << std::endl;
  return 0;
}
```
