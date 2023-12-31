# Awesome-Typescript-interview-questions-
Explore a curated collection of concise and insightful TypeScript interview questions in this repository. From fundamental concepts to advanced topics, these questions cover a range of aspects, helping you prepare for TypeScript-related interviews. 

 


### 1. What is TypeScript and why one should use it?
   TypeScript is a free and open-source programming language developed and maintained by Microsoft. It is a strict syntactical superset of JavaScript and adds optional static typing and class-based object-oriented programming to the language.

### 2. List the built-in types in Typescript
   These are also called the primitive types in TypeScript:
   - **Number type:** it is used to represent number type values and represents double precision floating point values.
     ```typescript
     var variable_name: number;
     ```

   - **String type:** it represents a sequence of characters stored as Unicode UTF-16 code. It is the same as the JavaScript primitive type.
     ```typescript
     var variable_name: string;
     ```

   - **Boolean type:** in TypeScript, it is used to represent a logical value. When we use the Boolean type, we get output only in true or false. It is also the same as the JavaScript primitive type.
     ```typescript
     var variable_name: bool;
     ```

   - **Null type:** it represents a null literal and it is not possible to directly reference the null type value itself.
     ```typescript
     var variable_name: number = null;
     ```

   - **Undefined type:** it is the type of undefined literal. This type of built-in type is the sub-type of all the types.
     ```typescript
     var variable_name: number = undefined;
     ```

### 3. Explain generics in TypeScript
   Generics are able to create a component or function to work over a variety of types rather than a single one.
   ```typescript
   /** A class definition with a generic parameter */
   class Queue<T> {
     private data = [];
     push = (item: T) => this.data.push(item);
     pop = (): T => this.data.shift();
   }

   const queue = new Queue<number>();
   queue.push(0);
   queue.push("1"); // ERROR: cannot push a string. Only numbers allowed
  ```

  ### 4. What are Modules in TypeScript?

Modules in TypeScript help in organizing the code. There are 2 types of Modules — Internal and External.

- **Internal Modules:**
  Internal Modules are now replaceable by using TypeScript’s namespace.

- **External Modules:**
  External Modules are used to specify and load dependencies between multiple external JS files. If there is only one JS file used, then external modules are not relevant.

### 5. What is TypeScript and why would I use it in place of JavaScript?

TypeScript is a superset of JavaScript, providing optional static typing, classes, and interfaces. One of the significant benefits is enabling IDEs to offer a richer environment for spotting common errors as you type. For a large JavaScript project, adopting TypeScript might result in more robust software while remaining deployable where a regular JavaScript application would run.

#### Key Points:
- TypeScript supports new ECMAScript standards, compiling them to chosen ECMAScript targets.
- JavaScript code is valid TypeScript code; TypeScript is a superset of JavaScript.
- TypeScript adds type support, including interfaces, enums, hybrid types, generics, union and intersection types, access modifiers, and more.
- Development experience with TypeScript is an improvement over JavaScript, providing real-time feedback from the TypeScript compiler.
- With strict null checks enabled, TypeScript ensures better handling of null and undefined values.
- A build process is required to compile TypeScript to JavaScript, with support for source maps for debugging.
- TypeScript is open source (Apache 2 licensed) and backed by Microsoft, led by Anders Hejlsberg, the lead architect of C#.

### 6. Do we need to compile TypeScript files, and why?

Yes, TypeScript files need to be compiled because browsers cannot directly interpret TypeScript, as it is a language extension. The process of converting TypeScript to JavaScript is referred to as compiling. It's essential to understand that in this context, compilation doesn't involve creating binary code; instead, the term "transpilation" is more accurate. Transpilation ensures that TypeScript code is translated into JavaScript, which can be executed by browsers.

### Q7: What are the benefits of TypeScript?

TypeScript offers the following benefits:

- Code structuring
- Class-based object-oriented programming
- Imposition of coding guidelines
- Type checking
- Compile-time error checking
- Intellisense

### Q8: How to call the base class constructor from the child class in TypeScript?

We can call the base class constructor using `super()`.

### Q9: What is TypeScript, and why do we need it?

JavaScript, though universally supported, has design flaws such as lack of class-based object-oriented features, unreliable dynamic typing, and a lack of compile-time error checking. TypeScript, developed by Microsoft, addresses these issues. It is a free and open-source programming language, a strict superset of JavaScript, adding optional static typing and class-based object-oriented programming. TypeScript is suitable for developers familiar with C#, Java, and other strongly typed languages.

### Q10: How to perform string interpolation in TypeScript?

String interpolation in TypeScript can be performed using template literals, which are literals delimited with backticks (`). For example:

```typescript
let value = 100;
console.log(`The size is ${value}`);
```

### Q11: What is the difference between .ts and .tsx extensions in TypeScript?

- Use `.ts` for pure TypeScript files.
- Use `.tsx` for files that contain JSX.


### Q12: What is the difference between Classes and Interfaces in TypeScript?

- Classes are used as object factories, defining blueprints with initializations and methods.
- Interfaces are virtual structures for type-checking, existing only in TypeScript context.

### Q13: What is Interface in TypeScript?

- An interface is a virtual structure for type-checking purposes.
- It defines the properties an object should have in terms of name and type.

### Q14: What is Decorators in TypeScript?

- Decorators are special declarations attached to classes, methods, properties, etc.
- They are functions that take their target as an argument, allowing code execution around the target.

### Q15: What are the differences between TypeScript and JavaScript?

- TypeScript is an object-oriented programming language.
- TypeScript has static typing with various ways to declare variables.
- TypeScript supports interfaces.
- TypeScript features optional parameters and Rest Parameter.
- TypeScript supports generics.
- TypeScript supports modules.
- Number, string, etc., are interfaces in TypeScript.

### Q16: When to use interfaces and when to use classes in TypeScript?

- Use classes when creating instances with type-checking for arguments, return types, or generics.
- Use interfaces when not creating instances, benefiting from virtual type-checking without generating source code.

### Q17: How to implement class constants in TypeScript?

In TypeScript, use the `readonly` modifier as the `const` keyword cannot be used for class properties.

```typescript
class MyClass {
    readonly myReadonlyProperty = 1;

    myMethod() {
        console.log(this.myReadonlyProperty);
    }
}
new MyClass().myReadonlyProperty = 5; // error, readonly
```
### Q18: How could you check null and undefined in TypeScript?
-Just use:
```
if (value) {
}
```
It will evaluate to true if value is not:

- null
- undefined
- NaN
- empty string ''
- 0
- false
TypesScript includes JavaScript rules.


### Q19: Does TypeScript support all object-oriented principles?

Yes, TypeScript supports all four main principles of Object-Oriented Programming:
1. Encapsulation
2. Inheritance
3. Abstraction
4. Polymorphism

TypeScript can implement all these principles with its smaller and cleaner syntax.

### Q20: Which object-oriented terms are supported by TypeScript?

TypeScript supports the following object-oriented terms:
- Modules
- Classes
- Interfaces
- Data Types
- Member functions

### Q21: What are getters/setters in TypeScript?

TypeScript supports getters/setters as a way of intercepting accesses to a member of an object. This provides finer-grained control over how a member is accessed on each object.

```typescript
class Foo {
  private _bar: boolean = false;

  get bar(): boolean {
    return this._bar;
  }
  
  set bar(theBar: boolean) {
    this._bar = theBar;
  }
}

const myFoo = new Foo();
const myBar = myFoo.bar;  // Correct (get)
myFoo.bar = true;        // Correct (set)
```

### Q21: What is a TypeScript Map file?

.map files are source map files that allow tools to map between the emitted JavaScript code and the TypeScript source files that created it. Debuggers, such as Visual Studio or Chrome's dev tools, can consume these files, enabling debugging of TypeScript code instead of the generated JavaScript.

### Q22: What is the difference between types `String` and `string` in TypeScript?

- `String` is the JavaScript String type used to create new strings.
- `string` is the TypeScript string type used to type variables, parameters, and return values.

### Q23: What does the pipe (|) mean in TypeScript?

The pipe (`|`) represents a union type in TypeScript. A union type describes a value that can be one of several types. For example, `number | string | boolean` is the type of a value that can be a number, a string, or a boolean.

Example:
```typescript
let something: number | string | boolean;
something = 1;     // ok
something = '1';   // ok
something = true;  // ok
something = {};    // Error: Type '{}' is not assignable to type 'string | number | boolean'
```

### Q24: How to make Arrays that can only be read in TypeScript?

Using the `ReadonlyArray` type describes arrays that can only be read from. Any variable with a reference to a `ReadonlyArray` can't add, remove, or replace any elements of the array.

Example:
```typescript
function foo(arr: ReadonlyArray<string>) {
    arr.slice();        // okay
    arr.push("hello!"); // error!
}
```

### Q25: What is the purpose of the Nullish Coalescing operator?

The nullish coalescing operator  `(??)` is a logical operator that returns its right-hand side operand when its left-hand side operand is null or undefined, and otherwise returns its left-hand side operand. Its main purpose is to simplify assigning default values. The nullish coalescing operator tests for null and undefined only.

```typescript
// Nullish coalescing
console.log(0 ?? 'error');     // 0
console.log('' ?? 'error');    // ''
console.log(null ?? 'error');  // 'error'
```


### Q26: Which access modifiers are implied when not specified?

- Everything in a class is public if not specified.
- Everything in a module is private unless the `export` keyword is used.


### Q27: What is the role of the "readonly" keyword in TypeScript?

- The `readonly` keyword is used to make a property or variable immutable. Once a value is assigned, it cannot be changed. This is particularly useful for creating objects with constant values.

### Q28: Explain the concept of "Type Inference" in TypeScript.

- Type inference is the ability of the TypeScript compiler to automatically deduce and assign types to variables based on their values. This allows developers to write code without explicitly specifying types in every case, making the code cleaner and more concise.

### Q29: How does TypeScript support "Mixins"?

- TypeScript supports mixins, a concept where a class can extend multiple classes to inherit their properties and methods. This is achieved by combining classes and using intersection types to merge their functionality.

### Q30: What is the purpose of the "never" type in TypeScript?

- The `never` type in TypeScript represents values that will never occur. It is often used as the return type for functions that always throw an exception or never return. It is also inferred for functions that have an infinite loop or always throw errors.
- 



## Feedback

If you have any feedback, please reach out to us at ashrafuj.jaman.tanbin@gmail.com



## 🔗 Links
[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://ashrafuj-jaman-s-porfolio.vercel.app/)
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ashrafuj-jaman)
 



![Logo](https://files.catbox.moe/ttaz60.png)




