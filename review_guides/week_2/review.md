# Week 2 - Automated UI Testing with Java

## Git Fundamentals
---
### Introduction
---
- **Git Fundamentals**
    - Git is a version control system used for tracking changes in source code during software development
    - Fundamental concepts:
        - **Repository**
            - A repository is a central location where the code and related files for a project are stored.
        - **Clone**
            - The process of creating a copy of a repository on your local machine is known as cloning.
        - **Commit**
            - A commit is a snapshot of changes made to the codebase. Commits are used to track the history of changes in the code.
        - **Branch**
            - A branch is a parallel version of the codebase, used to work on new features or bug fixes independently without affecting the main codebase.
        - **Merge**
            - Merging is the process of integrating changes made in one branch into another branch.
        - **Push**
            - Pushing is the process of uploading the changes made to the local repository to the remote repository.
        - **Pull**
            - Pulling is the process of downloading the changes made in the remote repository to the local repository.
        - **Remote**
            - A remote is a repository that is stored on a server or online service like GitHub, which can be accessed and managed from a local machine.
- **Initializing A Repository**
    - To initialize a Git repository, you can run the command `git init` in the root directory of your project. 
    - This will create a `.git` directory where Git will store all of the version control information for your project.
- **Staging Process**
    - The process of preparing changes to be committed to the repository
    - Before committing changes, developers can review and selectively choose which changes to include in the commit
    - The staging area acts as a buffer between the working directory (where changes are made) and the repository (where changes are comitted)
        - The staging process has these steps:
            1. Modify files in the working directory
            2. Use the `git add` command to stage changes for the next commit
            3. Use the `git status` command to review the changes that have been staged
            4. Use the `git commit` command to commit the staged changes to the repository
                - A git commit requires a message to be added to it for other developers (and yourself) to be able to refer back to and see what the commit is doing
- **Pushing To A Remote Repository**
    - To push your changes to a remote Git repository, you can use the `git push` command. 
    - For example: 
        - You want to push your changes to a repository hosted on GitHub, you can run:
            - `git push origin main` 
            > Assuming `origin` is the name of the remote repository and `main` is the name of the branch you want to push to
- **Git Common Commands**
    - These are basic Git commands that developers use to manage their Git repositories.
    - `git add`
        - Used to add changes to the current git repository to staging 
    - `git commit`
        - Used to commit changes to the repository
    - `git branch`
        - Used to create and manage branches
    - `git merge`
        - Used to merge changes from one branch to another
    - `git push`
        - Used to push changes to a remote repository
    - `git pull`
        - Used to pull changes from a remote repository.
- **Source Control Management**
    - There are different types of version control systems, including Git, SVN, CVS, and Mercurial. 
    - Git is a distributed version control system, which means that every developer has their own copy of the repository on their local machine.

## HTML/CSS
---
### HTML Foundation
---
- **Overview of HTML**
    - HTML (Hypertext Markup Language) is a markup language used to create web pages and web applications
    - It consists of a series of tags and attributes that define the structure and content of a web page
    - It provides a way to structure the content on the web and is essential to web development
- **HTML-Tags**
    - HTML tags are used to structure web pages. 
    - For example, the `<h1>` tag is used for the main heading of a page, while the `<p>` tag is used for paragraphs.
- **HTML-Document-Structure-and-DOM**
    - HTML document structure refers to the hierarchy of elements that make up an HTML document
    - It determines the order in which elements are displayed on the page and how they are related to each other
    - The Document Object Model (DOM) is a programming interface for web documents
        - It represents the page so that programs can change the document structure, style, and content
        - The DOM is represented by nodes and objects
    - The HTML document structure and the DOM are closely related, as the structure of the HTML document is represented by the DOM
        - Each HTML element is represented by a node in the DOM
- **Elements-and-Attributes**
    - HTML elements are modified using attributes. 
    - For example, the `href` attribute is used to specify the URL of a hyperlink
        - ```html
          <a href="https://google.com">Visit Google</a>
    - Two important attributes are `class` and `id`
        - `class`
            - Used to group elements together with similar characteristics
            - Allows developers to apply the same styles to multiple elements on a page
        - `id`
            - Used to identify a specific element on the page
            - Unlike `class`, each element can only have one `id` attribute as it is intended to be unique
        - ```html
          <button class="return">Return</button>
          <img id="logo" src="logo.png">
- **Inline and Block Elements**
    - Elements can be classified as either block-level elements or inline elements based on their default display behavior
    - **Block-level**
        - Elements that are formatted visually as a block, taking up the full width of their parent container by default
        - They begin on a new line and are stacked vertically from top to bottom
        - Examples: `<div>`, `<p>`, `<h1>`, `<ul>`, `<li>`, etc
    - **Inline**
        - Elements that are formatted to be inline with the surrounding content, taking up only as much space as necessary
        - They do not start on a new line and are often used within block-level elements to add additional content or formatting
        - Examples: `<span>`, `<a>`, `<em>`, etc.
- **Common-tags**
    - Commonly used HTML tags include
        - `<html>`
            - Root of the HTML document which is used to specify that the document is HTML
        - `<head>`
            - Used to contain all the head elements in the HTML file
            - Usually contains `<title>`, `<style>`, `<meta>`, etc
        - `<body>`
            - Used to define the body of an HTML document
            - Usually contains visible elements like `<img>`, `<table>`, etc
        - `<h1>` - `<h6>`
            - Usd to define the heading size
        - `<p>`
            - Used to define the paragraph content
        - `<li>`
            - Used to list content
        - `<img>`
            - Used to include an image in the page
        - etc
### CSS Foundation
---
- **Overview-of-CSS**
    - CSS or Cascading Style sheets, is used to describe the presentation of HTML documents
    - Web developers can separate the presentation of the web page from its content, to make it easier to change the layout and appearance
    - CSS styles are applied to HTML elements using selectors, which act as rules to specify what is styled and what is not
- **Inline, Internal and External Stylesheets**
    - CSS can be applied to HTML documents in a number of ways, including:
        - **Inline styles**
            - CSS code can be added directly to HTML elements using the style attribute.
        - **Internal styles**
            - CSS code can be added to a style element within the head section of an HTML document.
        - **External styles**
            - CSS code can be placed in a separate .css file and linked to the HTML document using the link element.
    - Styles can be cascaded and overridden using inheritance and specificity
    - The order in which the styles take precedence over each other is: Inline, Internal, then External
        - Inline styles will override internal, and internal overrides external
- **CSS Properties**
    - Here are the most common properties that can be used to style HTML elements:
        - `color`: sets the color of text
        - `background-color`: sets the background color of an element
        - `font-family`: sets the font family of text
        - `font-size`: sets the size of text
        - `font-weight`: sets the weight (boldness) of text
        - `text-align`: sets the alignment of text within an element
        - `line-height`: sets the height of a line of text
        - `padding`: sets the space between the content of an element and its border
        - `margin`: sets the space between an element and its neighboring elements
        - `border`: sets the style, width, and color of an element's border
        - `border-radius`: sets the radius of an element's corners
- **Element-selectors**
    - Element selectors are used to select HTML elements for styling. 
    - For example, the `p` selector selects all `<p>` elements.
        - ```css
        p {
            color: red;
        }
- **Class-and-ID-selectors**
    - Class and ID selectors are used to select HTML elements based on their class or ID attributes. 
    - ```css
      /* Style all elements with class "return" */
      .return {
        background-color: blue;
        color: white;
        padding: 10px 20px;
        border-radius: 5px;
      }  
      /* Style the element with ID "logo" */
      #logo {
        width: 200px;
        height: 100px;
      }
    - Class selector `.return` and an ID selector `#logo`
    - To apply a Class or ID to an element, you have to define the attribute in the element
- **CSS Box Model**
    - The CSS Box Model is a fundamental part of CSS, it describes the structure and behavior of HTML elements
    - Every HTML element is considered to be a rectangular box, and this box has four distinct areas:
        - **Content area**
            - This is where the actual content of the element is displayed, such as text, images, or video.
        - **Padding area**
            - This is the space between the content area and the element's border. Padding can be used to add space around the content, or to separate the content from the border.
        - **Border area**
            - This is the line that surrounds the padding area. The border can be styled with different colors, widths, and styles.
        - **Margin area**
            -This is the space between the border of an element and the adjacent elements. Margins can be used to create space between elements, or to center an element within its container.
### CSS Depth
---
- **Sibling-selectors**
    - Sibling selectors are used to target an element that comes immediately after another element
    - The selector uses the `+` symbol to target the next sibling element
        - ```css
          h1 + p {
            font-size: 1.2rem;
          }
        - This will target the first paragraph element that comes after a heading element
- **Advanced-selectors**
    - Used to target elements based on more complex relationships with other elements
    - There are several types:
        - **Descendant Selectors**
            - Targets an element that is a descendant of another element
            - It uses a space between two elements to indicate the relationship
            - ```css
              article p {
                font-size: 1.2rem;
              }
            - This code targets all paragraph elements that are descendants of an article element
        - **Child Selectors**
            - Targets an element that is a direct child of another element
            - It uses the `>` symbol to indicate the relationship
            - ```css
              article > p {
                font-size: 1.2rem;
              }
            - This code targets all paragraph elements that are direct children of an article element
### HTML Forms
---
- **Form Elements and Attributes**
    - HTML forms allow users to input and submit data to a website
    - `<form>`: The container for a form on a webpage
    - `action`: Attribute used to specify the URL where form data is sent upon submission
    - `method`: Attribute used to specify the HTTP method used to send form data (typically GET or POST)
    - `name`: Attribute used to assign a name to a form
    - Here is an example:
        - ```html
          <form action="/submit-form" method="post">
            <label for="name">Name:</label>
            <input type="text" id="name" name="name" required>
          
            <label for="email">Email:</label>
            <input type="email" id="email" name="email" required>
          
            <label for="password">Password:</label>
            <input type="password" id="password" name="password" required>
          
            <button type="submit">Submit</button>
          </form>
- **Input Elements and Input Types**
    - Input elements are used to create form fields that users can fill out with data
        - `text`: A single-line text input field
        - `password`: A single-line text input field with obscured characters
        - `email`: A single-line text input field used for email addresses
        - `tel`: A single-line text input field used for telephone numbers
        - `number`: A single-line text input field used for numeric data
        - `date`: A single-line text input field used for dates
        - `checkbox`: A checkbox input field
        - `radio`: A radio button input field
        - `file`: A file upload input field
        - `submit`: A button used to submit a form
        - `reset`: A button used to reset form input fields
        - `button`: A generic button
- **Submitting Forms**
    - Forms can be submitted in two main ways: GET and POST requests
    - When a form is submitted with a GET request, the form data is sent in the URL as query parameters
    - When a form is submitted with a POST request, the form data is sent in the request body
- **Select and Multi-Select**
    - Select elements allow users to select an option from a list
    - Multi-select elements allow users to select multiple options from a list
    - `<select>`: The container for a select element
    - `<option>`: An option in a select element
    - `selected`: Attribute used to specify the default selected option in a select element
    - `multiple`: Attribute used to specify that multiple options can be selected in a select element
    - Here is an example:
        - ```html
          <label for="cars">Choose a car:</label>
          <select id="cars" name="cars">
            <option value="volvo">Volvo</option>
            <option value="saab">Saab</option>
            <option value="fiat">Fiat</option>
            <option value="audi">Audi</option>
          </select>
          
          <label for="fruits">Choose your favorite fruits:</label>
          <select id="fruits" name="fruits" multiple>
            <option value="apple">Apple</option>
            <option value="banana">Banana</option>
            <option value="orange">Orange</option>
            <option value="kiwi">Kiwi</option>
          </select>
## Java Slim
---
### Java Orientation
---
- **Language Overview**
    - Java is a programming language used for software development
    - Java is an object-oriented language
        - It is based on the concepts of objects, which are instances of classes that encapsulate data and behavior
    - Java is platform-independent so the same code can be run on multiple platforms without modification
- **JDK, JRE, JVM**
    - **Java Development Kit**
        - Software development kit used for developing Java applications
    - **Java Runtime Environment**
        - Software environment used for running Java applications
    - **Java Virtual Machine**
        - A virtual machine that runs Java bytecode
    - The JDK includes teh JRE, as well as a set of tools and libraries for developing Java apps, like:
        - Java Compiler
        - Java Debugger
    - The JRE includes the JVM, as well as libraries and tools for running Java applications, but does **not** include the development tools
    - The JVM is responsible for executing Java bytecode
        - The compiled form of Jva code
    - Java applications are written in Java code, which is compiled to Java bytecode using the Java compiler in the JDK
    - The Java bytecode is then executed by the JVM, which translates it into machine code that can be run on the underlying hardware and operating system
- **Compilation Process**
    - Java code is written in plain text using a text editor or IDE and saved as a `.java` file
    - The compiler checks the syntax and semantics of the code then generates bytecode for the JVM to execute
    - The bytecode is saved in a file with the `.class` extension which can be executed on any platform that has a JVM installed
    - The bytecode is not machine code, it is an intermediate that can be translated into machine code by the JVM at runtime
### Java Basics
---
- **Primitive Types**
    - Java has 8 primitive data types, used to represent basic values
    - Primitives are stored directly in memory, which makes them faster to access and more efficient than objects
        - `boolean`
            - represents a single bit of information, and can have values of `true` or `false`
        - `byte`
            - 8-bit integer
        - `short`
            - 16-bit integer
        - `int`
            - 32-bit integer
        - `long`
            - 64-bit integer
        - `float`
            - 32-bit floating point number
        - `double`
            - 64-bit floating point number
        - `char`
            - Single 16-bit unicode character
    - Java has corresponding wrapper classes for each primitive type
        - Used to convert between primitive types and objects
- **Working with Basic Operators**
    - Java has a variety of operators that can be used to perform arithmetic, logical, and bitwise operations.
        - **Arithmetic Operators**
            - Addition `+`
                - `5 + 5`
            - Subtraction `-`
                - `10 - 4`
            - Multiplication `*`
                - `4 * 4`
            - Division `/`
                - `5 / 3`
            - Modulus `%`
                - Modulus is finding the remainder after division
                - `5 % 2` would be 1
            - Increment `++`
                - Increases the value of a variable by 1
            - Decrement `--`
                - Decreases the value of a variable by 1
        - **Logical Operators**
            - Logical operators are used to determine the logic between variables or values
                - And `&&`
                - Or `||`
                - Not `!`
        - **Comparison Operators**
            - Comparison operators are used to compare two values or variables
            - This lets us find answers and make decisions
            - The return value of a comparison is either `true` or `false`
                - Equal to `==`
                - Greater than `>`
                - Greater than or equal to `>=`
                - Less than `<`
                - Less than or equal to `<=`
        - **Bitwise Operators**
            - These are not used commonly, but are for operations on binary values
                - And (&)
                - Or (|)
                - Exclusive or (^)
                - Shift left (<<)
                - Shift right (>>)
                - Unsigned shift right (>>>)
        - **Assignment Operators**
            - Assignment (=)
                - `x = 5`
            - `+=`
                - `x += 3` is the same as `x = x + 3`
            - `-=`
                - `x -= 3` is the same as `x = x - 3`
            - `*=`
                - `x *= 3` is the same as `x = x * 3`
            - `/=`
                - `x /= 3` is the same as `x = x / 3`
            - `%=`
                - `x %= 3` is the same as `x = x % 3`
    - Operators can be used with variables, literals, and expressions to perform various computations
    - The order of operations, or operator precedence, determines the order in which operators are evaluated
    - Parenthesis override the default order of operations
- **Flow Control Statements**
    - Flow control statements are used to control the order in which statements are executed in a Java program
    - Here are the common ones:
        - `if` statement is used to test a condition and execute different code depending on the result:
            - ```java
              if (x > 5) {
                System.out.println("x is greater than 5");
              } else {
                System.out.println("x is less than or equal to 5");
              }
        - `for` statement is used to loop through a block of code a specified number of times
            - ```java
              for (int i = 0; i < 10; i ++){
                System.out.println(i);
              }
        - `while` statement is used to loop through a block of code as long as a condition is true
            - ```java
              int i = 0;
              while(i < 10){
                System.out.println(i);
                i++;
              }
        - `do-while` statement is used like the `while` loop, however it always executes the block at least once
            - ```java
              int i = 0;
              do{
                System.out.println(i);
                i++
              } while(i < 10);
        - `switch` statement is used to select one of many blocks of code to execute based on the value of an expression
            - ```java
              int chosenFlavor = 2;
              switch (chosenFlavor){
                case 1:
                    System.out.println("Chocolate is your favorite!");
                    break;
                case 2:
                    System.out.println("Vanilla is your favorite!");
                    break;
                default:
                    System.out.println("You have not chosen a valid flavor!");
                    break;
              }
    - Flow control can be nested and combined to create complex programs
    - Be careful not to create infinite loops
- **Arrays**
    - This is a data structure used to store a fixed number of elements of the same type
    - To declare an array, you must specify the type of the elements and the number of elements in the array
        - ```java
          int[] numbers = new int[5];
        - This declares an array named `numbers` that can store 5 integer values
        - You can also declare an array and instantiate it with values at the same time
        - ```java
          int[] numbers = {1, 2, 3, 4, 5};
        - Note the use of `{}` instead
    - Arrays in Java are zero-indexed, meaning the first element in the array has an index of 0, the second is 1, and so forth
    - To access an eelemnt from the array, we use the square bracket notation
        - `numbers[0]` would access the first element of the numbers array
    - You can assign values to arrays with the square bracket notation and the assignment operator
        - `numbers[0] = 42` assigns the value of 42 to the first element of the `numbers` array
- **Debugging**
    - It is the process of finding and fixing errors in software code
    - It is an invaluable skill for any developer, and there are a number of tools that can aid in the process
    - Common debugging techniques:
        - **Using print statements**
            - The simplest and most common way of debugging
            - You can add print statements to your code to see the value of variables or to check if a certain block of code is executed
            - ```java
              int x = 5;
              System.out.println("Value of x: " + x);
        - **Using a Debugger**
            - A debugger is a tool that allows you to step through your code line by line, set breakpoints, and examine variables and their values at each step
            - This is typically in built in your IDE
        - **Exception Handling**
            - Exceptions are a way of handling errors that occur during program executions
            - Try-Catch blocks can catch exceptions and print out their error messages to help debug your code
            - ```java
              try{
                int[] arr = {1, 2, 3};
                System.out.println(arr[3]);
              }catch(Exception e){
                System.out.println(e);
              }
- **Variable scopes**
    - Variable scopes refer to the range within which a variable can be accessed or used
    - The scope of the variable is determined by where it is declared in the code
    - There are four types of variable scopes in Java:
        - **Class Level Scope**
            - Variables declared at the class level have class-level scope
            - This means they can be accessed by any method in the class
            - ```java
              public class MyClass{
                int myVariable = 20;

                public void printVariable(){
                    // Accessing variable
                    System.out.println("Variable value: " + myVariable);
                }
              }
        - **Method Level Scope**
            - Variables declared inside a method have method-level scope
            - They can only be accessed within the method they are declared in
            - ```java
              public class MyClass {
                  public static void main(String[] args) {
                      int myVariable = 10;
              
                      if (myVariable == 10) {
                          // Accessing variable declared inside if block
                          int anotherVariable = 20;
                          System.out.println("Variable value: " + anotherVariable);
                      }
              
                      // This will give compilation error as the variable is out of scope
                      // System.out.println("Variable value: " + anotherVariable);
                  }
              }
        - **Block Level Scope**
            - Variables declared inside a block, such as a loop or if statement, have block level scope
            - They can only be accessed within the block they are declared in
            - A block is anything that is between two curly braces `{}`
            - ```java
              public class MyClass {
                  public static void main(String[] args) {
                      for (int i = 0; i < 5; i++) {
                          // Accessing variable declared inside for loop block
                          int myVariable = i;
                          System.out.println("Variable value: " + myVariable);
                      }
              
                      // This will give compilation error as the variable is out of scope
                      // System.out.println("Variable value: " + myVariable);
                  }
              }
### Java Methods
---
- **Testing through the main() method**
    - Testing approach where the test cases are executed through the `main()` method of a Java program
    - This is also known as the Application Testing approach
    - Steps to follow it:
        - Create a separate Java class for testing that only contains a `main()` method that will execute test cases
        - Import the Java classes to be tested
        - Write test cases that cover all the functionality of the Java classes being tested
        - Execute the test cases by running the `main()` method
        - Verify the results
### Java Classes
---
- **Inheritance**
    - A way of creating a new class from an existing one by inheriting the properteis and behaviors of the existing class
    - Allows for code reuse and helps with creating a hierarchy of classes
    - ```java
      public class Animal {
        public void eat(){
            System.out.printlng("The animal is eating");
        }
      }

      public class Dog extends Animal{
        public void bark(){
            System.out.printlng("The dog barks!");
        }
      }
- **Polymorphism**
    - The ability of objects to take on different forms and behave differently based on their context
    - Achieved through method overriding and method overloading
    - ```java
      public class Vehicle {
        public void makeSound(){
            System.out.println("The vehicle makes a sound");
        }
      }

      public class Car extends Vehicle {
        // Overriding the makeSound inherited from Vehicle
        public void makeSound(){
            System.out.println("The Car goes vroom!");
        }
      }
- **Encapsulation**
    - The idea of bundling data and methods that operate on that data within a single unit or class, and controlling access to that data through access modifiers
    - Helps with creating more secure and maintainable code
    - ```java
      public class Person{
        private String name;
        private int age;

        public String getName(){
            return name;
        }

        public void setName(String name){
            this.name = name;
        }

        public int getAge(){
            return age;
        }

        public void setAge(int age){
            this.age = age;
        }
      }
- **Abstraction**
    - The process of hiding complex implementation details and providing a simplified view of a system or component to its users
    - Helps with managing complexity and making code more reusable and maintainable
    - ```java
      public abstract class Animal {
        public abstract void makeSound();
      }

      public class Dog extends Animal {
        public void makeSound(){
            System.out.println("The Dog Barks!");
        }
      }
- **Classes and Objects**
    - **Class**
        - The blueprint or template for creating objects
            - An object is an instance of a class
        - Classes contain attributes (fields/properties) and methods that define the behaviors of objects
        - ```java
          public class Person {
            private String name;
            private int age;

            public Person(String name, int age){
                this.name = name;
                this.age = age;
            }

            public void sayHello(){
                System.out.println("Hello, my name is " + name);
            }
          }
    - **Objects**
        - Objects are instances of classes, and take on the properties given to it in classes
        - Objects are instantiated using the `new` keyword and a reference to the class that is used as the template to instantiate it
        - Objects occupy the heap in memory, and are referred to using their reference
        - If an object reference goes out of scope, or is not assigned to an object then it will be removed from memory
            - For example, if an object is created inside of a method, once the method is finished and the object reference is not returned, the object in memory will be removed
        - ```java
          Person person = new Person("John", 30);
          person.sayHello(); // Outputs: Hello, my name is John
- **Interfaces**
    - In Java, an interface is a collection of abstract methods that are used to define a set of behaviors that a class can implement
    - An interface is defined using the `interface` keyword
    - An interface can contain:
        - Constants
        - Abstract methods
        - Default methods
        - Static methods
    - ```java
      public interface MyInterface {
        // constant declarations
        int MAX_SIZE = 100;
        String DEFAULT_NAME = "John";

        // abstract method signatures
        void doSomething();
        String getName();

        // default method implementations
        default void doSomethingElse() {
            System.out.println("Doing something else");
        }

        // static method signatures
        static void printHello() {
            System.out.println("Hello");
        }
      }
    - An interface cannot be instantiated, instead it needs to be `implemented` by another class
    - When a class implements an interface, it must implement any `abstract` methods declared
    - ```java
      public class MyClass implements MyInterface {
        public void doSomething(){
            System.out.println("Do Something!");
        }
      }
- **Abstract Classes**
    - An abstract class is a class that cannot be instantiated and is typically used as a base class for other classes to extend
    - An Abstract class can contain:
        - Instance variables
        - Abstract methods
        - Concrete methods
        - Constructors
    - An abstract class cannot be instantiated however, and must be extended by another class in order to access the properties inside it
    - ```java
      public abstract class Shape {
          private String color;
          
          public Shape(String color) {
              this.color = color;
          }
          
          public String getColor() {
              return color;
          }
          
          public void setColor(String color) {
              this.color = color;
          }
          
          public abstract double getArea();
          
          public abstract double getPerimeter();
          
          public void printDetails() {
              System.out.println("Color: " + color);
              System.out.println("Area: " + getArea());
              System.out.println("Perimeter: " + getPerimeter());
          }
          
          // Concrete method
          public double calculateDiameter(double radius) {
              return radius * 2;
          }
      }
    - The `Shape` class is declared as `abstract`
    - It contains an instance variable `color`
    - There are two abstract methods `getArea()` and `getPerimeter()` that have no implementation
- **Constructors**
    - This is a special method that is called when an object of a class is created
    - It is used to initialize the object's attributes and perform any necessary setup
    - It can be overloaded to provide different ways of creating objects
    - ```java
      public class Person{
        private String name;
        private int age;

        public Person(String name, int age){
            this.name = name;
            this.age = age;
        }

        public Person(String name){
            this.name = name;
            this.age = 0;
        }

        public Person(int age){
            this.name = "Empty";
            this.age = age;
        }
      }

      Person person1 = new Person("John", 30);
      Person person2 = new Person("Mike");
      Person person3 = new Person(30);
    - The constructor method will be called based on the arguments passed into it
- **Access Modifiers**
    - Access Modifiers define the level of access to a class, method, or variable
    - There are four access modifiers in Java
        - `public`
            - A public class, method, or variable can be accessed from anywhere in the program
            - It has the widest scope
        - `private`
            - A private class, method, or variable can only be accessed with the same class in which it is declared
        - `protected`
            - A protected class, method, or variable can only be accessed within the same package or by subclasses in other packages
        - `default` (no modifier)
            - A class, method, or variable with no access modifier is only accessible within the same package
    - ```java
      public class Car {
          private String make;
          protected String model;
          int year;
          public String color;
          
          public Car(String make, String model, int year, String color) {
              this.make = make;
              this.model = model;
              this.year = year;
              this.color = color;
          }
          
          private void startEngine() {
              // code to start the engine
          }
          
          protected void accelerate() {
              // code to accelerate the car
          }
          
          void stop() {
              // code to stop the car
          }
          
          public static void main(String[] args) {
              Car myCar = new Car("Toyota", "Camry", 2022, "Blue");
              myCar.startEngine(); // this will not compile because startEngine() is private
              myCar.accelerate(); // this is allowed because accelerate() is protected
              myCar.stop(); // this is allowed because stop() is default (no modifier)
              System.out.println(myCar.color); // this is allowed because color is public
          }
      }
- **Non Access Keywords**
    - Non-access keywords are used in Java for defining different aspects of a class or method
    - Some common non-access keywords are:
        - `final`
            - When applied to a variable, it indicates that the value of the variable cannot be changed once assigned
            - When applied to a method, it indicates that the method cannot be overridden by a subclass
            - When applied to a class, it indicates that the class cannot be subclassed
        - `static`
            - Indicates that a member variable or method belongs to the class instead of the instance of the class
            - This means it can be accessed without creating an instance of the class
            - ```java
              public final class MyConstants {
                  public static final int MAX_SIZE = 100;
                  public static final String MESSAGE = "Hello, world!";
              }
        - `abstract`
            - Indicates that a class or method is incomplete and needs to be extended by another class
            - Abstract classes cannot be instantiated, and abstract methods must be implemented by the class that extends the abstract class
### Maven
---
- **Intro to Maven**
    - Maven is a build automation tool for Java projects
    - It automates the build process, including compilation, packaging, and distribution
    - Maven uses a Project Object Model (POM) to manage project dependencies, build profiles, and plugins
- **Central Repository**
    - Maven Central Repository is a public repository of artifacts for use with Maven
    - Artifacts are versioned and can be downloaded and used as dependencies in Maven Projects
- **XML and POM**
    - The Project Object Model (POM) is an XML file that describes a Maven project
    - Contains project metadata, dependencies, build settings, and plugins
    - Allows creation of multiple build profiles for different environments
    - Plugins are used to extend the build process, such as for testing, code coverage, and deployment
## Selenium Webdriver - Java
---
### Orientation
---
- **Selenium WebDriver Introduction**
    - Selenium is a popular open-source test automation tool for web applications
    - Selenium WebDriver is a component of Selenium that allows automation of web browser interactions
    - WebDriver uses browser-specific drivers to control browser interactions
- **Web Element**
    - A web element represents an HTML element on a web page, such as a button, input field, or dropdown
    - Web elements have properties, such as ID, name, class name, tag name, and text
    - WebDriver can locate web elements on a page using different locators, such as ID, name, class name, tag name, CSS selector, and XPath
    - Once a web element is located, WebDriver can perform actions on it, such as clicking, typing, or selecting
### Setup
---
- **WebDriver Configuration**
    - Before using WebDriver, the driver executable for the desired browser needs to be downloaded and configured
    - WebDriver can be configured using system properties, which specify the path to the driver executable and other settings
    - ```java
      import org.openqa.selenium.WebDriver;
      import org.openqa.selenium.chrome.ChromeDriver;
      
      public class WebDriverConfigurationExample {
         public static void main(String[] args) {
            
            // setting the path of the ChromeDriver executable
            System.setProperty("webdriver.chrome.driver", "/path/to/chromedriver");
            
            // creating a new instance of the ChromeDriver
            WebDriver driver = new ChromeDriver();
            
            // navigate to a website
            driver.get("https://www.example.com");
            
            // close the browser
            driver.quit();
         }
      }
- **WebDriverManager**
    - WebDriverManager is a Java library that automates the management of browser drivers for Selenium WebDriver
    - WebDriverManager can automatically download and configure the appropriate driver executable for the desired browser version and operating system
    - ```java
      import io.github.bonigarcia.wdm.WebDriverManager;
      import org.openqa.selenium.WebDriver;
      import org.openqa.selenium.chrome.ChromeDriver;
      
      public class WebDriverManagerExample {
         public static void main(String[] args) {
            
            // setting up the ChromeDriver using the WebDriverManager library
            WebDriverManager.chromedriver().setup();
            
            // creating a new instance of the ChromeDriver
            WebDriver driver = new ChromeDriver();
            
            // navigate to a website
            driver.get("https://www.example.com");
            
            // close the browser
            driver.quit();
         }
      }
### Xpath
---
- **Absolute and Relative Xpath**
    - Xpath is a language used for selecting elements from an XML or HTML document
    - Absolute Xpath specifies the complete path to an element from the root node
    - Relative Xpath specifies the path to an element from any node in the document
    - Example Absolute Xpath: `/html/body/div[2]/form/input[1]`
    - Example Relative Xpath: `//input[@name='username']`
    - ```java
      // Absolute xpath
      WebElement element1 = driver.findElement(By.xpath("/html/body/div[1]/div[2]/form/input[3]"));
      
      // Relative xpath
      WebElement element2 = driver.findElement(By.xpath("//form/input[@name='q']"));
### Locator Strategies
---
- **Locators**
    - Locators are used to identify web elements on a webpage
    - Some examples of locators are:
        - **ID**
            - Used to identify an element with a unique ID attribute
            - ```java
              WebElement element1 = driver.findElement(By.id("element-id"));
        - **Name**
            - Used to identify an element with a name attribute
            - ```java
              WebElement element2 = driver.findElement(By.name("element-name"));
        - **Class name**
            - Used to identify an element with a class attribute
            - ```java
              WebElement element3 = driver.findElement(By.className("element-class"));
        - **Tag name**
            - Used to identify an element by its tag name
            - ```java
              WebElement element4 = driver.findElement(By.tagName("element-tag"));
        - **Link text**
            - Used to identify a hyperlink element by the visible link text
            - ```java
              WebElement element5 = driver.findElement(By.linkText("element-link-text"));
        - **Partial link text**
            - Used to identify a hyperlink element by a partial match of the visible link text
            - ```java
              WebElement element6 = driver.findElement(By.partialLinkText("partial-link-text"));
        - **CSS selector**
            - Used to identify an element by its CSS selector
            - ```java
              WebElement element = driver.findElement(By.cssSelector("#header > h1 > a"));
        - **XPath**
            - Used to identify an element by its XPath
            - Examples shown above for absolute and relative xpath
### Driver Interactions
---
- **`click()`**
    - Used to simulate a click on an element on a webpage
    - ```java
      WebElement button = driver.findElement(By.id("button-id"));
      button.click();
- **`sendKeys()`**
    - Used to simulate typing into an element on a webpage
    - ```java
      WebElement textBox = driver.findElement(By.id("textbox-id"));
      textBox.sendKeys("example text");
- **Implicit Wait**
    - Implicit wait is a setting that waits for a certain amount of time when trying to find an element or elements if they are not immediately available.
    - This setting is applied to the entire lifespan of the WebDriver object and can be set 
    - Implicit wait is useful when the page takes some time to load or the web elements are not immediately visible on the page
    - ```java
      WebDriver driver = new ChromeDriver();
      driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
- **Explicit Wait**
    - Explicit wait is a dynamic wait that waits for a certain condition to occur before moving forward in the test.
    - This wait can be applied to a specific element or multiple elements, and the WebDriver will wait for a certain amount of time for that condition to be met.
    - This wait can be created using the `WebDriverWait` class and is typically combined with an expected condition to be checked.
    - ```java
      WebDriver driver = new ChromeDriver();
      WebDriverWait wait = new WebDriverWait(driver, 10);
      WebElement element = wait.until(ExpectedConditions.elementToBeClickable(By.id("someId")));
- **Fluent Wait**
    - Fluent wait is also a dynamic wait that waits for a certain condition to be met before moving forward in the test, but it provides more flexibility compared to explicit wait.
    - This wait can be created using the FluentWait class, and it allows the WebDriver to poll the web element repeatedly until the specified condition is met.
    - ```java
      WebDriver driver = new ChromeDriver();
      Wait<WebDriver> wait = new FluentWait<WebDriver>(driver)
         .withTimeout(Duration.ofSeconds(30))
         .pollingEvery(Duration.ofSeconds(5))
         .ignoring(NoSuchElementException.class);
      WebElement element = wait.until(ExpectedConditions.visibilityOfElementLocated(By.id("someId")));

## Java Slim (Cont)
---
### Java Collection
---
- Overview of Collection Hierarchy
    - A hierarchy of interfaces / classes that represent a group of objects as a single entity
    - It is used to provide different ways of storing and manipulating groups of elements
    - The root interface is `Collection`
    - Subinterfaces: `List`, `Set`, `Queue`, and `Dequeue`
    - `List` and `Set` are the most commonly used interfaces
- List Interface
    - List is an ordered collection of elements that allows duplicate entries
    - It extends the `Collection` interface and defines behavior for elements that are ordered, allowing positional access
    - Common implemtations: `ArrayList`, `LinkedList`
    - ```java
      List<String> list = new ArrayList<>();
      list.add("apple");
      list.add("banana");
      list.add("orange");
      System.out.println(list.get(1)); // Output: banana
- Set Interface
    - Set is a collection of elements with no duplicate entries
    - It extends the `Collection` interface, and does not allow positional access
    - Common implementations: `HashSet`, `TreeSet`
    - ```java
      Set<String> set = new HashSet<>();
      set.add("apple");
      set.add("banana");
      set.add("orange");
      System.out.println(set.size()); // Output: 3
- Map Interface
    - Map is a collection of key-value pairs where each key is unique
    - It provides a way of looking up a value based on its associated key
    - Common implementations: `HashMap`, `TreeMap`
    - ```java
      Map<String, Integer> map = new HashMap<>();
      map.put("apple", 1);
      map.put("banana", 2);
      map.put("orange", 3);
      System.out.println(map.get("banana")); // Output: 2
- Generics
    - Generics provide a way to specify the type of objects that a collection can hold at compile time
    - By specifying the type of objects, it allows for type safety, and prevents errors at runtime
    - It can be used with the Collection interfaces and classes
    - ```java
      List<String> list = new ArrayList<>();
      Map<String, Integer> map = new HashMap<>();
    - The generic go in between the angle brackets `<>`
### Exceptions
---
- **Reading a Stack Trace**
    - A stack trace is a report of the function call hierarchy that is currently in the execution stack
    - The stack is a representation of the order in which methods are being called
    - As a new method is called, it is added onto the stack, and when it resolves it is removed from the stack
    - When an exception is thrown, a stack trace is printed to help the programmer diagnose the problem
    - ```
      Exception in thread "main" java.lang.NullPointerException
          at com.example.myproject.Book.getTitle(Book.java:16)
          at com.example.myproject.Author.getBookTitles(Author.java:25)
          at com.example.myproject.CoAuthor.getBookTitles(CoAuthor.java:19)
          at com.example.myproject.Main.main(Main.java:10)
    - This stack trace indicates that a `NullPointerException` occurred on line 16 of the `Book` class
- **Errors vs Exceptions**
    - Errors and exceptions are both types of throwable object in Java
    - `Throwable` is an interface that is the inherited by both errors and exceptions
    - Errors are serious problems that cannot be handled by the application such as running out of memory
    - Exceptions are less severe problems that can be handled by the application
- **Handling Exceptions**
    - Exceptions can be handled in a try-catch block
    - When an exception is thrown, the catch block is executed, allowing the program to recover from the exception
    - There is also an addition `finally` block that can be included that will always run at the end of the try-catch block even if an exception occurs
    - ```java
      try {
          // code that might throw an exception
      } catch (ExceptionType e) {
          // code to handle the exception
      } finally {
          // code to run at the end of the try catch block
      }
- **Checked vs Unchecked Exceptions**
    - There are two types of excpetions: Checked and Unchecked
    - Checked exceptions are exceptions that must be caught or decalred in the method signature using the `throws` keyword
        - Examples: `IOException` and `SQLException`
    - Unchecked exceptions do not need to be caught or declared
        - Examples: `NullPointerException` and `ArrayIndexOutOfBoundsException`
    - If you do not handle a checked exception and decide to throw it instead
        - ```java
          public int getAge() throws Exception {
            // code that throws checked exception but not handled with try catch
          }
- **Creating Custom Exceptions**
    - Custom exceptions can be created by extending the `Exception` or `RuntimeException` class
    - Custom exceptions can be used to add more information to the exception message or to differentiate between different types of exceptions
    - ```java
      public class MyException extends Exception {
          public MyException(String message) {
              super(message);
          }
      }
- **Try-With-Resources**
    - The try-with-resources statement is a Java 7 feature that allows resources to be automatically closed after they are used
    - The try-with-resources statement uses a try-catch block to declare and initialize one or more resources and automatically closes the resources when the try block is exited
    - Resources that can be closed need to implement `Closeable` interface
    - An example of something that needs to be closed could be files or a database connection
    - ```java
      try (BufferedReader reader = new BufferedReader(new FileReader("file.txt"))) {
          String line = reader.readLine();
          while (line != null) {
              System.out.println(line);
              line = reader.readLine();
          }
      } catch (IOException e) {
          // handle the exception
      }
### JUnit
---
- **Intro to JUnit**
    - JUnit is a unit testing framework for the java programming language
    - It is widely used for writing and executing automated tests for Java
    - Some key features of JUnit
        - **Assertions**
            - Ways to verify the expected output of a test case
        - **Test fixtures**
            - JUnit provided annotations to define the setup and teardown methods that will be executed before and after each test method
        - **Test suits**
            - A way to group multiple test cases together and execute them as a suite
        - **Test runners**
            - Several test runners that can be used to exectue test cases and generate reports
- **Annotations & Assertions**
    - Annotations:
        - `@Test`: used to signal that the annotated method is a test method.
        - `@BeforeEach`: used to signal that the annotated method should be executed before each test method in the current test class.
        - `@AfterEach`: used to signal that the annotated method should be executed after each test method in the current test class.
        - `@BeforeAll`: used to signal that the annotated method should be executed before any test methods in the current test class.
        - `@AfterAll`: used to signal that the annotated method should be executed after all test methods in the current test class have been run.
    - Assertions:
        - `assertEquals(expected, actual)`: checks that the expected value is equal to the actual value.
        - `assertTrue(condition)`: checks that the given condition is true.
        - `assertFalse(condition)`: checks that the given condition is false.
        - `assertNull(object)`: checks that the given object is null.
        - `assertNotNull(object)`: checks that the given object is not null.
        - `assertSame(expected, actual)`: checks that the expected object and the actual object are the same.
        - `assertNotSame(expected, actual)`: checks that the expected object and the actual object are not the same.
    - ```java
      import org.junit.jupiter.api.Assertions;
      import org.junit.jupiter.api.Test;
      
      public class MathUtilsTest {
          
          @Test
          public void testAdd() {
              MathUtils mathUtils = new MathUtils();
              int result = mathUtils.add(2, 3);
              Assertions.assertEquals(5, result, "The result should be 5");
          }
          
          @Test
          public void testDivide() {
              MathUtils mathUtils = new MathUtils();
              Assertions.assertThrows(ArithmeticException.class, () -> mathUtils.divide(1, 0), "Divide by zero should throw ArithmeticException");
          }
          
          @Test
          public void testMultiply() {
              MathUtils mathUtils = new MathUtils();
              int result = mathUtils.multiply(2, 3);
              Assertions.assertEquals(6, result, "The result should be 6");
          }
      }
- **Intro to TDD**
    - Test-driven Development (TDD) is a software development process that emphasizes the creation of automated tests before actually writing code
    - You create small units of functionality and test them continuously in an iterative process throughout development
    - The TDD process typically involves these steps:
        1. **Write a failing test**
            - Start by writing a test that specifies the desired behavior of the code
            - The test should fail initially as no code has been written yet to implement the functionality
        2. **Write the code**
            - Write the minimum amount of code necessary to pass the test
            - This ensures that the code is testable and that the test is effective
        3. **Run the tests**
            - Run all of the tests to ensure that the new code does not break any existing functionality
        4. **Refactor the code**
            - Once the new code passes all of the tests, it can be refactored to improve its quality and readability
        5. **Repeat**
            - Repeat the process for each new feature or functionality that needs to be added to the codebase
    - Benefits of TDD:
        - **Improved code quality**
            - It encourages developers to write clean, modular, and testable code
        - **Faster development**
            - It helps catch bugs earlier in the development process, which leads to faster feedback and faster development cycles
        - **Improved documentation**
            - Tests serve as documentation for the codebase, making it easier for new developers to understand how the code works
        - **Increased confidence**
            - By writing tests that cover all aspects of the codebase, developers can be more confident in the quality of their code
    - An example of TDD:
        1. **Write a failing test**
            - ```java
              @test
              public void testSum() {
                Calculator calculator = new Calculator();
                int sum = calculator.sum(2, 3);
                assertEquals(5, sum);
              }
        2. **Write the code**
            - ```java
              public class Calculator {
                public int sum(int a, int b){
                    return a + b;
                }
              }
        3. **Run the tests**
            - ```
              Tests run: 1, Failures: 0, Errors: 0, Skipped: 0
        4. **Refactor the code** (none needed in this example)
        5. **Repeat** for any additional functionality that needs to be added
              