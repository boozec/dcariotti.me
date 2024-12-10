---
title: first code in Rust
date: 2020-04-13
---

Today, I woke up with a thought: learn Rust. I bought a book about 3 months ago and started to read it, browse code on GitHub, etc., but I never wrote any code myself.

After 1 hour (yeah, I suck), I implemented a Fibonacci sequence. I think I used every Rust tip I could remember, but I'm not entirely sure.

<img src="https://media.tenor.com/images/b58a6eb5e09d1c9d99151d90db671217/tenor.gif" alt="kinda suck" class="center">

---

This is the bad code I wrote, but I'm very proud of it.

```rust
use std::mem;

fn fib(n: &mut i32) -> i32 {
    let mut a = 1;
    let mut b = 1;
    while *n > 1 {
        a += b;
        mem::swap(&mut a, &mut b);
        *n -= 1;
    }

    b
}
```

<p>This prints the first <span>\(N\)</span> numbers from the Fibonacci sequence.</p>

```rust
println!("{}", fib(&mut N));
```

Maybe one day, I'll look at this code and think: "WTF is that?!".
<img src="https://media.tenor.com/images/a8db208ebc4a1cfb5390c26e676c34de/tenor.gif" alt="wtf" class="center">
