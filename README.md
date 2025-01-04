# Elixir Enum.each and Throw Example

This repository demonstrates a common error in Elixir when using `Enum.each` with `throw`.  The example shows how `throw` abruptly stops execution and prevents the code from completing normally.  The solution demonstrates a proper way to handle the termination condition.

## Bug
The original code utilizes `throw` inside `Enum.each` to signal the discovery of the number 3.  However, this results in the program's execution stopping before reaching the `IO.puts("Finished")` statement.  This is a common mistake when handling exceptional situations within `Enum.each`. 

## Solution
The solution demonstrates the correct usage of `try...catch` to gracefully handle the thrown exception.  This allows the code to continue execution after handling the `:three_found` case. 