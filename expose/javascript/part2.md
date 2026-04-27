1. It prints out **3**. This is because the for loop will keep incrementing the value of i until it's no longer strictly less than prices.length, meaning it will terminate once i reaches 3. And since i is declared as a var, it can be accessed throughout the function. 
2. It prints out **150**. This is because for each iteration of the for loop, discountedPrice is assigned that element of the prices array multiplied by 0.5. Once you get to the final element of the prices array (300), it's multiplied by 0.5 which gets you 150. Also, because discountedPrice is a var, it's accessible outside of the for loop block, meaning there won't be an error. 
3. It prints out **150**. This is because finalPrice takes the value of discountedPrice during the final iteration of the for loop, multiplies it by 100, rounds it (doesn't matter since it's already an integer), and divides it by 100, bringing it back to the original number which was 150. Also, because finalPrice is a var, it's accessible outside of the for loop block. 
4. This function will return a list **[50, 100, 150]**. Every iteration of the for loop takes the corresponding element from the prices list, applies the discount, and pushes it to the discounted list. So for a prices list of [100, 200, 300], the discounted list [50, 100, 150] will be returned.
5. This will cause a **ReferenceError** because i is not defined in that scope. Because i is defined via let, its scope only extends to the for loop block. It can't be called outside of that block. 
6. This will also cause a **ReferenceError** because discountedPrice is declared via let, meaning its scope only extends to the for loop block where it was made. It can't be called outside of that for loop block.
7. This will print out **150**. The finalPrice variable is declared via let, but it's declared in the function, not inside the for loop block. That means its scope extends to the overall function, and it can be accessed. 
8. This will return a list **[50, 100, 150]**. The computations done are the same as in question 4. What interests us here is the variable declaration. Even though it is declared via let, discounted is declared in the function, not within the for loop block. That means it can successfully be accessed and returned in the function. 
9. This will cause a **ReferenceError** because i is declared via let in the for loop block, meaning it's not accessible outside of that block. 
10. This will print out **3**. The variable length is declared via const and is never reassigned. It's also in the scope because it's declared in the function, not inside of the for loop block. 
11. This will return the list **[50, 100, 150]**. The computations work out to be the same as the previous questions, even though the rounding step is missing. The variable discounted is declared via const inside the function, meaning it's reachable anywhere in the function, so there's no issue there. When it comes to arrays, const simply means the variable can't be reassigned to another variable. Pushing elements into the array is no problem. 
12. 
```javascript
student.name // Accessing name property
student['Grad Year'] // Accessing Grad Year property
student.greeting() // Calling function for greeting property
student['Favorite Teacher'].name // Accessing name property in Favorite Teacher property
student.courseLoad[0] // Accessing index 0 of courseLoad property array
```
13.  
- A. '3' + 2 -> **'32'** because integers map to their string representation, resulting in string concatenation.
- B. '3' - 2 -> **1** because - only works numerically so it will just compute 3 - 2 which is 1.
- C. 3 + null -> **3** because null is converted to 0 so it's 3 + 0 which is 3. 
- D. '3' + null -> **'3null'** because null is converted to a string and it's concatenated.
- E. true + 3 -> **4** because true is converted to its numerical representation which is 1 so 1 + 3 which is 4.
- F. false + null -> **0** because both of them are converted to 0 and 0 + 0 is 0.
- G. '3' + undefined -> **'3undefined'** because undefined is converted to a string and it's concatenated.
- H. '3' - undefined -> **NaN** because '3' will be converted to its numeric form and any arithmetic involving NaN is NaN.
14. 
- A. '2' > 1 -> **true** because '2' will be interpreted numerically and 2 > 1.
- B. '2' < '12' -> **false** because they're both strings and will be compared lexicographically, where '2' is not < '1'.
- C. 2 == '2' -> **true** because they will be compared numerically and 2 = 2.
- D. 2 === '2' -> **false** because this is a strict equality and 2 and '2' don't share the same type. 
- E. true == 2 -> **false** because true is interpreted numerically and 1 is not equal to 2.
- F. true === Boolean(2) -> **true** because Boolean(2) will convert to true and true === true.
15.  == is a loose equality, meaning it will automatically convert types to perform comparisons. === is a strict equality. It will not perform any type conversions and it needs types and values to match to return true. 
16.  
```javascript
for (let property in statistics) {
    let value = statistics[property];

    if (property.startsWith('r') || value % 2 != 0) {
        console.log(value);
    }
}
```
17. The result will be the array **[2, 4, 6]**. This is because modifyArray takes the function doSomething as a parameter and calls that function to compute the elements that are pushed into the new array. I was able to test this by printing the output:

```javascript
console.log(modifyArray([1, 2, 3], doSomething));
```

18. 
```javascript
function printTime() {
    let d = new Date();
    let time = d.toLocaleTimeString();
    console.log(time);
}

setInterval(printTime, 1000);
```

19. 
1
4
3
2
