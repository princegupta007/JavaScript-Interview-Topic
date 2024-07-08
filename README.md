# Topics Wise Que & Ans

## Practical Topics

### 1. Basic Syntax and Operators
- **Variables (let, const, var)**
  - **Explanation**: `let` and `const` are block-scoped, `var` is function-scoped. `const` is for constants.
  - **Example**:
    ```javascript
    let age = 25;
    const name = 'Alice';
    var city = 'New York';
    ```

- **Data types (string, number, boolean, null, undefined, symbol, bigint)**
  - **Explanation**: JavaScript has dynamic types, which means the same variable can hold different types of values.
  - **Example**:
    ```javascript
    let text = 'Hello'; // string
    let num = 123; // number
    let isHappy = true; // boolean
    let unknown = null; // null
    let notDefined; // undefined
    let uniqueId = Symbol('id'); // symbol
    let largeNumber = BigInt(9007199254740991); // bigint
    ```

- **Operators (arithmetic, assignment, comparison, logical, bitwise)**
  - **Explanation**: Operators are used to perform operations on variables and values.
  - **Example**:
    ```javascript
    let a = 5, b = 10;
    let sum = a + b; // arithmetic
    let isEqual = a == b; // comparison
    let andCondition = (a > 0 && b > 0); // logical
    let bitwiseAnd = a & b; // bitwise
    ```

### 2. Control Structures
- **Conditional statements (if, else, switch)**
  - **Explanation**: Control the flow of the code based on conditions.
  - **Example**:
    ```javascript
    if (a > b) {
      console.log('a is greater');
    } else {
      console.log('b is greater or equal');
    }

    switch (a) {
      case 1:
        console.log('a is 1');
        break;
      case 2:
        console.log('a is 2');
        break;
      default:
        console.log('a is something else');
    }
    ```

- **Loops (for, while, do...while)**
  - **Explanation**: Repeat a block of code multiple times.
  - **Example**:
    ```javascript
    for (let i = 0; i < 5; i++) {
      console.log(i);
    }

    let j = 0;
    while (j < 5) {
      console.log(j);
      j++;
    }

    let k = 0;
    do {
      console.log(k);
      k++;
    } while (k < 5);
    ```

### 3. Functions
- **Function declaration and expression**
  - **Explanation**: Functions can be defined and assigned to variables.
  - **Example**:
    ```javascript
    function add(a, b) {
      return a + b;
    }

    const subtract = function(a, b) {
      return a - b;
    };
    ```

- **Arrow functions**
  - **Explanation**: Shorter syntax and does not have its own `this`.
  - **Example**:
    ```javascript
    const multiply = (a, b) => a + b;
    ```

- **Higher-order functions**
  - **Explanation**: Functions that take other functions as arguments or return functions.
  - **Example**:
    ```javascript
    function higherOrder(fn, value) {
      return fn(value);
    }

    higherOrder(console.log, 'Hello');
    ```

- **Callbacks**
  - **Explanation**: Functions passed as arguments to other functions.
  - **Example**:
    ```javascript
    function greeting(name, callback) {
      console.log('Hello ' + name);
      callback();
    }

    greeting('Alice', function() {
      console.log('This is a callback function');
    });
    ```

- **Closures**
  - **Explanation**: Functions that retain access to their lexical scope.
  - **Example**:
    ```javascript
    function outer() {
      let count = 0;
      return function inner() {
        count++;
        console.log(count);
      };
    }

    const counter = outer();
    counter(); // 1
    counter(); // 2
    ```

- **Recursion**
  - **Explanation**: A function calling itself.
  - **Example**:
    ```javascript
    function factorial(n) {
      if (n <= 1) return 1;
      return n * factorial(n - 1);
    }

    console.log(factorial(5)); // 120
    ```

### 4. Objects and Arrays
- **Object creation and manipulation**
  - **Explanation**: Creating and working with objects.
  - **Example**:
    ```javascript
    const person = {
      name: 'Alice',
      age: 25
    };
    person.city = 'New York';
    console.log(person);
    ```

- **Array methods (map, filter, reduce, forEach, find, etc.)**
  - **Explanation**: Built-in methods to manipulate arrays.
  - **Example**:
    ```javascript
    const numbers = [1, 2, 3, 4, 5];
    const doubled = numbers.map(n => n * 2);
    const even = numbers.filter(n => n % 2 === 0);
    const sum = numbers.reduce((acc, n) => acc + n, 0);
    console.log(doubled, even, sum);
    ```

- **Destructuring**
  - **Explanation**: Extracting values from arrays or objects.
  - **Example**:
    ```javascript
    const { name, age } = person;
    const [first, second] = numbers;
    ```

- **Spread and rest operators**
  - **Explanation**: `...` used to spread or gather elements.
  - **Example**:
    ```javascript
    const arr1 = [1, 2, 3];
    const arr2 = [...arr1, 4, 5];

    function sum(...args) {
      return args.reduce((acc, n) => acc + n, 0);
    }
    ```

### 5. ES6+ Features
- **Template literals**
  - **Explanation**: String literals allowing embedded expressions.
  - **Example**:
    ```javascript
    const greeting = `Hello, ${name}`;
    ```

- **Default parameters**
  - **Explanation**: Setting default values for function parameters.
  - **Example**:
    ```javascript
    function greet(name = 'Guest') {
      console.log(`Hello, ${name}`);
    }
    ```

- **Destructuring assignment**
  - **Explanation**: Extracting values from arrays or objects.
  - **Example**:
    ```javascript
    const { name, age } = person;
    const [first, second] = numbers;
    ```

- **Spread/rest operators**
  - **Explanation**: `...` used to spread or gather elements.
  - **Example**:
    ```javascript
    const arr1 = [1, 2, 3];
    const arr2 = [...arr1, 4, 5];

    function sum(...args) {
      return args.reduce((acc, n) => acc + n, 0);
    }
    ```

- **Promises and async/await**
  - **Explanation**: Handling asynchronous operations.
  - **Example**:
    ```javascript
    const promise = new Promise((resolve, reject) => {
      setTimeout(() => resolve('Done!'), 1000);
    });

    async function asyncFunction() {
      const result = await promise;
      console.log(result);
    }
    ```

- **Modules (import/export)**
  - **Explanation**: Using ES6 module system.
  - **Example**:
    ```javascript
    // file1.js
    export const add = (a, b) => a + b;

    // file2.js
    import { add } from './file1.js';
    ```

### 6. DOM Manipulation
- **Selecting elements (getElementById, querySelector, etc.)**
  - **Explanation**: Accessing HTML elements.
  - **Example**:
    ```javascript
    const element = document.getElementById('myElement');
    const button = document.querySelector('button');
    ```

- **Modifying elements (innerHTML, textContent, styles, etc.)**
  - **Explanation**: Changing content or style of elements.
  - **Example**:
    ```javascript
    element.innerHTML = '<p>New Content</p>';
    element.style.color = 'blue';
    ```

- **Event handling (addEventListener, event delegation)**
  - **Explanation**: Responding to user interactions.
  - **Example**:
    ```javascript
    button.addEventListener('click', () => {
      console.log('Button clicked');
    });

    document.body.addEventListener('click', (event) => {
      if (event.target.matches('button')) {
        console.log('Button clicked');
      }
    });
    ```

- **Form handling and validation**
  - **Explanation**: Managing form inputs and validating data.
  - **Example**:
    ```javascript
    const form = document.querySelector('form');
    form.addEventListener('submit', (event) => {
      event.preventDefault();
      const name = form.elements

['name'].value;
      if (name === '') {
        alert('Name is required');
      } else {
        console.log('Form submitted', name);
      }
    });
    ```

### 7. Event Loop and Asynchronous JavaScript
- **Call stack and event loop**
  - **Explanation**: Understanding how JavaScript executes code.
  - **Example**:
    ```javascript
    console.log('Start');
    setTimeout(() => {
      console.log('Callback');
    }, 1000);
    console.log('End');
    ```

- **Promises**
  - **Explanation**: Handling asynchronous operations.
  - **Example**:
    ```javascript
    const promise = new Promise((resolve, reject) => {
      setTimeout(() => resolve('Done!'), 1000);
    });

    promise.then((result) => {
      console.log(result);
    });
    ```

- **Async/await**
  - **Explanation**: Syntactic sugar for Promises.
  - **Example**:
    ```javascript
    async function asyncFunction() {
      const result = await promise;
      console.log(result);
    }
    ```

- **Microtasks and macrotasks**
  - **Explanation**: Understanding the difference between microtasks and macrotasks.
  - **Example**:
    ```javascript
    Promise.resolve().then(() => console.log('Microtask'));
    setTimeout(() => console.log('Macrotask'), 0);
    console.log('Synchronous');
    ```

### 8. Error Handling
- **Try...catch...finally**
  - **Explanation**: Handling exceptions.
  - **Example**:
    ```javascript
    try {
      throw new Error('Something went wrong');
    } catch (error) {
      console.log(error.message);
    } finally {
      console.log('Always executed');
    }
    ```

- **Custom errors**
  - **Explanation**: Creating custom error types.
  - **Example**:
    ```javascript
    class CustomError extends Error {
      constructor(message) {
        super(message);
        this.name = 'CustomError';
      }
    }

    throw new CustomError('This is a custom error');
    ```

- **Error propagation**
  - **Explanation**: Passing errors up the call stack.
  - **Example**:
    ```javascript
    function func1() {
      throw new Error('Error in func1');
    }

    function func2() {
      try {
        func1();
      } catch (error) {
        console.log('Caught in func2', error.message);
        throw error;
      }
    }

    try {
      func2();
    } catch (error) {
      console.log('Caught in global scope', error.message);
    }
    ```

### 9. JavaScript in the Browser
- **Browser APIs (localStorage, sessionStorage, cookies)**
  - **Explanation**: Storing data in the browser.
  - **Example**:
    ```javascript
    localStorage.setItem('name', 'Alice');
    const name = localStorage.getItem('name');

    sessionStorage.setItem('session', '123');
    const session = sessionStorage.getItem('session');

    document.cookie = 'user=Alice';
    ```

- **Fetch API and AJAX**
  - **Explanation**: Making HTTP requests.
  - **Example**:
    ```javascript
    fetch('https://api.example.com/data')
      .then(response => response.json())
      .then(data => console.log(data))
      .catch(error => console.error('Error:', error));

    const xhr = new XMLHttpRequest();
    xhr.open('GET', 'https://api.example.com/data');
    xhr.onload = function() {
      if (xhr.status === 200) {
        console.log(JSON.parse(xhr.responseText));
      }
    };
    xhr.send();
    ```

- **WebSockets**
  - **Explanation**: Real-time communication.
  - **Example**:
    ```javascript
    const socket = new WebSocket('ws://example.com/socket');

    socket.onopen = () => {
      console.log('WebSocket open');
      socket.send('Hello Server');
    };

    socket.onmessage = (event) => {
      console.log('Message from server', event.data);
    };
    ```

### 10. Testing
- **Unit testing (Jest, Mocha, Chai)**
  - **Explanation**: Testing individual units of code.
  - **Example**:
    ```javascript
    // Jest example
    test('adds 1 + 2 to equal 3', () => {
      expect(add(1, 2)).toBe(3);
    });
    ```

- **Integration testing**
  - **Explanation**: Testing how different parts of the application work together.
  - **Example**:
    ```javascript
    // Using Jest and Supertest for integration testing
    const request = require('supertest');
    const app = require('./app');

    test('GET /api/users', async () => {
      const response = await request(app).get('/api/users');
      expect(response.statusCode).toBe(200);
      expect(response.body).toEqual(expect.any(Array));
    });
    ```

- **Writing testable code**
  - **Explanation**: Ensuring code is easy to test.
  - **Example**:
    ```javascript
    // Write functions with clear inputs and outputs
    function sum(a, b) {
      return a + b;
    }

    // Use dependency injection
    function fetchData(apiClient) {
      return apiClient.get('/data');
    }
    ```

## Theoretical Topics

### 1. JavaScript Fundamentals
- **History and evolution of JavaScript**
  - **Explanation**: Understanding the origins and growth of JavaScript.
  - **Example**: JavaScript was created by Brendan Eich in 1995 and has since evolved with multiple versions of ECMAScript, with ES6 (2015) being a major update.

- **ECMAScript versions and features**
  - **Explanation**: Knowing the key features introduced in each ECMAScript version.
  - **Example**: ES6 introduced let/const, arrow functions, classes, template literals, and modules.

### 2. Execution Context and Scope
- **Global and local scope**
  - **Explanation**: Variables declared outside functions have global scope; inside functions have local scope.
  - **Example**:
    ```javascript
    let globalVar = 'I am global';

    function scopeExample() {
      let localVar = 'I am local';
      console.log(globalVar); // Accessible
    }

    console.log(localVar); // Error: localVar is not defined
    ```

- **Hoisting**
  - **Explanation**: Variables and function declarations are moved to the top of their containing scope during compilation.
  - **Example**:
    ```javascript
    console.log(hoistedVar); // undefined
    var hoistedVar = 'I am hoisted';

    hoistedFunction(); // Works
    function hoistedFunction() {
      console.log('This function is hoisted');
    }
    ```

- **Lexical scoping**
  - **Explanation**: Functions are executed using the variable scope in which they were defined.
  - **Example**:
    ```javascript
    function outer() {
      let outerVar = 'Outer';

      function inner() {
        console.log(outerVar); // Accessible due to lexical scoping
      }

      inner();
    }

    outer();
    ```

- **Scope chain**
  - **Explanation**: JavaScript resolves variable access by traversing up the nested scopes.
  - **Example**:
    ```javascript
    let globalVar = 'Global';

    function outer() {
      let outerVar = 'Outer';

      function inner() {
        let innerVar = 'Inner';
        console.log(globalVar); // Global
        console.log(outerVar); // Outer
        console.log(innerVar); // Inner
      }

      inner();
    }

    outer();
    ```

### 3. Closures
- **Definition and use cases**
  - **Explanation**: A closure is a function that retains access to its lexical scope.
  - **Example**:
    ```javascript
    function createCounter() {
      let count = 0;
      return function() {
        count++;
        return count;
      };
    }

    const counter = createCounter();
    console.log(counter()); // 1
    console.log(counter()); // 2
    ```

- **Memory efficiency**
  - **Explanation**: Closures can help with memory efficiency by encapsulating state.
  - **Example**: Above `createCounter` function keeps the `count` variable private and efficient.

- **Common pitfalls**
  - **Explanation**: Misunderstanding scope or causing memory leaks.
  - **Example**: Retaining unnecessary references inside a closure can lead to memory leaks.

### 4. Prototype and Inheritance
- **Prototype chain**
  - **Explanation**: JavaScript objects inherit properties and methods from their prototype.
  - **Example**:
    ```javascript
    function Person(name) {
      this.name = name;
    }

    Person.prototype.greet = function() {
      console.log('Hello, ' + this.name);
    };

    const alice = new Person('Alice');
    alice.greet(); // Hello, Alice
    ```

- **Prototypal inheritance**
  - **Explanation**: Objects inherit directly from other objects.
  - **Example**:
    ```javascript
    const parent = {
      greet() {
        console.log('Hello from parent');
      }
    };

    const child = Object.create(parent);
    child.greet(); // Hello from parent
    ```

- **ES6 class syntax**
  -

 **Explanation**: Syntactic sugar for working with prototypes and inheritance.
  - **Example**:
    ```javascript
    class Person {
      constructor(name) {
        this.name = name;
      }

      greet() {
        console.log('Hello, ' + this.name);
      }
    }

    const alice = new Person('Alice');
    alice.greet(); // Hello, Alice
    ```

### 5. This Keyword
- **Understanding `this` in different contexts**
  - **Explanation**: The value of `this` depends on the execution context.
  - **Example**:
    ```javascript
    const obj = {
      name: 'Alice',
      greet() {
        console.log('Hello, ' + this.name);
      }
    };

    obj.greet(); // Hello, Alice

    const greet = obj.greet;
    greet(); // Hello, undefined
    ```

- **Call, apply, bind methods**
  - **Explanation**: Methods to control the value of `this`.
  - **Example**:
    ```javascript
    function greet() {
      console.log('Hello, ' + this.name);
    }

    const obj = { name: 'Alice' };

    greet.call(obj); // Hello, Alice
    greet.apply(obj); // Hello, Alice

    const boundGreet = greet.bind(obj);
    boundGreet(); // Hello, Alice
    ```

- **Arrow functions and lexical `this`**
  - **Explanation**: Arrow functions do not have their own `this`; they inherit it from the enclosing scope.
  - **Example**:
    ```javascript
    const obj = {
      name: 'Alice',
      greet: () => {
        console.log('Hello, ' + this.name); // `this` is not obj
      }
    };

    obj.greet(); // Hello, undefined
    ```

### 6. Memory Management
- **Garbage collection**
  - **Explanation**: Automatic memory management by reclaiming unused memory.
  - **Example**: The JavaScript engine automatically cleans up objects that are no longer referenced.

- **Memory leaks and how to avoid them**
  - **Explanation**: Unused memory that is not released can lead to performance issues.
  - **Example**:
    ```javascript
    // Avoiding closures holding unnecessary references
    function outer() {
      let obj = { largeData: '...' };

      return function inner() {
        console.log(obj);
      };
    }
    ```

### 7. Event Bubbling and Capturing
- **Event propagation phases**
  - **Explanation**: Event goes through capturing, target, and bubbling phases.
  - **Example**:
    ```javascript
    element.addEventListener('click', event => {
      console.log('Bubbling phase');
    });

    element.addEventListener('click', event => {
      console.log('Capturing phase');
    }, true);
    ```

- **Event delegation**
  - **Explanation**: Attaching a single event listener to a parent element.
  - **Example**:
    ```javascript
    document.body.addEventListener('click', event => {
      if (event.target.matches('button')) {
        console.log('Button clicked');
      }
    });
    ```

- **Preventing default behavior**
  - **Explanation**: Using `event.preventDefault()` to stop default actions.
  - **Example**:
    ```javascript
    link.addEventListener('click', event => {
      event.preventDefault();
      console.log('Link click prevented');
    });
    ```

### 8. Functional Programming
- **Pure functions**
  - **Explanation**: Functions with no side effects and consistent output for the same input.
  - **Example**:
    ```javascript
    function add(a, b) {
      return a + b;
    }
    ```

- **Immutability**
  - **Explanation**: Data cannot be changed once created.
  - **Example**:
    ```javascript
    const arr = [1, 2, 3];
    const newArr = [...arr, 4];
    ```

- **Higher-order functions**
  - **Explanation**: Functions that operate on other functions.
  - **Example**:
    ```javascript
    function higherOrder(fn, value) {
      return fn(value);
    }

    higherOrder(console.log, 'Hello');
    ```

- **Function composition**
  - **Explanation**: Combining multiple functions to create a new function.
  - **Example**:
    ```javascript
    const compose = (f, g) => x => f(g(x));
    const add1 = x => x + 1;
    const double = x => x * 2;
    const add1ThenDouble = compose(double, add1);
    console.log(add1ThenDouble(5)); // 12
    ```

### 9. Module Systems
- **CommonJS**
  - **Explanation**: Module system used in Node.js.
  - **Example**:
    ```javascript
    // module1.js
    module.exports = function() {
      console.log('Hello from CommonJS');
    };

    // module2.js
    const greet = require('./module1');
    greet();
    ```

- **AMD**
  - **Explanation**: Asynchronous Module Definition, used in browsers.
  - **Example**:
    ```javascript
    define(['module1'], function(module1) {
      module1();
    });
    ```

- **ES6 modules**
  - **Explanation**: Standardized module system in JavaScript.
  - **Example**:
    ```javascript
    // module1.js
    export const greet = () => console.log('Hello from ES6 module');

    // module2.js
    import { greet } from './module1';
    greet();
    ```

- **Module bundlers (Webpack, Rollup)**
  - **Explanation**: Tools to bundle JavaScript modules for usage in a browser.
  - **Example**: Webpack can bundle multiple modules into a single file for deployment.

### 10. Design Patterns
- **Singleton**
  - **Explanation**: Ensures a class has only one instance.
  - **Example**:
    ```javascript
    const singleton = (function() {
      let instance;

      function createInstance() {
        return new Object('I am the instance');
      }

      return {
        getInstance: function() {
          if (!instance) {
            instance = createInstance();
          }
          return instance;
        }
      };
    })();

    const instance1 = singleton.getInstance();
    const instance2 = singleton.getInstance();
    console.log(instance1 === instance2); // true
    ```

- **Factory**
  - **Explanation**: Creates objects without specifying the exact class.
  - **Example**:
    ```javascript
    class Car {
      constructor(model) {
        this.model = model;
      }
    }

    class CarFactory {
      createCar(model) {
        return new Car(model);
      }
    }

    const factory = new CarFactory();
    const car = factory.createCar('Tesla');
    console.log(car.model); // Tesla
    ```

- **Observer**
  - **Explanation**: A subject notifies observers about state changes.
  - **Example**:
    ```javascript
    class Subject {
      constructor() {
        this.observers = [];
      }

      addObserver(observer) {
        this.observers.push(observer);
      }

      notifyObservers(message) {
        this.observers.forEach(observer => observer.update(message));
      }
    }

    class Observer {
      update(message) {
        console.log(message);
      }
    }

    const subject = new Subject();
    const observer1 = new Observer();
    const observer2 = new Observer();

    subject.addObserver(observer1);
    subject.addObserver(observer2);

    subject.notifyObservers('Hello Observers');
    ```

### 11. Performance Optimization
- **Debouncing and throttling**
  - **Explanation**: Controlling the rate at which a function is executed.
  - **Example**:
    ```javascript
    function debounce(func, delay) {
      let timeout;
      return function() {
        clearTimeout(timeout);
        timeout = setTimeout(() => func.apply(this, arguments), delay);
      };
    }

    function throttle(func, limit) {
      let inThrottle;
      return function() {
        if (!inThrottle) {
          func.apply(this, arguments);
          inThrottle = true;
          setTimeout(() => (inThrottle = false), limit);
        }
      };
    }
    ```

- **Lazy loading**
  - **Explanation**: Deferring the loading of resources until they are needed.
  - **Example**:
    ```javascript
    document.addEventListener('DOMContentLoaded', function() {
      const lazyImages = document.querySelectorAll('img.lazy');

      const lazyLoad = () => {
        lazyImages.forEach(img => {
          if (img.getBoundingClientRect().top < window.innerHeight && img.getBoundingClientRect().bottom > 0) {
            img.src = img.dataset.src;
            img.classList.remove('lazy');
          }
        });
      };

      lazyLoad();
      window.addEventListener('scroll', lazyLoad);
    });
    ```

- **Code splitting**
  - **Explanation**: Breaking down code into smaller chunks to be loaded on demand.
  - **Example**: Webpack allows dynamic imports to achieve code splitting.

- **Memory management**
  - **Explanation**: Efficiently managing memory usage to avoid leaks and improve performance.
  - **Example**: Using weak references and avoiding unnecessary global variables.

### 12. Security
- **Cross-Site Scripting (XSS)**
  - **Explanation**: Injecting malicious scripts into web pages.
  - **Example**:


    ```javascript
    const userInput = '<script>alert("XSS")</script>';
    const sanitizedInput = userInput.replace(/</g, '&lt;').replace(/>/g, '&gt;');
    document.body.innerHTML = sanitizedInput; // Safe
    ```

- **Cross-Site Request Forgery (CSRF)**
  - **Explanation**: Unauthorized commands are transmitted from a user that the web application trusts.
  - **Example**: Using anti-CSRF tokens in forms to prevent CSRF attacks.

- **SQL Injection**
  - **Explanation**: Inserting malicious SQL queries into input fields.
  - **Example**:
    ```javascript
    const userInput = "'; DROP TABLE users; --";
    const query = `SELECT * FROM users WHERE name = '${userInput}'`;
    // Use parameterized queries to prevent SQL injection
    ```

- **Content Security Policy (CSP)**
  - **Explanation**: Mitigating XSS attacks by specifying allowed content sources.
  - **Example**: Setting `Content-Security-Policy` header in HTTP responses.

## Advanced Topics

### 1. Web Components
- **Custom elements**
  - **Explanation**: Defining new HTML elements.
  - **Example**:
    ```javascript
    class MyElement extends HTMLElement {
      constructor() {
        super();
        this.attachShadow({ mode: 'open' });
        this.shadowRoot.innerHTML = '<p>My custom element</p>';
      }
    }

    customElements.define('my-element', MyElement);
    ```

- **Shadow DOM**
  - **Explanation**: Encapsulating styles and markup.
  - **Example**:
    ```javascript
    class MyElement extends HTMLElement {
      constructor() {
        super();
        this.attachShadow({ mode: 'open' });
        this.shadowRoot.innerHTML = '<style>p { color: red; }</style><p>Styled text</p>';
      }
    }

    customElements.define('my-element', MyElement);
    ```

- **HTML templates**
  - **Explanation**: Defining reusable HTML templates.
  - **Example**:
    ```html
    <template id="my-template">
      <p>Template content</p>
    </template>

    <script>
      const template = document.getElementById('my-template').content.cloneNode(true);
      document.body.appendChild(template);
    </script>
    ```

### 2. Service Workers
- **Caching and offline capabilities**
  - **Explanation**: Enhancing performance and offline access by caching resources.
  - **Example**:
    ```javascript
    self.addEventListener('install', event => {
      event.waitUntil(
        caches.open('my-cache').then(cache => {
          return cache.addAll(['/index.html', '/styles.css']);
        })
      );
    });

    self.addEventListener('fetch', event => {
      event.respondWith(
        caches.match(event.request).then(response => {
          return response || fetch(event.request);
        })
      );
    });
    ```

- **Push notifications**
  - **Explanation**: Sending notifications to users even when the web app is not active.
  - **Example**: Using the Push API and Notification API to send and display notifications.

- **Background sync**
  - **Explanation**: Synchronizing data in the background.
  - **Example**: Using the Background Sync API to defer actions until the user has stable connectivity.

### 3. WebAssembly
- **Introduction to WebAssembly**
  - **Explanation**: A binary instruction format for executable programs on the web.
  - **Example**: Compiling C/C++ code to WebAssembly for performance-critical parts of a web app.

- **Use cases**
  - **Explanation**: When to use WebAssembly.
  - **Example**: High-performance applications like games, image processing, and video editing.

- **Loading and using WebAssembly modules**
  - **Explanation**: Integrating WebAssembly with JavaScript.
  - **Example**:
    ```javascript
    fetch('module.wasm').then(response => response.arrayBuffer()).then(bytes => WebAssembly.instantiate(bytes)).then(results => {
      const instance = results.instance;
      console.log(instance.exports.exportedFunction());
    });
    ```

### 4. GraphQL
- **Introduction to GraphQL**
  - **Explanation**: A query language for APIs.
  - **Example**: Defining a GraphQL schema and queries for flexible data retrieval.

- **Setting up a GraphQL server**
  - **Explanation**: Creating a server to handle GraphQL queries.
  - **Example**:
    ```javascript
    const { ApolloServer, gql } = require('apollo-server');

    const typeDefs = gql`
      type Query {
        hello: String
      }
    `;

    const resolvers = {
      Query: {
        hello: () => 'Hello world'
      }
    };

    const server = new ApolloServer({ typeDefs, resolvers });

    server.listen().then(({ url }) => {
      console.log(`🚀 Server ready at ${url}`);
    });
    ```

- **Writing GraphQL queries and mutations**
  - **Explanation**: Defining and executing queries and mutations.
  - **Example**:
    ```graphql
    query {
      hello
    }

    mutation {
      addUser(name: "Alice") {
        id
        name
      }
    }
    ```

### 5. TypeScript
- **Introduction to TypeScript**
  - **Explanation**: A typed superset of JavaScript.
  - **Example**: Type annotations for variables and function parameters.

- **Type annotations**
  - **Explanation**: Adding type information to variables and functions.
  - **Example**:
    ```typescript
    let count: number = 5;

    function greet(name: string): string {
      return 'Hello, ' + name;
    }
    ```

- **Interfaces and classes**
  - **Explanation**: Defining interfaces and classes for type-safe code.
  - **Example**:
    ```typescript
    interface Person {
      name: string;
      age: number;
    }

    class Student implements Person {
      name: string;
      age: number;
      grade: string;

      constructor(name: string, age: number, grade: string) {
        this.name = name;
        this.age = age;
        this.grade = grade;
      }
    }

    const student: Person = new Student('Alice', 20, 'A');
    ```

- **Generics**
  - **Explanation**: Creating reusable components with generics.
  - **Example**:
    ```typescript
    function identity<T>(value: T): T {
      return value;
    }

    let num = identity<number>(42);
    let str = identity<string>('Hello');
    ```

- **TypeScript with React**
  - **Explanation**: Using TypeScript in a React application.
  - **Example**: Adding type annotations to React components and props.
    ```typescript
    import React from 'react';

    interface Props {
      name: string;
      age: number;
    }

    const Greeting: React.FC<Props> = ({ name, age }) => (
      <div>
        <p>Hello, {name}. You are {age} years old.</p>
      </div>
    );

    export default Greeting;
    ```