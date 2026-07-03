# man2html

Convert manpages to HTML documents.

## Usage

Just a short version of this:

```sh
zcat /data/data/com.termux/files/usr/share/man/man1/cmake.1.gz | groff -mandoc -Thtml > cmake-man.html
```

To find out man page paths use `whereis` command:

```sh
$ whereis cmake

cmake: /data/data/com.termux/files/usr/bin/cmake /data/data/com.termux/files/usr/share/man/man1/cmake.1.gz
```

`man2html` takes the name of a manpage as an argument, so you don't need to specify the manpage by its path.

```
$ man2html termux
```

`man2html` allways outputs to stdout. You can save the generated html page using output redirection in your shell, like this:
```
$ man2html termux > termux_manpage.html
```

## Installation

Copy the script somewhere in your $PATH. Clone or download .zip manually.

```
git clone "https://gitea.dmz.rs/disu1950/man2html"
cd man2html
cp man2html /data/data/com.termux/files/home/.local/bin
chmod +x /data/data/com.termux/files/home/.local/bin/man2html
```

## License

This project is licensed under the WTF Public License, version 3.
