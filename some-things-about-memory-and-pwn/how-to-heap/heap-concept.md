# Heap Concept

### Freelist

List memory block free for use, when a new malloc request comes in, it searches the freelist to reuse the freed memory blocks.

### Arena

Is an internal memory management space in a memory allocation library such as glibc. In a multithreaded program, each thread can be assigned a separate arena to perform memory allocation and deallocation operations, to minimize conflicts and increase performance.

### Arenas

In multithreaded environments, memory managers (such as glibc's ptmalloc) use the concept of arenas to divide the heap into smaller chunks, each of which can be assigned to one or more threads. This reduces conflict and increases performance when multiple threads allocate or deallocate memory.

### Glibc

The glibc package _contains standard libraries which are used by multiple programs on the system_.

###
