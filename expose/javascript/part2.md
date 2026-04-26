1. Line 12 will print 3 because of var's function level scope. Var i was declared in the for loop as 0, and it increased all the way to 3, matching prices.length, and when it exited the for loop, it was able to be called by console.log due to it's large scope.
2. Line 13 will print 150 because of var's function level scope. In the final iteration of the for loop, discountedPrice does 300 * .5 which is 150, and this variable still retains the value when it exits the for loop.
3. Line 14 will print 150 for the same reason as above, as finalPrice is also declared using var, but in this case it was declared in the same scope as console.log.
4. The function will return the prices array at whatever the discount is. In this case, it takes [100, 200, 300] and returns [50, 100, 150] because the discount is 50%.
5. Line 12 will return an error because the variable i was declared using let. Let is a block-level variable, so the i will only be limited to the for loop and once it exits, it would be out of scope and deleted from memory, causing line 12 to return an error.
6. Line 13 will return an error for the same reason as above, except with the variable discountedPrice this time.
7. Line 14 will print 150 because finalPrice was declared in the same scope as console.log. This means console.log can access finalPrice. Additionally, since it was declared at the highest level scope, it can also be accessed from within the inner scope of the for loop, which allows its value to be updated.
8. The function will return the prices array at whatever the discount is. In this case, it takes [100, 200, 300] and returns [50, 100, 150] because the discount is 50%. Even though the variables this time were declared with let unlike question 4, everything is still accessed properly within their proper scopes so it works as intended.
9. Line 11 returns an error for the same reason as question 5. 
10. Line 12 will print 3, because length was declared in the same scope as the console.log statement, meaning it can access the variable length. 
11. The function will return the prices array at whatever the discount is. In this case, it takes [100, 200, 300] and returns [50, 100, 150] because the discount is 50%. Even though the variables were declared with const, it has the same scope level as let, and none of the const variables are being reassigned in this code. It seems like discountedPrice is being reassigned in the loop, but everytime the loop enters a new iteration, it creates a new scope, so it's like discountedPrice is being declared constantly, not reassigned.

12A. student.name

12B. student['Grad Year']

12C. student.greeting()

12D. student['Favorite Teacher'].name

12E. student.courseLoad[0]

13A. Returns '32' because the + operator is used as concatenation when one of the operands is a string

13B. Returns 1 because the - operator is always used for math

13C. Returns 3 because null is mapped to 0, so it does addition between 3 and 0

13D. Returns '3null' because + operator is used as concatenation since '3' is a string, and it uses null as a string

13E. Returns 4 because true is mapped to 1, so it does addition between two integers

13F. Returns 0 because false and null both map to 0, so it does addition between them

13G. Returns '3undefined' because + operator is used as concatenation since '3' is a string, and it uses undefined as a string

13H. Returns NaN because - operator is used for math, but because one of the operands is undefined, it results in a NaN

14A. Returns true because '2' gets converted to a number and 2 is greater than 1

14B. Returns false because both values are strings so it compares alphabetically, and '2' is alphabetically after '12'

14C. Returns true because '2' gets converted to a number and 2 is equal to 2

14D. Returns false because === is stricter than ==. It checks for both value and data type, and in this expression one is a string and the other is a number

14E. Returns false because true maps to the number 1, so it checks if 1 is equal to 2

14F. Returns true because Boolean() converts a value to a boolean value. Since any number that is not zero is true, then this expression checks if true is equal to true

15. The difference between == and === is that triple equals is stricter, and checks for both value and data type. Using a double equals allows for type conversion, while triple equals does not.
16. JS Code
17. The function above returns [2, 4, 6]. This is because modifyArray takes an array and a function as input. Everytime newArr.push(callback(array[i])) is called, it first does the callback function which calls doSomething(num), which just doubles num. So each time push is called, it pushes 1\*2, 2\*2, then 3*2, resulting in 2, 4, 6. 
18. JS Code
19. The output of the above code will be 1, 4, 3, 2. This is because 1 is first in the code, then the timeout functions are called, then the function ends with 4. Afterwards, the timeout functions are called after a certain time. The first one to be called is 3 because it had a delay of 0 ms, and then 2 because it had a delay of 1s.