# Type Annotation

## Table of Contents

- [Our First Type Annotation]()
- [Working With Numbers and Booleans]()
- [Compiling TypeScript]()
- [Type Inference]()
- [The Any Type]()
- [Delayed Initialization and Implicit Any]()

### Our First Type Annotation

Type annotations in TypeScript are used to specify the data type of a variable, parameter, or property. They provide a way to explicitly declare the expected type of a value, which allows TypeScript to catch type-related errors during compilation. Here are some code examples of 
type annotations for strings and numbers, along with short descriptions:

1. **Type Annotation for Strings**:

```ts
// Variable with a type annotation for a string
let message: string = "This is a string.";
```

In this example, the `message` variable is explicitly annotated with the type `string`, specifying that it can only store string values.

2. **Type Annotation for Numbers**:

```ts
// Variable with a type annotation for a number
let age: number = 30;
```

In this case, the `age` variable is annotated with the type `number`, indicating that it can only contain numeric values.

Type annotations in TypeScript are used to define the 
expected data type of a variable. This helps catch type-related errors 
during development and provides better code documentation.

### Working with numbers and booleans

Here are examples of type annotations for numbers and booleans:

1. **Type Annotation for Numbers**:

```ts
// Variable with a type annotation for a number
let score: number = 95;
```

In this example, the `score` variable is explicitly annotated with the type `number`, specifying that it can only store numeric values.

2. **Type Annotation for Booleans**:

```ts
// Variable with a type annotation for a boolean
let isCompleted: boolean = true;
```

Here, the `isCompleted` variable is annotated with the type `boolean`, indicating that it can only hold boolean values, which are `true` or `false`.

Type annotations in TypeScript are a way to define and 
enforce the expected data types of variables, which is especially useful for catching type-related errors and ensuring code reliability.

### Compiling TypeScript

Certainly, here are the shortened steps to compile TypeScript in Visual Studio Code using the `tsc` command:

1. **Install Node.js and TypeScript**: Install Node.js from [nodejs.org](https://nodejs.org/) and then use npm to install TypeScript globally:
   
   ```
   npm install -g typescript
   ```
- **Create a TypeScript File**: Create or open a TypeScript (.ts) file in your project, e.g., `app.ts`.

- **Open Integrated Terminal**: In Visual Studio Code, open the integrated terminal:
  
  - Go to `View` > `Terminal`.
  - Navigate to your project directory.

- **Compile TypeScript Using `tsc`**:
  
  ```
  tsc app.ts
  ```

- This generates a JavaScript (.js) file with the same name (e.g., `app.js`).

- **Run the Compiled JavaScript Code**:
  
  ```
  node app.js
  ```

These simplified steps should help you quickly compile and run TypeScript in Visual Studio Code using the `tsc` command.

### Type Inference

Type inference in TypeScript is the ability of the compiler to automatically determine and assign data types to variables, parameters, and expressions based on the values and how they are used in the code. TypeScript analyzes the context and infers the types, which can help 
reduce the need for explicit type annotations while maintaining type safety. Let's revisit the previous examples and highlight type 
inference:

1. **Type Annotation for Strings**:
   
   ```ts
   let message: string = "This is a string.";
   ```

In this example, we explicitly annotate the `message` variable with the type `string`.
 However, TypeScript can infer the type of the variable based on the 
value assigned to it, so the type annotation is optional. TypeScript 
will automatically infer that `message` is of type `string` because it's initialized with a string value.

```ts
let message = "This is a string."; // Type inferred as string
```

**Type Annotation for Numbers**:

```ts
let age: number = 30;
```

Just like in the previous example, TypeScript can infer the type of `age` without the need for an explicit type annotation:

```ts
let age = 30; // Type inferred as number
```

**Type Annotation for Booleans**:

Similarly, for boolean values, type inference can determine the type without an annotation:

```ts
let isCompleted: boolean = true;
```

The type `boolean` is inferred by TypeScript based on the value `true`:

```ts
let isCompleted = true; // Type inferred as boolean
```

Type inference is one of the strengths of TypeScript 
because it allows you to write code with less ceremony and still benefit from static typing. It's especially useful when you want to keep your code concise and readable without sacrificing type safety. However, you can always add type annotations when needed to provide more clarity or when TypeScript cannot infer the type accurately.

### The Any Type

The `any` type in TypeScript represents dynamic or untyped values, allowing 
variables to have values of any type. Here is a  brief code examples:

**Dynamic Typing**:

```ts
let dynamicValue: any = 42;
dynamicValue = "Hello, TypeScript!";
```

### Delayed Initialization and Implicit Any



- **Delayed Initialization** refers to declaring a variable without an initial value, often inferring the type as `any`. Values are assigned later.

```ts
let data; // Variable declared without initialization
// ...
if (someCondition) {
  data = 42; // Initialize 'data' inside a conditional branch
} else {
  data = "Hello"; // 'data' can hold different types
}
```

In this code example, data is declared 
without an initial value, and TypeScript infers it as any. It's assigned
 different types later in the code.

- **Implicit Any** occurs when TypeScript infers a variable to have the `any` type due to unclear initialization, typically when type annotations are
   omitted. It's best to use explicit type annotations to prevent implicit
   `any` types and ensure strong typing.

```ts
let value; // Implicit 'any' type
value = 42; // Valid
value = "Hello"; // Valid
```

In this code, `value` is implicitly inferred 
as the any type because there is no type annotation and no explicit 
initialization. Implicit any types should be avoided by providing 
explicit type annotations when declaring variables to maintain strong 
typing and prevent runtime errors.
