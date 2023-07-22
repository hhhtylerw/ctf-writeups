# rntk

## Prompt
check out my random number toolkit!

`nc amt.rs 31175`

## Solution
Open Ghidra and analyze the binary to find the main function.

The points of interest are `generate_canary()`, `random_guess()`, and `win()`. 

`main()` is the entry point. It runs `generate_canary()` and takes user input.
![1](image1.png)

`generate_canary()` uses the current time as a seed, generates a random number, and saves it as `global_canary`.
![2](image2.png)

`random_guess()` takes user input via `gets()` and is resistant to attacks by maintaining that a `local_canary` is equal to the `global canary`.
![3](image3.png)

`win()` is an unreachable function that sends the flag.
![4](image4.png)

Using GDB, one can analyze the call stack. Breakpoints should be set before and after the vulnerable `gets()` in order to see how it affects the stack.

## Flag
``
