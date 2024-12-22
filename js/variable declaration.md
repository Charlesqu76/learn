# JavaScript Variable Declarations

JavaScript provides three main ways to declare variables:

## 1. `var`
- **Scope**: Function-scoped (accessible within the function).  
- **Redeclaration**: Allowed (no error if declared again).  
- **Hoisting**: Variables are hoisted but initialized with `undefined`.  
- **Example**:  
    ```javascript
    var name = "John";
    var name = "Doe";  // No error
    console.log(name);  // "Doe"
    ```

---

## 2. `let`
- **Scope**: Block-scoped (only accessible within the block).  
- **Redeclaration**: Not allowed in the same scope.  
- **Hoisting**: Hoisted but not initialized.  
- **Example**:  
    ```javascript
    let age = 25;
    age = 26;  // Reassignment is allowed
    // let age = 30;  // Error: 'age' has already been declared
    console.log(age);  // 26
    ```

---

## 3. `const`
- **Scope**: Block-scoped.  
- **Redeclaration**: Not allowed.  
- **Reassignment**: Not allowed (immutable reference).  
- **Hoisting**: Hoisted but not initialized.  
- **Example**:  
    ```javascript
    const PI = 3.14;
    // PI = 3.1415;  // Error: Assignment to constant variable
    const user = { name: "Alice" };
    user.name = "Bob";  // Allowed (object properties can be changed)
    console.log(user.name);  // "Bob"
    ```

---

## Key Differences

| Feature         | `var`                        | `let`                        | `const`                      |
|-----------------|------------------------------|------------------------------|------------------------------|
| Scope           | Function                     | Block                        | Block                        |
| Redeclaration   | Allowed                      | Not allowed                  | Not allowed                  |
| Reassignment    | Allowed                      | Allowed                      | Not allowed                  |
| Hoisting        | Yes (initialized as `undefined`) | Yes (not initialized)        | Yes (not initialized)        |

---

## Best Practices
- Use **`const`** by default to ensure immutability.  
- Use **`let`** when reassignment is necessary.  
- Avoid **`var`** unless maintaining legacy code.  

<!--stackedit_data:
eyJoaXN0b3J5IjpbODQ1NzI1NTA3XX0=
-->