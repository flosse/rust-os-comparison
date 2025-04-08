# Rust OS comparison

A comparison of operating systems written in [Rust](https://rustlang.org).

There are several open source operating systems written in Rust.
Most of them are proofs of concepts.
The only system that goes a step further is **Redox**.
It comes with a window manager as well as basic applications like an
[editor](https://github.com/redox-os/sodium) and a file manager.
**Theseus** is approaching maturity with the ability to execute legacy components in a WASM sandboxed environment.

- **Redox**             ([repository](https://github.com/redox-os/redox) / [homepage](http://www.redox-os.org/))
- **Theseus OS**        ([repository](https://github.com/theseus-os/Theseus) / [homepage](https://www.theseus-os.com/))
- **Tock**              ([repository](https://github.com/helena-project/tock) / [homepage](http://www.tockos.org/))
- **intermezzOS**       ([repository](https://github.com/intermezzos/kernel) / [homepage](http://intermezzos.github.io/))
- **reenix**            ([repository](https://github.com/scialex/reenix))
- **rustboot**          ([repository](https://github.com/charliesome/rustboot))
- **RustOS**            ([repository](https://github.com/ryanra/RustOS))
- **QuiltOS**           ([repository](https://github.com/QuiltOS/QuiltOS))
- **Tifflin (rust_os)** ([repository](https://github.com/thepowersgang/rust_os))
- **bkernel**           ([repository](https://github.com/rasendubi/bkernel))
- **Quasar**            ([repository](https://github.com/LeoTestard/Quasar))
- **SOS**               ([repository](https://github.com/hawkw/sos-kernel))
- **MOROS**             ([repository](https://github.com/vinc/moros) / [homepage](http://moros.cc/))
- **Fexlix OS**         ([repository](https://github.com/mrgian/felix))
- **Aero**              ([repository](https://github.com/Andy-Python-Programmer/aero))
- **Hermit**            ([repository](https://github.com/hermitcore/rusty-hermit))
- **Asterinas**         ([repository](https://github.com/asterinas/asterina))


| Name            | Architectures     | Pure Rust | Active? | Kernel architecture          | Target              | Userpace? | Optional GUI? | Contributors | Filesystem              | License                    |
|-----------------|-------------------|-----------|---------|------------------------------|---------------------|-----------|---------------|--------------|-------------------------|----------------------------|
| **Redox**       | x86 and x86_64    | yes       | yes     | Microkernel                  | General purpose     | yes       | yes           | 60           | [ZFS]/[RedoxFS]/[FAT32] | MIT                        |
| **Theseus OS**  | x86_64, ARM WIP   | yes       | yes     | Safe-language SAS/SPL OS[^1] | General + Embedded  | N/A       | yes           | 25           | Custom/FAT32            | MIT                        |
| **Tock**        | Cortex M          |           | yes     |                              |                     |           | no            | 40           |                         | APL 2 / MIT                |
| **intermezzOS** | x86_64            | no        | yes     | ?                            | PoC                 | no        | no            | 18           | no                      | APL 2 / MIT                |
| **RustOS**      | i386              | ?         | yes     | None                         | PoC                 | no        | no            | 10           | no                      | APL 2 / MIT                |
| **rustboot**    | i386              | ?         | no      | None                         | PoC                 | no        | no            | 8            | no                      | MIT                        |
| **bkernel**     | ARM               | yes       | yes     | ?                            | Embedded devices    | no        | no            | 4            | ?                       | GPL with linking exception |
| **SOS**         | x86_64            | yes       | yes     | Microkernel                  | PoC                 | no        | no            | 3            | ?                       | MIT                        |
| **reenix**      | [Brown's CS167/9] | no        | no      | Monolithic (current state)   | PoC                 | no        | no            | 3            | ?                       | [unknown]                  |
| **Quasar**      | x86_64            | ?         | no      | ?                            | ?                   | no        | no            | 2            | ?                       | ?                          |
| **Tifflin**     | x86_64/amd64      | almost    | yes     | Monolithic                   | ?                   | ?         | yes           | 1            | ISO9660                 | 2-Clause-BSD               |
| **MOROS**       | x86_64            | yes       | yes     | Monolithic                   | General purpose     | limited   | no            | 1            | [MFS]                   | MIT                        |
| **Felix OS**    | x86_64            | yes       | yes     | ?                            | General purpose     | ?         | no            | 3            | [FAT16]  Read Only      | MIT                        |
| **Aero**        | x86_64            | ?         | yes     | Monolithic                   | General purpose     | ?         | yes           | 10           | ?                       | GPL                        |
| **Hermit**      | x86_64, aarch64   | yes       | yes     | Unikernel                    | Cloud and HPC       | no        | no            | >30          | virtiofs                | Apache, BSD                |
| **Embassy**     | many              | yes       | yes     | embedded framework           | embedded            | n/a       | no            | 388          | ?                       | APL2 / MIT / CC 4.0        |
| **Hubris**      | many              | yes       | yes     | message passing kernel       | embedded            | n/a       | no            | 50           | ?                       | MPL 2.0                    |
| **Asterinas**   | x86_64            |           | yes     | [Framekernel]                | General purpose     | ?         | ?             | 42           | ?                       | MPL 2.0                    |

Also worth noting: [Robigalia](https://gitlab.com/robigalia/sel4), a sel4 userspace, written in Rust.

[Brown's CS167/9]: http://cs.brown.edu/courses/cs167/
[ZFS]: https://github.com/redox-os/zfs
[RedoxFS]: https://github.com/redox-os/redoxfs
[FAT32]: https://github.com/deepaksirone/redox-loader
[unknown]: https://github.com/scialex/reenix/issues/1
[MFS]: https://github.com/vinc/moros/blob/trunk/doc/filesystem.md
[Framekernel]: https://asterinas.github.io/book/kernel/the-framekernel-architecture.html

[^1]: Theseus is a safe-language OS that runs all components within a [Single Address Space (SAS)](https://en.wikipedia.org/wiki/Single_address_space_operating_system) and Single Privilege Level (SPL).

## Blog posts and papers

-[Writing the second video game for the Micro:bit in Rust](https://hackernoon.com/writing-the-second-video-game-for-the-micro-bit-in-rust-3cd8b5ab22d3)

- Talking Tock Week
    - [5](http://www.tockos.org/blog/2016/talking-tock-5/),
    - [4](http://www.tockos.org/blog/2016/talking-tock-4/),
    - [3](http://www.tockos.org/blog/2016/talking-tock-3/),
    - [2](http://www.tockos.org/blog/2016/talking-tock-2/),
    - [1](http://www.tockos.org/blog/2016/talking-tock-1/)

- Theseus OS Documents
    - [Theseus OS Book](https://www.theseus-os.com/Theseus/book/index.html)
    - [Theseus OS Source Code Documentation](https://www.theseus-os.com/Theseus/doc/___Theseus_Crates___/index.html)
    - [Theseus OS Conference Publications](https://www.theseus-os.com/Theseus/book/misc/papers_presentations.html)
    - [Theseus OS source code on GitHub](https://github.com/theseus-os/Theseus)
    - [Theseus OS Technical Blog](https://www.theseus-os.com/)


- [FreeRTOS meets Rust](http://www.hashmismatch.net/freertos-meets-rust/)
- [Pragmatic Bare Metal Rust](http://www.hashmismatch.net/pragmatic-bare-metal-rust/)
- This week in intermezzOS:
  - [1](https://intermezzos.github.io/blog/articles/twii1/),
  - [2](https://intermezzos.github.io/blog/articles/twii2/),
  - [3](https://intermezzos.github.io/blog/articles/twii3/)

- [Writing an OS in Rust](http://os.phil-opp.com/)
    - [Returning from Exceptions](http://os.phil-opp.com/returning-from-exceptions.html)
    - [Allocating Frames](http://os.phil-opp.com/allocating-frames.html)
    - [Printing to Screen](http://os.phil-opp.com/printing-to-screen.html)
    - [Setup Rust](http://os.phil-opp.com/setup-rust.html)
    - [Entering Long Mode](http://os.phil-opp.com/entering-longmode.html)
    - [A minimal x86 kernel](http://blog.phil-opp.com/rust-os/multiboot-kernel.html)
    - [Remap the Kernel](http://os.phil-opp.com/remap-the-kernel.html)
    - [Kernel Heap](http://os.phil-opp.com/kernel-heap.html)

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
- [Betriebssystem Redox in Rust geschrieben](http://www.pro-linux.de/news/1/23383/betriebssystem-redox-in-rust-geschrieben.html) (German)

### Embedded Systems

- [Safer microcontrollers almost here](http://dylanmckay.io/blog/rust/avr/llvm/2017/02/09/safer-microcontrollers-almost-here.html)
- [Exploring ARM inline assembly in Rust](http://embed.rs/articles/2016/arm-inline-assembly-rust/)
- Bare Metal Rust
    - [3: Configure your PIC to handle interrupts correctly](http://www.randomhacks.net/2015/11/16/bare-metal-rust-configure-your-pic-interrupts/)
    - [2: Retarget your compiler so interrupts are not evil](http://www.randomhacks.net/2015/11/11/bare-metal-rust-custom-target-kernel-space/)
    - [1: Low-level CPU I/O ports](http://www.randomhacks.net/2015/11/09/bare-metal-rust-cpu-port-io/)
- [Rust bare metal on ARM microcontroller](http://antoinealb.net/programming/2015/05/01/rust-on-arm-microcontroller.html)
- [Blinking an LED with Rust on a Beaglebone Black](http://theotherandygrove.com/blinking-an-led-with-rust-on-a-beaglebone-black/)
- [Zinc goals redefined and extended](http://zinc.rs/blog/#/2014/07/14/zinc-goals/)
- Rust on an Arduino Uno
  - [Part 1](http://jakegoulding.com/blog/2016/01/02/rust-on-an-arduino-uno/)
  - [Part 2](http://jakegoulding.com/blog/2016/01/17/rust-on-an-arduino-uno-part-2/)
  - [Part 3](http://jakegoulding.com/blog/2016/01/24/rust-on-an-arduino-uno-part-3/)
  - [Part 4](http://jakegoulding.com/blog/2016/05/12/rust-on-an-arduino-uno-part-4/)
- [Rust on Arduino Due](http://de.slideshare.net/kellogh/glue-con14)
- http://embedded.hannobraun.de/
- [Raspberry Pi Bare Metal Programming with Rust](https://blog.thiago.me/raspberry-pi-bare-metal-programming-with-rust/)
- [Running Rust code on a BBC micro:bit micro-controller](https://github.com/SimonSapin/rust-on-bbc-microbit)
