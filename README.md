# Experiment 13 To study and implement Constructor Overloading

## Aim
To write a code using constructor overloading

## Software: VS code

## Theory
### Characteristics of constructor overloading: 
Sure, here is the definition of **Constructor Overloading** broken down into points:

1. **Multiple Constructors:** Constructor overloading allows a class to have more than one constructor, each with a different set of parameters.

2. **Different Parameter Lists:** The constructors must have different parameter lists, which can vary by the number, type, or order of parameters.

3. **Automatic Selection:** When an object is instantiated, the compiler automatically selects the appropriate constructor based on the arguments provided.

4. **Flexible Initialization:** Overloaded constructors allow for different ways to initialize an object, depending on the data available at the time of creation.

5. **Same Name:** All overloaded constructors must share the same name as the class, just like any other constructor.

6. **No Return Type:** Like all constructors, overloaded constructors do not have a return type. 

7. **Enhanced Versatility:** Constructor overloading makes the class more versatile, allowing for more flexible object creation.

### Advantages of Constructor Overloading in C++:
1. Flexibility: Allows the class to be instantiated in multiple ways, depending on the available data.

2. Ease of Use: Users can initialize objects with different sets of data conveniently.

3. Improved Readability: Makes the code more readable by clearly defining how objects can be created.


### Rules for Constructor Overloading in C++:

1. Different Signatures: Each overloaded constructor must have a different signature (i.e., a different set of parameters).

2. No Return Type: Like all constructors, overloaded constructors do not have a return type, not even void.

3. Same Name: All constructors must have the same name as the class name.

### How Constructor Overloading Works in C++:

1. When an object is created, the C++ compiler checks the arguments provided and chooses the constructor that matches the argument list.

2. If no arguments are passed, the default constructor is called.

3. If arguments are passed, the constructor with the matching parameters is called.

## Code 
~~~

// Varun Pendem
// PRN: 2307012319

#include <iostream>
using namespace std;

class Box {
private:
    double width, height, depth;

public:
    // Default constructor
    Box() {
        width = height = depth = 0;

    }

    // Constructor with one parameter
    Box(double side) {
        width = height = depth = side;
        
    }

    // Constructor with three parameters
    Box(double w, double h, double d) {
        width = w;
        height = h;
        depth = d;
        
    }

    void showVolume() {
        cout << "Volume: " << (width * height * depth) << endl;
    }
};

int main() {
    Box box1; // Calls the default constructor
    cout<<"Enter the side of the box: "<<endl;
    int side;
    cin>>side;
    Box box2(side); // Calls the constructor with one parameter
    int wd,ht,dep;
    cout<<"Enter the 3 sides of the box: "<<endl;
    cin>>wd>>ht>>dep;
    Box box3(wd,ht,dep); // Calls the constructor with three parameters

    cout << "Default constructor called!" << endl;
    box1.showVolume();
    cout << "Constructor with one parameter called!" << endl;
    box2.showVolume();
    cout << "Constructor with three parameters called!" << endl;
    box3.showVolume();

    return 0;
}

~~~

## Code Ouput: -
![image](https://github.com/user-attachments/assets/69e6d220-ca48-40b0-b8db-fbd16de1059a)



## Conclusion: -
1. Learnt how to implement constructors in the program.
2. Leant how classes and objects function.
3. Learnt about constructor overlaoding, its advantages, characteristics and rules.
