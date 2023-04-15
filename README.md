This is a Rust program for testing out the
[`rustyline-async`](https://github.com/zyansheep/rustyline-async) crate —
specifically, whether it works on Windows, as [I experienced problems with more
advanced usage on that platform](https://github.com/jwodder/confab/issues/168).

Installation
============

Release Assets
--------------

Prebuilt binaries are available for the most common platforms.  The binaries
for the latest release of the code can be found on [the Releases
page](https://github.com/jwodder/rustyline-async-test/releases) under the
"Assets" header.

Compiling from Source
---------------------

In order to compile this program from source, you will need to first [install
Rust and Cargo](https://www.rust-lang.org/tools/install).

To install the `rustyline-async-test` binary in `~/.cargo/bin`, run:

    cargo install --git https://github.com/jwodder/rustyline-async-test

Alternatively, a binary localized to a clone of this repository can be built
with:

    git clone https://github.com/jwodder/rustyline-async-test
    cd rustyline-async-test
    cargo build  # or `cargo build --release` to enable optimizations
    # You can now run the binary with `cargo run` while in this repository.


Expected Behavior
=================

When `rustyline-async-test` is working properly, it will print out a `prompt>`
prompt.  Entering a line of text at this prompt will cause the program to
repeat it back to you and issue a new prompt.  For each second that passes
without pressing "Enter", a line reading "`Message received!`" will be output
above the prompt.  You can press the Up and Down arrow keys to go back through
previously-entered lines.  Entering "`quit`" quits the program.

![rustyline-async-test in action](recording.gif)
