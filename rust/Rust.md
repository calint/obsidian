## Learn By Examples
https://doc.rust-lang.org/stable/rust-by-example/
https://practice.course.rs/
https://fasterthanli.me/articles/a-half-hour-to-learn-rust

## Tools
https://github.com/Kobzol/cargo-wizard

## Utility Crates
https://docs.rs/slotmap/latest/slotmap/

## Interesting Articles
https://cglab.ca/%7Eabeinges/blah/too-many-lists/book/README.html
https://jacko.io/object_soup.html

## Bare-metal
https://docs.rust-embedded.org/embedonomicon/smallest-no-std.html
https://github.com/johnthagen/min-sized-rust
https://interrupt.memfault.com/blog/zero-to-main-rust-1
https://github.com/ch32-rs/ch32-hal
https://docs.rust-embedded.org/book/

## Kernel
https://os.phil-opp.com/minimal-rust-kernel/

## Game Programming
https://loglog.games/blog/leaving-rust-gamedev/ 
https://pragprog.com/titles/hwrust/hands-on-rust/

## SIMD
https://docs.rs/glam/latest/glam/

## Portals
https://docs.rs/glam/latest/glam/

## Local Manuals
 file:///home/c/.rustup/toolchains/nightly-x86_64-unknown-linux-gnu/share/doc/rust/html/core/index.html
 file:///home/c/.rustup/toolchains/nightly-x86_64-unknown-linux-gnu/share/doc/rust/html/book/index.html

## Lifetimes
* https://www.youtube.com/watch?v=HwupNf9iCJk
* *Interior Mutability*
* Cell: mutate reference of copy-able content
* RefCell: borrow checker at runtime, may panic, in multi-threaded application blocks
* RwLock: threads safe, one writer many readers
* Arc: threads safe reference count
* Mutex: simplified RwLock without concept of lock for read or write
