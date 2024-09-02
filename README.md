# Installing Zig on macOS

## Intro

Hi! If you've got here, maybe you had the same journey that I did: follow the instuctions on the [Zig](https://ziglang.org) website for installing on macOS, only to discover that most Zig tutorials (like [Ziglings](https://codeberg.org/ziglings/exercises)) don't support the latest _stable_ version, but usually something closer to bleeding edge.

Well... this is what I did, and hopefully it helps.

## Installation

1. ### Download

    Head on over to the Zig [download page](https://ziglang.org/download/) and downloadt the appropriate file. If you're on an M-series processor, that is the `aarch64`, otherise `x86_64`.

1. ### Extract

    I have put my binary in my user's home folder, at `~/bin`. You might have to create the `bin` folder if you don't already have one.

    ```zsh
    tar -xzf ~/Downloads/zig-macos-aarch64-<version>.tar.xz -C ~/bin
    ```

3. ### Symlink

    This is optional, but it makes things easier in the future, such as for updating.

    ```zsh
    ln -s ~/bin/zig-macos-aarch64-<version>/zig ~/bin/zig
    ```

4. ### Add to Path

    If you chose to put your zig executable in the `~/bin` folder, and you have not already added that folder to your path, you will need to do that.

    ```zsh
    echo 'export PATH=$PATH:~/bin' >> ~/.zshrc
    ```

    then, apply the changes to your `.zshrc` to the current shell.

    ```zsh
    source ~/.zshrc
    ```

5. ### Test

    You should now be able to use Zig from your terminal:

    ```zsh
    zig version
    ```
