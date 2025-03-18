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

## "nostdlib" Motivation & Purpose

nostdlib is a lightweight, minimalistic approach to C development that removes dependencies on the standard library. The motivation behind this project is to provide developers with greater control over their code by eliminating unnecessary overhead, reducing binary size, and enabling deployment in resource-constrained environments.

Many modern development environments rely heavily on the standard library, which, while convenient, introduces unnecessary bloat, security risks, and unpredictable dependencies. nostdlib aims to give developers fine-grained control over memory management, execution flow, and system calls by working directly with the underlying platform.

### Benefits

#### Minimal overhead
By removing the standard library, nostdlib significantly reduces runtime overhead, allowing for faster execution and smaller binary sizes.

#### Increased security
Standard libraries often include unnecessary functions that increase the attack surface of an application. nostdlib mitigates security risks by removing unused and potentially vulnerable components.

#### Reduced binary size
Without linking to the standard library, binaries are smaller, making them ideal for embedded systems, bootloaders, and operating systems where storage is limited.

#### Enhanced performance
Direct control over system calls and memory management leads to performance gains by eliminating abstraction layers imposed by standard libraries.

#### Better portability
By relying only on fundamental system interfaces, nostdlib allows for easier porting across different platforms without worrying about standard library availability.
