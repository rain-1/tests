# tests

This is a general tool to test a program (via command line invocation) on a bunch of inputs. Either diffing the result against an expected value or searching for an error message.

You invoke it like this `tests <test-directory> <command-line>` with `{}` being a special placeholder in the command line to pass in filenames.

For example try `tests example/ "bash {}"`
