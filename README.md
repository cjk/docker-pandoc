# CjK’s pandoc Docker configuration

A simple docker image for pandoc with filters, fonts, and the latex bazaar.

## How To

Run `cjk/pandoc`  With regular `pandoc` args. Mount your files at `/pandoc`.

``` console
$ docker run --rm -v ${PWD}:/pandoc cjk/pandoc README.md
```

Tip: use a shell alias to use `pandoc` just like `pandoc`. Add this to your `~/.bashrc` :

``` console
$ alias pandoc="docker run --rm -v `pwd`:/pandoc cjk/pandoc"
$ pandoc document.md
```

## Build it

Use `Makefile` or `docker` client:

```
make
```

or

```
docker build .
```
