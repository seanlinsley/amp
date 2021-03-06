# Installation

Instructions to compile from source can be found below. If your OS isn't listed,
you'll need to follow the manual installation instructions and install the
specified dependencies (build dependencies can be removed after compilation,
if desired).

Adding support for your preferred distro is a great way to contribute to the
project!

## Arch Linux

Available via [AUR](https://aur.archlinux.org/packages/amp):

```bash
git clone https://aur.archlinux.org/amp.git
cd amp
makepkg -isr
```

## macOS

Available via [Homebrew](https://brew.sh):

```bash
brew tap jmacdonald/amp && brew install amp
```

## Manual installation

### Dependencies

* `git`
* `libxcb` (X11 clipboard support)

### Build Dependencies

* `cmake`
* `python`
* `rust`

### Building

1. Install Rust, either through your system's package manager or using [Rust's `rustup` toolchain management utility](https://www.rust-lang.org/en-US/install.html).
2. Ensure the aforementioned dependencies are installed.
2. Clone the repository:
    ```bash
    git clone https://github.com/jmacdonald/amp.git
    ```
3. Build
    ```bash
    cd amp
    cargo build --release
    ```
4. Add the `amp` release build directory to your path (use `~/.bashenv` if using `bash`):
    ```bash
    echo "export PATH=\"$(pwd)/target/release:\$PATH\"" >> ~/.zshenv
    ```
