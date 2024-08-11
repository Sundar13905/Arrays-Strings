# ARRAYS AND STRINGS IN C++

# EXPERIMENT 7 ARRAYS

## AIM
To study and implement C++ Arrays 

## THEORY

In computer science, an array is a data structure consisting of a collection of elements (values or variables), of same memory size, each identified by at least one array index or key.
Arrays have continous memory allocation
In C++ language, the array has a fixed size meaning once the size is given to it, it cannot be changed i.e. you can’t shrink it nor can you expand it. The reason was that for expanding if we change the size we can’t be sure ) that we get the next memory location to us for free. The shrinking will not work because the array, when declared, gets memory statically allocated, and thus compiler is the only one that can destroy it. 
For example: -
If an array is of the integer datatype, then: -
1. The array will contain only integer datatype values and variables
2. If the first element memory address is allocated at 1000 then the 2nd element will have the memory address as 1004
3. The array indexing will start at 0, so if u want ot access the first element of lets say array arr, it will have to be called at either the value of arr[0] or via reference(address of the first element)

### Applications of Array Data Structure: -
1. To represent data in matrix form, a vector or a tabular form
2. To store data for processing
3. Implementing data structures such as queues and stacks as well dynamic memeory allocation like linked lists and trees


### Array Operations: -
1. __Traversal__ : Visiting each element of an array in a specific order (e.g., sequential, reverse).
2. __Insertion__ : Adding a new element to an array at a specific index.
3. __Deletion__ : Removing an element from an array at a specific index.
4. __Searching__ : Finding the index of an element in an array.

### Types of arrays: -
1. One dimensional arrays
2. Multi dimensional arrays


### Advaantages of arrays
1. Arrays allow random access to elements. This makes accessing elements by position faster.
2. Arrays have better cache locality which makes a pretty big difference in performance.
3. Arrays represent multiple data items of the same type using a single name.
4. Arrays are used to implement the other data structures like linked lists, stacks, queues, trees, graphs, etc.

### Disadvantages of arrays
1. As arrays have a fixed size, once the memory is allocated to them, it cannot be increased or decreased, making it impossible to store extra data if required. An array of fixed size is referred to as a static array. 
Allocating less memory than required to an array leads to loss of data.
2. An array is homogeneous in nature so, a single array cannot store values of different data types. 
3. Arrays store data in contiguous memory locations, which makes deletion and insertion very difficult to implement. This problem is overcome by implementing linked lists, which allow elements to be accessed sequentially.  


### Initialization of arrays 
#### 1. Fixed Size, fixed Value arrays
~~~
int arr[5]; 
// Another way (creation and initialization both)
int arr2[5] = {1, 2, 3, 4, 5};
~~~

#### 2. Dynamical memory allocation, but fixed size
~~~
int *arr = new int[5];
~~~

#### 3. Dynamic size
-This is one of the differences between C and C++
~~~
vector<int> v;
~~~


## CODE

~~~
#include <iostream>
using namespace std;

int main()
{
    int a[100] = {78, 890, 67, 34, 13};
    int b[5] = {56, 78, 12, 90, 97};
    int c[100] = {19, 10, 100, 45, 47};

    cout << "Traditional method" << endl;
    for(int i = 0; i < 5; i++)
    {
        cout << a[i] << endl;
    }
    cout << endl;

    //modern method printing 
    cout<<"Modern method of printing of an array"<<endl;
    for(int j: b)
    {
        cout<<j<<" ";
    }
    cout<<endl;

    cout<<"--------------------------------"<<endl;
    // user defined array
    cout<<"user defined array"<<endl;
    int array[100],n;
    cout<<"Enter the size of array"<<endl;
    cin>>n;
    cout<<"Enter the array elements"<<endl;
    for(int i = 0;i<n;i++)
    {
        cin>>array[i];
    }

    cout<<"The array is as follows: "<<endl;
    for(int i =0;i<n;i++)
    {
        cout<<array[i]<<" ";
    }
    cout<<endl;

    cout<<"-----------------------------------"<<endl;

    // reversing an array
    cout<<"Reversing an array"<<endl;
    for(int j = n-1;j>= 0;j--)
    {
        cout<<array[j]<<endl;
    }
    cout<<endl;

    //finding marks 
    cout<<"-----------------------------------"<<endl;
    cout<<"Finding an element in a array"<< endl;
    int mark,marks[100],flag = 0,count = 0;
    cout<<"Enter 5 elements "<<endl;
    for(int i =0;i<5;i++)
    {
        cin>>marks[i];
    }
    cout<<"Which element position do u want"<<endl;
    cin>>mark;

    for(int i =0;i<5;i++)
    {
        if(mark == marks[i])
        {
            cout<<"position of the element is at: "<<i<<endl;
            count++;
            flag = 1;
        }
    }

    if(count == 0)
    {
        cout<<"No elements found"<<endl;
    }
    else if(flag == 1)
    {
        cout<<"Element is present at: "<< count << "times" << endl;
    }

    cout<<"-----------------------------------"<<endl;
    // sum of an array
    cout<<"The sum of array elements "<<endl;
    int sum = 0;
    for(int i = 0;i<5;i++)
    {
        sum = sum+marks[i];
    }
    cout<<"Sum of elements: "<<sum<< endl;

    //average of an array 

    float avg;
    avg = sum/5;

    cout<<"The average of the array is: "<<avg<<endl;

    cout<<"-----------------------------------------"<<endl;

    // minimum of an array

    int min=marks[0],max=marks[0];

    for(int i =0;i<5;i++)
    {
        if(min<marks[i])
        {
            min = marks[i];
        }
    }
    cout<<"\nThe least value of the array is: "<<min<<endl;

    for(int i =0;i<n;i++)
    {
        if(max>marks[i])
        {
            max = marks[i];
        }
    }
    cout<<"\nThe highest value of the array is: "<<max<<endl;

    cout<<"-----------------------------"<<endl;
    
    return 0;
}
~~~

## CODE OUTPUT
![Array_code_output](https://github.com/Sundar13905/Arrays-Strings/blob/main/Arrays_Output.png)

## CONCLUSION

We learnt how to implement arrays and its operations in C++ programming languages


----------------------------------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------------------------------


# EXPERIMENT 7 STRINGS 

## AIM

To study and implement C++ strings

## THEORY

A string is a datatype having a sequence of characters used to represent text. Strings are commonly used for storing and manipulating textual data in computer programs. They can be manipulated using various operations like concatenation, substring extraction, and comparison.

In most programming languages, strings are treated as a distinct data type. This means that strings have their own set of operations and properties. They can be declared and manipulated using specific string-related functions and methods.

### Application of strings

1. Hashing and encryption of data: - Random strings are generated to secure data or encrypt data
2. Data representation
3. Database operation
4. Web developmenent

### Operations of strings: -
1. Find the length of a string 
2. Accessing Characters	from a string using its indexing value
3. Concating or merging of 2 strings 
4. Appending and Concatenating Strings	
5. comparing 2 strings
6. Making substrings	
6. Searching a character from a string  
7. replacing a character or substring from the orignal string 
8. inserting a character into a string
9. deleting or erasing a character from a string 
10. Coversion to obtain a C_type string (character array)


The above operations can be directly accessed in C++ programming language that has been stored in String header file for example __length()__ to find the length of a string, __at()__, __append()__ , __compare()__ , __substring()__ , find(), etc.

## CODE
~~~
#include<iostream>
#include<string>

using namespace std;

int main()
{
    string a;
    cout<<"Enter any string"<<endl;
    cin>> a;
    cout<<"The entered string is: "<<a<<endl;

    cout<<"-----------------"<<endl;

    cout<<"Concatenation of 2 strings: "<<endl;
    cout<<"\nEnter 2 strings to concatenate: "<<endl;
    string str1,str2,str3,str4;
    cin>> str1>> str2;
    cout<<"\nConcatenation of the 2 strings: "<<str1+str2<<endl;

    cout<<"-------------------"<<endl;
    cout<<"\nReversing a string"<<endl;
    cout<<"\nEnter a string to reverse"<<endl;
    cin>> str3;
    for(int i = str3.length()-1;i>=0;i--)
    {
        cout<<str3[i];
    }

    cout<<"\n-------------------------"<<endl;
    cout<<"\nTo check whether the given string is a Palindrome"<<endl;
    cout<<"Enter a string to check whether a given string is a Palindrome"<<endl;
    cin>>str4;
    int len = str4.length();
    bool flag = true;
    for (int i = 0; i < len / 2; i++)
    {
        if (str4[i] != str4[len - 1 - i])
        {
            flag = false;
            break;
        }
    }

    if(flag)
    {
        cout<<"The given string is  a palindrome"<<endl;
    }
    else 
    {
        cout<<"The given string is not a palindrome"<<endl;
    }


    return 0;
}
~~~

## CODE OUTPUR 
![String_output](https://github.com/Sundar13905/Arrays-Strings/blob/main/String_output.png)






