# Memory allocation function
It is a small file with malloc, free, calloc and realloc implementations.

## Compile and Run

`gcc -o memalloc.so -fPIC -shared memalloc.c`

The -fPIC and -shared options makes sure the compiled output has position-independent code and tells the linker to produce a shared object suitable for dynamic linking.

`export LD_PRELOAD=$PWD/memalloc.so`

And now you can use our functions instead of system ones.

You can do `unset LD_PRELOAD` to stop using our allocator.