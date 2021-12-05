# Guidelines for contributers

This document is just me being grumpy about how I like development being done. If you think I should lower my expectations (which I probably should) or you have any other questions or requests, feel free to reach out/**create an issue**. 

And thank you so much for contributing! Any help is much appreciated <3

## Feature branches

I hope this is self explanatory. When you add a feature, add it on a new branch, and have it reviewed before merging into `main`, especially if there were merge conflicts.

## All you need is issues

Most communication between maintainers/should happend via issues, namely:
- `TODO`s and `FIXME`s in the code (vs-code even has an extension for that)
- Feature proposals (for implementation it's more appropriate to open a pull request)
- Missing docs/specs if you notice their abstence and expecially if you happen to need them

## Testing

Please write unit tests for the non-trivial functionality you add. If it's hard/impossible to write noce self contained units, more often than not your code is too coupled. Try making it more modular. 

That being said, most features I expect to be relatively trivial. Type soundness should probably be tested, because JavaScript, but otherwise don't stress too much. Although, more tests is always better :)

## Documentation

 A JSDoc should be sufficient, in case a function is long/obscure. Do describe your approach and expected result when doing meta programming and other black magic.
