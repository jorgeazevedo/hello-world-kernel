# Hello, world!

This is an example of a basic kernel module.

## Dependencies

Most of this package's dependencies are fullfilled by `build-essentials` and
getting the linux headers for your kernel version.

## Comnpilation

Just calling the rather standardized makefile is suficient.

    make

## Loading and Unloading it

To keep an eye on the kernel ring buffer, you can cat kmsg

    sudo cat /proc/kmsg

Loading the module can be done by

    sudo insmod hello.ko

Conversely, unloading is done by

    sudo rmmod hello

This should print something close to the following in the kernel ring buffer

    <4>[398767.984333] Hello world!
    <4>[398769.493268] Goodbye world!
