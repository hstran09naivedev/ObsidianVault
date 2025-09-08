**Autoboxing** is the **automatic conversion** of primitive types to their corresponding wrapper classes, while **Unboxing** is the reverse process.
```java
// Manual conversion (old way)
int primitive = 5;
Integer wrapper = Integer.valueOf(primitive);  // Manual boxing
int backToPrimitive = wrapper.intValue();      // Manual unboxing

// Automatic conversion (autoboxing/unboxing)
Integer autoBoxed = 5;        // Autoboxing: int → Integer
int autoUnboxed = autoBoxed;  // Unboxing: Integer → int
```

Example:

| Primitive | Wrapper Class | Autoboxing Example   |
| --------- | ------------- | -------------------- |
| `boolean` | `Boolean`     | `Boolean b = true;`  |
| `byte`    | `Byte`        | `Byte b = 1;`        |
| `short`   | `Short`       | `Short s = 2;`       |
| `char`    | `Character`   | `Character c = 'A';` |
| `int`     | `Integer`     | `Integer i = 3;`     |
| `long`    | `Long`        | `Long l = 4L;`       |
| `float`   | `Float`       | `Float f = 5.0f;`    |
| `double`  | `Double`      | `Double d = 6.0;`    |
Detail examples

```java
// Autoboxing examples
Integer i = 100;          // int → Integer
Double d = 3.14;          // double → Double
Boolean b = true;         // boolean → Boolean
Character c = 'X';        // char → Character

// Unboxing examples
int primitiveInt = i;     // Integer → int
double primitiveDouble = d; // Double → double
boolean primitiveBool = b;  // Boolean → boolean
char primitiveChar = c;     // Character → char
```
