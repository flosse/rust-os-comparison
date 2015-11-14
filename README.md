# Rust OS comparison

A comparison of operating systems written in [Rust](https://rustlang.org).

At the moment there are four open source OS:

- **redox**    ([repository](https://github.com/redox-os/redox) / [homepage](http://www.redox-os.org/))
- **reenix**   ([repository](https://github.com/scialex/reenix))
- **rustboot** ([repository](https://github.com/charliesome/rustboot))
- **Tifflin (rust_os)**  ([repository](https://github.com/thepowersgang/rust_os))


|                         Name | redox | reenix                                                | rustboot | Tifflin      |
| ---------------------------- | ----- |------------------------------------------------------ | -------- | ------------ |
|                  **License** | MIT   | [unknown](https://github.com/scialex/reenix/issues/1) | MIT      | 2-Clause-BSD |
|            **Architectures** | x86   | [Brown's CS167/9](http://cs.brown.edu/courses/cs167/) | i368     | x86_64/amd64 |
| **Pure Rust implementation** | yes   | no                                                    | ?        | *almost*     |
|                      **GUI** | yes   | no                                                    | no       | yes          |
|               **VirtualBox** | yes   | no                                                    | no       | ?            |
|                     **Qemu** | yes   | yes                                                   | yes      | yes          |


## Blog posts and papers

- [A minimal x86 kernel](http://blog.phil-opp.com/rust-os/multiboot-kernel.html)
- [This Week in Redox 1](http://www.redox-os.org/news/this-week-in-redox-1/)
- [Redox is Serious](http://dictator.redox-os.org/index.php?controller=post&action=view&id_post=17)
- [Rust bare metal on ARM microcontroller](http://antoinealb.net/programming/2015/05/01/rust-on-arm-microcontroller.html)
- [Reenix: Implementing a Unix-Like Operating System in Rust](https://scialex.github.io/reenix.pdf) (PDF)
- [Experiences Building an OS in Rust](https://mostlytyped.com/posts/experiences-building-an-os-in-ru)
- [Writing an OS in Rust in tiny steps (Steps 1-5)](http://jvns.ca/blog/2014/03/12/the-rust-os-story/)
- [My Rust OS will never be finished (and it's a success!)](http://jvns.ca/blog/2014/03/21/my-rust-os-will-never-be-finished/)
- [Ownership is Theft: Experiences Building an Embedded OS in Rust](http://amitlevy.com/papers/tock-plos2015.pdf) (PDF)
- [Using Rust for an Undergraduate OS Course](http://rust-class.org/0/pages/using-rust-for-an-undergraduate-os-course.html)
- [Bare Metal Rust: Low-level CPU I/O ports](http://www.randomhacks.net/2015/11/09/bare-metal-rust-cpu-port-io/)
- [Bare Metal Rust 2: Retarget your compiler so interrupts are not evil](http://www.randomhacks.net/2015/11/11/bare-metal-rust-custom-target-kernel-space/)
