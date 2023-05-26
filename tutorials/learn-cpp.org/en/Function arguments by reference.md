Tutorial
--------

In C++, let's say that you want to add 1 to a varible through the use of a function for exmaple addone, however if you try the following code which would seem to work at your current level of knowledge, it wouldn't work, let's find out why?
    
    #include <iostream>
    
    void addone(int x) {
        x++;
    }
    
    int main() {
        int n = 2;
        addone(n);
        std::cout << n;
        return 0;
    }

The previous code would print 2 (the orginal value of n) but not 3, To fix this we could assign the function a ptr(pointer) that it can manipulate to also change the value of n: We can do so like such:

    #include <iostream>
    void addone(int& x) {
        x++;
    }
    
    int main()
    {
        int n = 2;
        addone(n);
        std::cout << n;
        return 0;
    }

Exercise
--------

Write a function called `birthday`, which adds one to the `age` of a `person`.

Tutorial Code
-------------

    #include <iostream>

    class Person
    {
    public:
    std::string name;
    int age;
    Person(std::string name, int age) : name(name), age(age)
    {

    }
    };

    //Your Code Goes Here

    int main()
    {
    Person Lucas("Lucas", 25);
    std::cout << "Lucas is : " << Lucas.age << " Years Old!\n";
    Birthday(Lucas.age);
    std::cout << "Lucas is : " << Lucas.age << " years old!!";
    return 0;
    }


Expected Output
---------------

    Lucas is : 25 Years Old!
    Lucas is : 26 years old!!

Solution
--------
    #include <iostream>

    class Person
    {
    public:
    std::string name;
    int age;
    Person(std::string name, int age) : name(name), age(age)
    {

    }
    };

    void Birthday(int& age)
    {
    age++;
    }

    int main()
    {
    Person Lucas("Lucas", 25);
    std::cout << "Lucas is : " << Lucas.age << " Years Old!\n";
    Birthday(Lucas.age);
    std::cout << "Lucas is : " << Lucas.age << " years old!!";
    return 0;
    }

      return 0;
    }
