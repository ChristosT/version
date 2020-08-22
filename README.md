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
version node // v14.70
version gcc // 10.1.0
version java // 1.8.0_262
```

Download, put in your path, update, send pull requests.
