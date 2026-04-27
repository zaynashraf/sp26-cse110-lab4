1. 'values added:  20'
2. 'final result:  20'
3. You shouldn't use var because of it being function scoped, meaning you can accidentally access it in places in your code where it shouldn't be accessible (like outside of an if block). This can lead to logical errors and bugs, as well as naming conflicts. 
4. 'values added:  20'
5. It causes a **ReferenceError** because result is not defined. This is because we're using let here, which operates on a block scope. Outside of the if block, result is not defined, meaning when you try to call it using console.log, you get an error. 
6. It causes a **TypeError** because the code is attempting an assignment to a constant variable on line 7, which is not allowed. 
7. It causes a **TypeError** because the code is attempting an assignment to a constant variable on line 7, which is not allowed. However, even if we were to remove that assignment, it would still cause a ReferenceError because result is not defined outside of that if block. 