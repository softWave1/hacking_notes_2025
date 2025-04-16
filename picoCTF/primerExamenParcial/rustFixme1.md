# Rust fixme 1

# Description
Have you heard of Rust? Fix the syntax errors in this Rust file to print the flag! Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/3f0e13f541928f420d9c8c96b06d4dbf7b2fa18b15adbd457108e8c80a1f5883/fixme1.tar.gz).
# Solution
-  After downloading the file and decompress it there's a cargo project which is the rust package manager after trying to compile it and try to run it I found some issues that relay on the existence of syntax mistakes in the source code of the project.

``` bash
tree fixme1
fixme1
├── Cargo.lock
├── Cargo.toml
└── src
    └── main.rs
cd fixme1/
cargo run
Compiling rust_proj v0.1.0 (/home/jay/esC/fixme1)
error: expected `;`, found keyword `let`
 --> src/main.rs:5:37
  |
5 |     let key = String::from("CSUCKS") // How do we end statements in Rust?
  |                                     ^ help: add `;` here
...
8 |     let hex_values = ["41", "30", "20", "63", "4a", "45", "54", "76", "01", "1c", "7e", "59", "63", "e1", "61", "25", "7f", "...
  |     --- unexpected token

error: argument never used
  --> src/main.rs:26:9
   |
25 |         ":?", // How do we print out a variable in the println function? 
   |         ---- formatting specifier missing
26 |         String::from_utf8_lossy(&decrypted_buffer)
   |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ argument never used

error[E0425]: cannot find value `ret` in this scope
  --> src/main.rs:18:9
   |
18 |         ret; // How do we return in rust?
   |         ^^^ help: a local variable with a similar name exists: `res`

For more information about this error, try `rustc --explain E0425`.
error: could not compile `rust_proj` (bin "rust_proj") due to 3 previous errors
```

- Once I found the errors in the code I proceed to fix them.

```rust
use xor_cryptor::XORCryptor;

fn main() {
    // Key for decryption
    // Fix: An ending ;
    let key = String::from("CSUCKS"); // How do we end statements in Rust?

    // Encrypted flag values
    let hex_values = ["41", "30", "20", "63", "4a", "45", "54", "76", "01", "1c", "7e", "59", "63", "e1", "61", "25", "7f", "5a", "60", "50", "11", "38", "1f", "3a", "60", "e9", "62", "20", "0c", "e6", "50", "d3", "35"];

    // Convert the hexadecimal strings to bytes and collect them into a vector
    let encrypted_buffer: Vec<u8> = hex_values.iter()
        .map(|&hex| u8::from_str_radix(hex, 16).unwrap())
        .collect();

    // Create decrpytion object
    let res = XORCryptor::new(&key);
    if res.is_err() {
        //Fix: misspelling on the ruturn keyword
        return; // How do we return in rust?
    }
    let xrc = res.unwrap();

    // Decrypt flag and print it out
    let decrypted_buffer = xrc.decrypt_vec(encrypted_buffer);
    println!(
        //Fix: There wasn't curly brackets in the middle of the format {}
        "{:?}", // How do we print out a variable in the println function? 
        String::from_utf8_lossy(&decrypted_buffer)
    );
}
```

-  Once the code is free of errors I run the code and get the flag
```bash
cargo run
   Compiling rust_proj v0.1.0 (/home/jay/esC/fixme1)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.18s
     Running `target/debug/rust_proj`
"picoCTF{4r3_y0u_4_ru$t4c30n_n0w?}"
```
# References
- [The cargo book](https://doc.rust-lang.org/cargo/)
- [Introduction to rust](https://www.geeksforgeeks.org/introduction-to-rust-programming-language/)