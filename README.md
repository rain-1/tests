# tests

This is a general tool to test a program (via command line invocation) on a bunch of inputs. Either diffing the result against an expected value or searching for an error message.

You invoke it like this `tests <directory> <commandline>` using `{}` being a special placeholder in the command line to pass in filenames. The directory should contain a batch of test files and to each `FILENAME` either `FILENAME.expect` or `FILENAME.error`.

For example try `tests example/ "bash {}"`

# use with travis-ci

You can use this with travis-ci easily.

Just get your git repo and add tests as a submodule:

```
git submodule add -b master https://github.com/rain-1/tests.git
```

then add a target to your makefile like

```
test:
  ./tests/tests t/trivial 'cat init.scm {} | ./bin/sch3'
```
