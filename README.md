# CMPT
an attempt to emulate an entire CPU inside of Geometry Dash

# Progress
Working - currently works, but does not place any objects.

# Usage (of non-level library)
```rs
let cmpt = import "cmpt.spwn"
extract cmpt
// Fibonacci numbers
load([
    MOVV, R0, 10,
    CALL, 6,
    HALT,

    PUSH, R0,

    MOVV, R0, 0,
    MOVV, R1, 1,
    MOVV, R3, 1,
    PRINT, R1,

    MOVR, R2, R0,
    ADD, R2, R1,
    PRINT, R2,

    MOVR, R0, R1,
    MOVR, R1, R2,

    MOVV, R2, 1,
    ADD, R3, R2,

    POP, R2,
    PUSH, R2,

    JL, R3, R2, 19,

    POP, R0,

    RET
]);
run();
```
Output:
```
1
1
2
3
5
8
13
21
34
55
```
