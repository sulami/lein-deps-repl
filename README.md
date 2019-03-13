# Lein Deps REPL

Sometimes you just want to try out a library in a REPL, but throwing up a
Leiningen project or even a `deps.edn` file is so cumbersome. Leiningen can load
in dependencies per invocation, but the syntax is quite convoluted, so I wrote
this simple bash wrapper to be able to pull in one or more libraries and start a
REPL with them.

## Usage

```bash
./lein-deps-repl '[criterium "0.4.4"]'
```

The REPL defaults to
[rebel-readline](https://github.com/bhauman/rebel-readline), which I find much
better for quick exploration of a library, but it can be changed like this:

```bash
# default repl command
REPL_COMMAND=repl ./lein-deps-repl '[criterium "0.4.4"]'
```
