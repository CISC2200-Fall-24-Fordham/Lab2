# CISC2200 Spring 2024 Lab2

In this lab assignment, we practice **working with linked list**, **working with class template**,
and **understanding testcases**.

## Download starter code

From your terminal (mac or WSL/Ubunto) window, you can use the following command to download it:
```
git clone https://github.com/CISC2200-Spring2024/lab2.git
```

## Programming Environment Setup
If you haven't done so already, please set up programming environment our our own computer, by following [Setup Tutorial](https://eecs280staff.github.io/tutorials/). 

- The _Commannd Line Tools_ are required. 

- The _C++ Dev Environment_ (VSCode) is highly recommened.

**Please follow these tutorials closely and carefully.**

## Requirements

The class template **SLList** as studied in the class is defined in the **SLList.h** provided.

Please implement the following member functions, **iteratively (i.e., without using recursion)** in the **SLList.h**. The pseudocode for these 
linked list manipulation will be discussed in class. 

0. (Optional but helpful for debugging) Add a member function **display()** to display to the terminal the items stored in the list.
1. Implement the copy constructor, note that you need to perform deep-copy 
2. Implement  **geti()** member function 
3. Implement **removeFirst()** member function
4. Implement **removeLast()**  member function
5. Implement **insertAt()** member function

## Hints

The **main.cpp** provided in this repository tests the above member functions and checks to see if the returned value or the list is changed as 
expected by the function. For example, the following code snippet first create a list **K** passing an existing list **L** as parameter, which leads to the copy constructor being called.
It subsequently checks if the two lists have same size or not, and whether the list **K**'s first element and last element have values as expected. 

```
 //test copy constructor
  ds::SLList<int> *K = new ds::SLList<int>(L);

  if (L.size() != K->size() ||
     K->get(0) != nums[0] ||
     K->get(SIZE - 1) != nums[SIZE - 1])
  {
      cout <<"failed copy constructor test\n";
  }
  else
          cout <<"passed copy constructor test\n";
```

You can modify the file **main.cpp** anyway you wish 
in order to test your member functions. You should take an incremental approach: 

1. Implement the **display()** method to help examining the content of the list
2. Build a list using **addFirst**, **addLast** methods that are provided (and therefore bug free). Display the resulting list. 
3. Implement the required member functions one at time, test and debug it on the list you built, before moving on to work on the next function.


## Submission 

Submit your **SLList.h** file at the following link by Feb 13, 2024, midnight (11:59pm). The autograder compiles and tests your programs using 
some testcases that are different from those in **main.cpp**. If your program fails some testcases, go back to review your code, and test your member functions
with different inputs.

[lab2 submission link
](https://storm.cis.fordham.edu:8443/web/project/1485)
