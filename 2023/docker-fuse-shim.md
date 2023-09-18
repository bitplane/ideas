# FUSE shim for Docker

Could this work to get custom mounts working?!

```C
#define _GNU_SOURCE
#include <dlfcn.h>
#include <stdio.h>

int open(const char *pathname, int flags) {
    // Custom FUSE logic here
    
    ...

    // Call the original libc open
    int (*original_open)(const char*, int);
    original_open = dlsym(RTLD_NEXT, "open");
    return original_open(pathname, flags);
}
```

```bash
gcc -shared -fPIC my_fuse_shim.c -o my_fuse_shim.so -ldl
LD_PRELOAD=./my_fuse_shim.so your_program
```


