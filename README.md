# test-mbedtls-dependency error

:~/Repos/test-mbedtls-dependency$ cargo build --target=x86_64-fortanix-unknown-sgx  
   Compiling yasna v0.2.2  
   Compiling rs-libc v0.1.0  
   Compiling libc v0.2.65  
   Compiling byteorder v1.3.2  
   Compiling bitflags v1.2.1  
   Compiling serde v1.0.101  
   Compiling mbedtls v0.4.0 (https://github.com/haraldh/rust-mbedtls?rev=8cd4a575dd41cbc6a545e7fbd10d6924c8275f66#8cd4a575)
   Compiling mbedtls-sys-auto v2.18.0 (https://github.com/haraldh/rust-mbedtls?rev=8cd4a575dd41cbc6a545e7fbd10d6924c8275f66#8cd4a575)  
error[E0432]: unresolved import `super::libc::FILE`  
  --> /home/enarxnuc/.cargo/git/checkouts/rust-mbedtls-9749fa8112dd1a19/8cd4a57/mbedtls-sys/src/types.rs:91:13  
   |  
91 |     pub use super::libc::FILE;  
   |             ^^^^^^^^^^^^^^^^^ no `FILE` in the root  

error[E0432]: unresolved imports `super::libc::time_t`, `super::libc::tm`  
  --> /home/enarxnuc/.cargo/git/checkouts/rust-mbedtls-9749fa8112dd1a19/8cd4a57/mbedtls-sys/src/types.rs:94:27  
   |  
94 |     pub use super::libc::{time_t, tm};  
   |                           ^^^^^^  ^^ no `tm` in the root  
   |                           |  
   |                           no `time_t` in the root  
   |                           help: a similar name exists in the module: `size_t`  

error: aborting due to 2 previous errors  

For more information about this error, try `rustc --explain E0432`.  
error: could not compile `mbedtls-sys-auto`.  

To learn more, run the command again with --verbose.  
