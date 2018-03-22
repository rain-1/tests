# tests

This is a general tool to test a program (via command line invocation) on a bunch of inputs. Either diffing the result against an expected value or searching for an error message.

You invoke it like this `tests <directory> <commandline>` using `{}` being a special placeholder in the command line to pass in filenames. The directory should contain a batch of test files and to each `FILENAME` either `FILENAME.expect` or `FILENAME.error`.

For example try `tests example/ "bash {}"`

