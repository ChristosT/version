# version
What version do I have of ___?

You've been there...

```
java -v // unrecognized option
java -V // unrecognized option
java --version // unrecognized option
java --Version // unrecognized option
java -Version // unrecognized option
java -version // 1.8.0_262
```

There's no standard.

```
gcc --version
node -v
node --version
python -V
perl -v
perl --version
go version
lua -v
rustc --version
```

`version` is a simple, easily updateable script that tells you what version you are on.

```
version node   // v14.70
version gcc    // 10.1.0
version java   // 1.8.0_262
version pascal // 'pascal' does not seem to be installed.
```
## Installation

Download, put in your path.

## Autocompletion

Work in progress. There's a `version.completion` file that registers all known tools. Run `source version.completion` and you should now have tab completion in bash and zsh. You should set up your startup script (.bashrc or .zshrc or whatever) to source this file on startup. If you change the file, you can run the `make_completion` script to update the completion file and then re-source it. Still learning about this feature and may have something better in the future.

## Info
Current version: v0.3.2

Recognized tools: 100

## Contribute

[Contribution guidelines](contributions.md)

## FAQ

Q: Couldn't you just run all the different variations on an unknown command and see which one works?

A: Yes. But running various random commands on somoene else's computer and seeing what happens is not a best practice.

---

Q: Why does it give me an error on command _____?

A: Feel free to file an issue and I'll look into it. Some tools have different variants that behave differently. For example, `sed --version` works fine on my Linux machine, but `sed` does not seem to have any version argument at all on my Mac.

---

Q: Why does it say I don't have a program installed when I know I do?

A: Again, some tools work differently on different systems. For example, on Linux, I can launch Firefox from the command line with `firefox`. But on Mac, I have to type `open -a Firefox`, because on Mac Firefox is not really a command line program. Instead, `Firefox.app` is a special folder containing the executable `firefox` nested a few levels deep. But since that's not in the search path, `version` cannot find it. If you can launch the program Foo by typing `foo` on the command line, then `version foo` should work (if it's in the list). There are no plans to make version work for Mac `.app` programs.
