# assert-the-unexpected

This implements the node core `assert` API as an Unexpected facade.

A great deal of emphasis was placed on compatibility and this module aims to
be a drop-in replacement. It was developed against the node 4.7.3 test suite
in core which it passes with the exception of the following:
* circular references are not supported
* deepEqual() **not** throwing on comparisons of:
    - "a" to {0:'a'} (supported for Arrays)
    - mismatching prototypes
