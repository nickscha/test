# test
A C89 standard compliant, single header, nostdlib (no C Standard Library) simple testing framework.

For more information please look at the "test.h" file or take a look at the "examples" or "tests" folder.

## Quick Start

Download or clone test.h and include it in your project.

```C
#include "test.h"

int main() {

    /* Use assert to break/stop program when expression is not met*/
    assert(1 == 1);

    /* Use test as an conditional expression. If it fails it will log out the result but the program will continue */
    test(10 % 5 == 0);

    return 0;
}
```

## Run Example: nostdlib, freestsanding

In this repo you will find the "examples/test_win32_nostdlib.c" with the corresponding "build.bat" file which
creates an executable only linked to "kernel32" and "user32" and is not using the C standard library and executes the program afterwards.
