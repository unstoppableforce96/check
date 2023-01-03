[Table of Contents]
- [Route Map for C Programming Language](#route-map-for-c-programming-language)
  - [Concepts to learn in order to start programming in C](#concepts-to-learn-in-order-to-start-programming-in-c)
    - [Data types and Variables](#data-types-and-variables)
    - [Operators](#operators)
    - [I/O Operations](#io-operations)
    - [math.h header file](#mathh-header-file)
      - [sqrt()](#sqrt)
      - [pow()](#pow)
    - [Practice 1](#practice-1)
        - [Problem 1](#problem-1)
        - [Problem 2](#problem-2)


# Route Map for C Programming Language
## Concepts to learn in order to start programming in C
- Data types and Variables
- Operators
- I/O Operations
- math.h header file
- Conditional Statements
- Loops
- User Defined Functions
- Arrays
- Strings
- Structures

### Data types and Variables

<details>
  <summary> Read and Learn about data types and variables from here </summary>
  
  [CodeminD](http://bit.ly/3CgD096)
  [Other](https://www.geeksforgeeks.org/data-types-in-c)
  [Other](https://www.geeksforgeeks.org/variables-in-c)

  
</details>

### Operators

<details>
  <summary> Read and Learn about Operators </summary>
  
  [CodeminD](http://bit.ly/3CgD096)
  [Other](https://www.geeksforgeeks.org/operators-in-c/)

  
</details>


### I/O Operations

<details>
  <summary> Learn about I/O operations in C from here </summary>
  
  [Click me](https://www.geeksforgeeks.org/operators-in-c/)

  
</details>


### math.h header file
math.h is a header file in C, in which some standard mathematical built_in functions are present. In order to use those functions in out program we must include it in our program.

Some important functions that are present in math.h are
- sqrt()
- pow()
- ceil()
- floor()
- abs()

Let's see one by one with some examples

#### sqrt()
This function takes a value and returns it's sqaure root (in double data type).
<details>
  <summary> Examples </summary>

**Example 1**
```c
#include <stdio.h>
#include <math.h>
int main() {
    int n = 144;
    int s = sqrt(n);
    printf("Square root of %d is %d", n, s);
}
```
The above exmaple will print 
***Square root of 144 is 12*** as output.

**Example 2**
```c
#include <stdio.h>
#include <math.h>
int main() {
    int n = 30;
    printf("%.2f", sqrt(n));
}
```
The above exmaple will print 
***5.48*** as output as it's the square root of 30, and we also adjusted the result to 2 decimal places after point.

</details>

#### pow()
This function takes 2 values a and b and returns a power b (a to the power of b). Returns a double data as result type.

<details>
  <summary> Examples </summary>
**Example 1**
```c
#include <stdio.h>
#include <math.h>
int main() {
    int a = 3;
    int b = 4;
    int p = pow(a, b);
    printf("%d power %d is %d", a, b, p);
}
```
The above exmaple will print 
***3 power 4 is 81*** as output.

**Example 2**
```c
#include <stdio.h>
#include <math.h>
int main() {
    int a = 16;
    float b = 0.5;
    printf("%.2f", pow(a, b));
}
```
The above exmaple will print 
***4.00*** as output as it's the square root of 16 (Notice that power 0.5 is nothing but square root), and we also adjusted the result to 2 decimal places after point.

</details>

<br>

<details>
  <summary> More about math.h from here </summary>
  
  [Click me](https://www.geeksforgeeks.org/operators-in-c/)

  
</details>


### Practice 1

Now that you've learned something about variables, datatypes, operators and I/O statements, it's time to put them to a test.

Let's explore some simple problems with examples and then you can practice on your own.

Here're some simple problems with solutions and explanations.

##### Problem 1
Find out the ***Area*** and ***Perimeter*** of a Square when ***side*** value is given.

<details>
  <summary> <b> Solution </b> </summary>
  
  ```c
  #include <stdio.h>
  int main() {
        // Variable declaration part
        int side, area, peri;

        // Reading side value from user using scanf()
        scanf("%d", &side);

        // calculating area and perimeter
        area = side * side;
        peri = 4 * side;

        // printing the result
        printf("Area is: %d\n", area);
        printf("Perimeter is: %d", peri);
  }
  ```

 **Explanation:**  
 - Here we've taken 3 variables 1 for input (side) 2 for outputs (area and peri).
 - Then we read the *side* value from the user using scanf(). Notice that this is the best practice to read the input from user so that we can work on them and produce the output accordingly.
 - After that, we just calculated the area and perimeter using appropriate formulas
 - And finally we printed the results to the output screen using printf() statement.

</details>

<br>

##### Problem 2
You're given two points ***(x1, y1)*** and ***(x2, y2)*** find out the distance between those points.

<details>
  <summary> <b> Solution </b> </summary>
  
  ```c
  #include <stdio.h>
  #include <math.h>
  int main() {
        // Variable declaration part
        int x1, y1, x2, y2;
        float distance;

        // Reading x1, y1, x2 and y2 values from user using scanf()
        scanf("%d%d%d%d", &x1, &y1, &x2, &y2);

        // calculating distance
        distance = sqrt(pow((x2 - x1), 2) + pow((y2 - y1), 2));

        // printing the result
        printf("%.2f", distance);
  }
  ```

 **Explanation:**  
 - Here we've taken 4 integer variables *x1, y1, x2, y2* and 1 floating point variable *distance*.
 - Then we read *x1, y1 and x2, y2* values from user using scanf()
 - The reason we took *distance* variable as of type float is we get the distance between 2 points in floating point values almost all times as the calculation includes a square root operation.
 - And as calculation part we applied the following formula $\sqrt{(x2 - x1)^2 + (y2 - y1)^2}$
 - To do this we took the help of **pow()** function to perform square operation on *(x2 - x1)* and on *(y2 - y1)* and the help of **sqrt()** function from ***math.h*** header file  to perform square root on the result.
 - And finally we printed the result (adjusted to 2 decimal places after point) to the output screen using printf() statement.

</details>