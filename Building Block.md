
Java fundamentals, variables, data types, and garbage collection

---
### 1. About the Environment
#### JDK
(Java Development Kit)**: Contains compiler and tools for Java development
#### JVM
(Java Virtual Machine)**: Runs compiled Java programs
#### Compilation Process:
`javac ClassName.java` → `java ClassName`
#### Single-File Source Code
Can run directly with `java ClassName.java` (no separate compilation needed)
### 2. Understanding the Class Structure
#### Basic Class Structure

```java
public class Animal {
    String name; // Field/Variable 
    public String getName() { // Method return name; 
    }
}
```

#### Members
- Fields (variables)
- Methods
#### Keywords
Special words with reserved meanings (`public`, `class`, etc.)
### main() Method
Standard signature: `public static void main(String[] args)`
Command line arguments: `arg[0]`, `arg[1]`. Array indexing from 0
#### Example
```java
public class Zoo {
  public static void main(String[] args) {
    System.out.println(args[0]); // First argument 
    System.out.println(args[1]); // Second argument 
    }
}
```

When I run `java Zoo.java`, the arguments will be empty
When I run `java Zoo.java first second`. The output of the `Zoo` program will be:
```console
first
second
```

### Package Declarations and Imports

#### What are Packages?
* Logical groupings for classes, similar to folders in a file cabinet
* Purpose: Organize thousands of Java classes to avoid naming conflicts
* Analogy: Like mailing addresses - package name is the building address, class name is the apartment number
#### Package Naming Conventions
* Hierarchical structure: `com.company.project.modul`
* 
