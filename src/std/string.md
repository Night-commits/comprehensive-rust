# String

[`String`][1] is the standard heap-allocated growable UTF-8 string buffer:

```rust,editable
fn main() {
    let mut s1 = String::new();
    s1.push_str("Hello");
    println!("s1: len = {}, capacity = {}", s1.len(), s1.capacity());

    let mut s2 = String::with_capacity(s1.len() + 1);
    s2.push_str(&s1);
    s2.push('!');
    println!("s2: len = {}, capacity = {}", s2.len(), s2.capacity());
}
```

`String` implements [`Deref<Target = str>`][2], which means that you can call all
`str` methods on a `String`.

[1]: https://doc.rust-lang.org/std/string/struct.String.html
[2]: https://doc.rust-lang.org/std/string/struct.String.html#deref-methods-str
