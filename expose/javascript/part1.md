1. It returns "values added: 20"
2. It returns "final result: 20"
3. You should not use var because of it's function level scope. This means variables declared with var can be used anywhere in the function, even if it was declared inside an inner block of the function. This can lead to bugs like overwriting data, and it could make it harder to debug.
4. It returns "values added: 20"
5. It returns an error. This is because let is a block-level variable. This means it's limited to the block it's declared in, so in this case, it's limited to the if block, and the 2nd console.log does not recognize the variable result.
6. The earlier line, line 7, returns an error because result is a const variable. This means it can't be changed once declared, and line 7 attempts to do so. As a result, it returns an error.
7. For the same reason as 6, it returns an error due to line 7.
