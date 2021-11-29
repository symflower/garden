# Garden

These are binaries, packages and scripts that we made to help us build all our [products](https://get.symflower.com). We hope that you can use them for your projects too.

Please feel free to add issues [to the issue tracker](https://github.com/symflower/garden/issues) for features you want to see and problems you have discovered. For general discussions and questions, please use the [discussion board](https://github.com/symflower/garden/discussions).

Cheers,<br/>
The Symflower team

## /bin

This directory contains binaries (and scripts that act as binaries) that are meant for everyday use. We recommend including this directory in your [PATH variable](https://en.wikipedia.org/wiki/PATH_(variable)).

### [/bin/untilfail](/bin/untilfail)

Ever had to debug a non-deterministic program or wondered if some behavior of your code is truly flaky? The `untilfail` binary helps you find reproducers for such cases. Just pass the respective command to your program and it will execute the command until it fails. We recommend adding additional outputs to your command until you have isolated your program.

```bash
untilfail some-program-with-a-bug
```

You can even specify a timeout in case you’re out hunting for infinite loops.

```bash
untilfail -t 10 some-program-with-an-infinite-bug
```

For additional arguments and options you can take a look at the help.

```bash
untilfail -h
```
