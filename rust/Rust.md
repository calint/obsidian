## Learn By Examples
https://doc.rust-lang.org/stable/rust-by-example/  
https://practice.course.rs/  
https://fasterthanli.me/articles/a-half-hour-to-learn-rust  

## Tools
https://github.com/Kobzol/cargo-wizard  
Cargo subcommand that applies [profile](https://doc.rust-lang.org/cargo/reference/profiles.html) and [config](https://doc.rust-lang.org/cargo/reference/config.html#configuration-format) templates to your Cargo project to configure it for maximum performance, fast compile times or minimal binary size.  

https://www.youtube.com/watch?v=qY9j4dRaMjU  
**Make iterators 10X better with itertools**  

https://github.com/cordx56/rustowl/  
Visualize ownership and lifetimes in Rust for debugging and optimization  

## Utility Crates
https://docs.rs/slotmap/latest/slotmap/  

https://www.youtube.com/watch?v=FPRH66r-zUQ  
**Top 10 Rust crates you must know**
* log
* chrono

## Cargo Plugins
https://www.youtube.com/watch?v=T7JBLghJtNU  
**MUST know Rust Cargo plugins**
* cargo-tarpaulin: test coverage for x86 on Linux

## Conditional compilation
https://www.youtube.com/watch?v=QkHhwYJaP0U  
**Conditional Compilation with Cargo Features**

## Interesting Articles
https://cglab.ca/%7Eabeinges/blah/too-many-lists/book/README.html  
https://jacko.io/object_soup.html  

## Bare-metal
https://docs.rust-embedded.org/embedonomicon/smallest-no-std.html  
https://github.com/johnthagen/min-sized-rust  
https://interrupt.memfault.com/blog/zero-to-main-rust-1  
https://github.com/ch32-rs/ch32-hal  
https://docs.rust-embedded.org/book/  
https://embassy.dev/  
https://www.youtube.com/watch?v=MxUSSunT-yk&list=PLxM2CWwQlzBu9-UHsaxnQpc0YweGwKwn3  on Raspberry PI  

## Kernel
https://os.phil-opp.com/minimal-rust-kernel/  

## Game Programming
https://loglog.games/blog/leaving-rust-gamedev/  
https://pragprog.com/titles/hwrust/hands-on-rust/    

## SIMD
https://docs.rs/glam/latest/glam/  

# Parallelism
https://www.youtube.com/watch?v=YxG7PhZ3fb4  
* rayon
* does not support communication between threads as of v1.6.1

https://www.youtube.com/watch?v=FE1BkKqYCGU  
**Concurrency in Rust - Message Passing**
* `std::sync::mpsc`: multi-producer single consumer of messages
## Local Manuals
 file:///home/c/.rustup/toolchains/nightly-x86_64-unknown-linux-gnu/share/doc/rust/html/core/index.html  
 file:///home/c/.rustup/toolchains/nightly-x86_64-unknown-linux-gnu/share/doc/rust/html/book/index.html  

## Lifetimes
https://www.youtube.com/watch?v=juIINGuZyBc  
**Rust Lifetimes Finally Explained!**
* Functions with input/output references: Rust analyzes argument lifetimes to determine return reference validity. Since functions only receive inputs, return references must derive from input reference lifetimes. At call sites, Rust infers return reference validity by selecting the shortest input lifetime. For single reference arguments returning references, Rust implicitly assigns identical lifetimes. When self is referenced, all outputs inherit self's lifetime. (The question remains: what happens if an input reference's scope terminates before self's?)
* Regarding structs that contain refs: Lifetime of refs must be valid at least as long as the lifetime of the struct instance.

https://www.youtube.com/watch?v=HwupNf9iCJk  
**Interior Mutability**
* Cell: not thread-safe, mutate reference of copy-able content  
* RefCell: not thread-safe, borrow checker at runtime, may panic
* RwLock: thread-safe, one writer many readers  
* Arc: thread-safe, reference count  
* Mutex: thread-safe, simplified RwLock without concept of lock for multiple readers or one write  

https://www.youtube.com/watch?v=6fwDwJodJrg  
**Rust's second most complicated feature explained**
* examine: `fn fow() -> for<a'> impl Fn(&'a str) -> String`  

# Closures
https://www.youtube.com/watch?v=rnxutl7t1hI  
**Advanced Function and Closures in Rust**
* Fn: captures variables as immutable
* FnMut: captures variables as mutable
* FnOnce: transfers ownership of variables

# Traits
https://www.youtube.com/watch?v=Nzclc6MswaI  
**5 traits your types must implement**
* in a public crate: `Debug, Clone, Default, PartialEq, Send & Sync`
	* `Send`: type safe to send between  threads  
	* `Sync`: Safe to be shared via threads through references  
	* `Send + Sync` are "autotraits" implemented unless type contains a field that is not:
		`!Send` and `!Sync` (Negative Trait Bounds): The key here is the use of the `!` (exclamation mark) before the trait. This signifies a _negative trait bound_. It explicitly states that the type `Rc<T>` _does not_ implement the `Send` and `Sync` traits for any type `T`.
* additional  `PartialOrd, Hash, Eq, Ord`  
* additional optionals `Serialize + Deserialize` from `serde` crate
* note: also demonstrates `feature` declaration and conditional compilation

https://www.youtube.com/watch?v=ReBmm0eJg6g  
**Using Trait Objects in Rust**
* trait methods may not return `self` or have generic parameters

# Smart Pointers
https://www.youtube.com/watch?v=dYEC6NElVOg  
**Smart Pointers in Rust - The Deref Trait**
* `Deref`, `DerefMut`
* example: `Box<String> -> deref -> &String -> deref -> &str`

https://www.youtube.com/watch?v=RPWZcTYBS4k  
**Smart Pointers in Rust - The Drop Trait**
* implement `Drop` trait to hook when Rust drops a value
* explicit call to drop not allowed i.e. `v.drop()`, use `drop(v)`

https://www.youtube.com/watch?v=M9Owp3iLigg  
**Smart Pointers in Rust - Reference Counting**
* `Rc`: reference counter for single threaded use
* `Rc::clone(&Rc)` (convention) or `rcv.clone()`: increments reference counter
* `Weak` a type of `Rc` that does not imply ownership. example leaf -> parent. `upgrade` and `downgrade` to switch between types

# Iterators
* `iter_mut()` mutable references
* `into_iter()` takes ownership

# Dynamic  Dispatch
https://www.youtube.com/watch?v=wU8hQvU8aKM  
**Two Ways To Do Dynamic Dispatch**
* Rust vs C++ way of doing dynamic dispatch

# Macros
https://www.youtube.com/watch?v=SMCRQj9Hbx8  
**Comprehending Proc Macros**  
# Books
* https://doc.rust-lang.org/rust-by-example  
* https://doc.rust-lang.org/book/
* https://doc.rust-lang.org/embedded-book/
* https://rust-cli.github.io/book/
* https://rustwasm.github.io/docs/book/
* https://doc.rust-lang.org/cargo/
* https://rust-for-rustaceans.com/
* https://github.com/sger/RustBooks

## Portals
* https://docs.rs/glam/latest/glam/  
* https://letsgetrusty.kartra.com/page/XDk8  

# Docker
https://www.youtube.com/watch?v=_gMzg77Qjm0  
**Deploy your Rust project in 20 minutes**

# ADT
Algebraic Data Types
*TypeA | TypeB: "sum" => Enum
TypeA + TypeB: "product" => struct

# Etc
* "orphan rules": cannot implement a foreign trait of a foreign type
* `mem::take(...)`: move a value out of a mutable reference, even if the type `T` is not `Copy`
* `Box(X)` can automatically be converted to `&X` when passed as function arguments
* receive array slice instead of `&Vec` and function argument works for arrays also
* function arguments `impl Printer` vs `dyn Printer`: `impl` is same as generic argument `fn f<T>(x: &T) where T: Printer`. `impl` often used in return type meaning "something that implements xxx". `impl` is  a more modern way where it can be applied.

