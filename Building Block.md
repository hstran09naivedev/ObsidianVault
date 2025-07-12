
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
### 3. main() Method
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

### 4. Package Declarations and Imports

#### What are Packages?
* Logical groupings for classes, similar to folders in a file cabinet
* Purpose: Organize thousands of Java classes to avoid naming conflicts
* Analogy: Like mailing addresses - package name is the building address, class name is the apartment number
#### Package Naming Conventions
* Hierarchical structure: `com.company.project.module`
* Reverse domain naming: `com.wiley.javabook` (from wiley.com)
* **JDK packages**: Start with `java` (e.g., `java.util`, `java.lang`)
* **Child packages**: More specific packages (e.g., `java.util.concurrent.atomic`)
* **Rules**: Mostly letters/numbers separated by periods
Example
```java
package com.wiley.javabook;         // Valid
package a.b.c;                      // Valid (exam style)
package java.util;                  // JDK package
package java.util.concurrent;       // Child package
```
#### Import Statements
**Purpose**: Tell compiler which package to look in for classes
**Without import**: Compiler error "cannot find symbol"
Example
```java
// Without import - DOES NOT COMPILE
public class NumberPicker {
    public static void main(String[] args) {
        Random r = new Random();  // Error: cannot find symbol
    }
}

// With import - Compiles successfully
import java.util.Random;
public class NumberPicker {
    public static void main(String[] args) {
        Random r = new Random();  // Works!
        System.out.println(r.nextInt(10));
    }
}
```
#### Wildcard Imports
**Syntax**: `import java.util.*;`
**Purpose**: Import all classes in a package
**Limitation**: Does NOT import child packages
**Performance**: No runtime impact - compiler optimizes
##### [[Why avoid Wildcard Imports]]
#### java.lang Package - Automatic Import
- **Special package**: `java.lang` is automatically imported
- **Common classes**: `String`, `System`, `Object`, `Integer`, etc.
- **No explicit import needed**: Can use directly
```java
// These imports are REDUNDANT
import java.lang.System;   // Redundant
import java.lang.*;        // Redundant  
import java.util.Random;   // Needed
import java.util.*;        // Redundant if Random is specifically imported

public class NumberPicker {
    public static void main(String[] args) {
        Random r = new Random();
        System.out.println(r.nextInt(10)); // System available without import
    }
}
```
#### Naming Conflicts and Resolution
- **Problem**: Multiple packages contain classes with same name
- **Example**: `java.util.Date` vs `java.sql.Date`
- **Resolution Rules**:
    1. Explicit class import beats wildcard
    2. Multiple wildcards with same class name = compiler error
    3. Multiple explicit imports of same class = compiler error
```java
// CONFLICT - Compiler error
import java.util.*;
import java.sql.*;     // Both have Date class - ambiguous!

// RESOLUTION 1 - Explicit import wins
import java.util.Date; // Explicit import takes precedence
import java.sql.*;     // Wildcard import

// RESOLUTION 2 - Use fully qualified name
import java.util.*;
import java.sql.*;
public class DateExample {
    java.util.Date utilDate;     // Fully qualified
    java.sql.Date sqlDate;       // Fully qualified
}

// ERROR - Multiple explicit imports
import java.util.Date;
import java.sql.Date;    // Compiler error - ambiguous 
```
### 5. Understanding Data Types
**Primitive Types**: Basic building blocks (`int`, `boolean`, `double`, etc.)
**Reference Types**: Objects that can have methods and be assigned `null`
**Wrapper Classes**: Reference type equivalents of primitives (`Integer`, `Boolean`, etc.)

| Type    | Size    | Range                           |
| ------- | ------- | ------------------------------- |
| boolean | -       | true/false                      |
| byte    | 8 bits  | -128 to 127                     |
| short   | 16 bits | -32,768 to 32,767               |
| int     | 32 bits | -2,147,483,648 to 2,147,483,647 |
| long    | 64 bits | Large range                     |
| float   | 32 bits | Decimal numbers                 |
| double  | 64 bits | Larger decimal numbers          |
| char    | 16 bits | Single character                |

[[Why is there no static size for boolean primitive type]]?
