## Interfacing Rust from Python

lib.rs
<pre>
extern crate libc;

#[no_mangle]
pub extern fn double(x: i32) -> i32{
    x * 2
}

</pre>

Cargo.toml
<pre>
[package]
name = "python_rust"
version = "0.1.0"

[lib]
name = "lib"
crate-type = ["dylib"]

[dependencies]
libc = "0.2.0"
</pre>
main.py
<pre>
from cffi import FFI

ffi = FFI()
ffi.cdef("""
    int double(int);
""")

C = ffi.dlopen(".\\target\\release\\lib.dll")

print C.double(3)
C.process(1000)
</pre>