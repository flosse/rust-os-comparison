# Rust OS comparison

A comparison of operating systems written in [Rust](https://rustlang.org).

There are several open source operating systems written in Rust.
Most of them are proofs of concepts.
The only system that goes a step further is **redox**.
It comes with a window manager as well as basic applications like an
[editor](https://github.com/redox-os/sodium) and a file manager.

- **redox**             ([repository](https://github.com/redox-os/redox) / [homepage](http://www.redox-os.org/))
- **reenix**            ([repository](https://github.com/scialex/reenix))
- **rustboot**          ([repository](https://github.com/charliesome/rustboot))
- **RustOS**            ([repository](https://github.com/ryanra/RustOS))
- **Tifflin (rust_os)** ([repository](https://github.com/thepowersgang/rust_os))
- **bkernel**           ([repository](https://github.com/rasendubi/bkernel))
- **intermezzOS**       ([repository](https://github.com/intermezzos/kernel) / [homepage](http://intermezzos.github.io/))
- **Quasar**            ([repository](https://github.com/LeoTestard/Quasar))


|                         Name | redox | reenix                                                | rustboot | RustOS       | Tifflin      | bkernel                    | intermezzOS | Quasar      |
| ---------------------------- | ----- |------------------------------------------------------ | -------- | --------     | ------------ | -------------------------- | ------------| ------------|
|                  **License** | MIT   | [unknown](https://github.com/scialex/reenix/issues/1) | MIT      | APL 2 / MIT  | 2-Clause-BSD | GPL with linking exception | APL 2 / MIT | ?           |
|            **Architectures** | x86   | [Brown's CS167/9](http://cs.brown.edu/courses/cs167/) | i386     | i386         | x86_64/amd64 | ARM                        | x86_64      | x86_64      |
| **Pure Rust implementation** | yes   | no                                                    | ?        | ?            | *almost*     | yes                        | no          | ?           |
|                      **GUI** | yes   | no                                                    | no       | no           | yes          | no                         | no          | no          |
|               **VirtualBox** | yes   | no                                                    | no       | no           | ?            | no                         | no          | no          |
|                     **Qemu** | yes   | yes                                                   | yes      | yes          | yes          | no                         | yes         | yes         |
|             **Contributors** | 29    | 3                                                     | 9        | 10           | 1            | 3                          | 4           | 1           |


## Blog posts and papers

- [Writing an OS in Rust](http://os.phil-opp.com/)
    - [Allocating Frames](http://os.phil-opp.com/allocating-frames.html)
    - [Printing to Screen](http://os.phil-opp.com/printing-to-screen.html)
    - [Setup Rust](http://os.phil-opp.com/setup-rust.html)
    - [Entering Long Mode](http://os.phil-opp.com/entering-longmode.html)
    - [A minimal x86 kernel](http://blog.phil-opp.com/rust-os/multiboot-kernel.html)
    - [Remap the Kernel](http://os.phil-opp.com/remap-the-kernel.html)
- [This Week in Redox 1](http://www.redox-os.org/news/this-week-in-redox-1/) / [Redox News](http://www.redox-os.org/news/)
- [Redox is Serious](http://dictator.redox-os.org/index.php?controller=post&action=view&id_post=17)
- [Reenix: Implementing a Unix-Like Operating System in Rust](https://scialex.github.io/reenix.pdf) (PDF)
- [Experiences Building an OS in Rust](https://mostlytyped.com/posts/experiences-building-an-os-in-ru)
- [Writing an OS in Rust in tiny steps (Steps 1-5)](http://jvns.ca/blog/2014/03/12/the-rust-os-story/)
- [My Rust OS will never be finished (and it's a success!)](http://jvns.ca/blog/2014/03/21/my-rust-os-will-never-be-finished/)
- [Ownership is Theft: Experiences Building an Embedded OS in Rust](http://amitlevy.com/papers/tock-plos2015.pdf) (PDF)
- [Using Rust for an Undergraduate OS Course](http://rust-class.org/0/pages/using-rust-for-an-undergraduate-os-course.html)
- [Running Rust on the Rumprun unikernel](https://gandro.github.io/2015/09/27/rust-on-rumprun/)
- [Making Popcorn: Adding a disk to a Rust Rumprun Unikernel](https://polyfractal.com/post/adding-a-disk-to-a-rust-rumprun-unikernel/)
- [bkernel: a Rust Operating System](http://www.alexeyshmalko.com/2015/bkernel-a-rust-operating-system/)
- [(x86_64) Why are platform features such as the red zone enabled by default?](https://internals.rust-lang.org/t/x86-64-why-are-platform-features-such-as-the-red-zone-enabled-by-default/)
- [Operating system development wiki](https://github.com/rust-lang/rust-wiki-backup/blob/master/Operating-system-development.md)
- [Create a secure POSIX-compatible userland on top of seL4](https://robigalia.org/)

### Embedded Systems

- Bare Metal Rust
    - [3: Configure your PIC to handle interrupts correctly](http://www.randomhacks.net/2015/11/16/bare-metal-rust-configure-your-pic-interrupts/)
    - [2: Retarget your compiler so interrupts are not evil](http://www.randomhacks.net/2015/11/11/bare-metal-rust-custom-target-kernel-space/)
    - [1: Low-level CPU I/O ports](http://www.randomhacks.net/2015/11/09/bare-metal-rust-cpu-port-io/)
- [Rust bare metal on ARM microcontroller](http://antoinealb.net/programming/2015/05/01/rust-on-arm-microcontroller.html)
- [Blinking an LED with Rust on a Beaglebone Black](http://theotherandygrove.com/blinking-an-led-with-rust-on-a-beaglebone-black/)
- [Zinc goals redefined and extended](http://zinc.rs/blog/#/2014/07/14/zinc-goals/)
- [Rust on an Arduino Uno](http://jakegoulding.com/blog/2016/01/02/rust-on-an-arduino-uno/)
- [Rust on Arduino Due](http://de.slideshare.net/kellogh/glue-con14)
- [Raspberry Pi Bare Metal Programming with Rust](https://blog.thiago.me/raspberry-pi-bare-metal-programming-with-rust/)
