# c++primer-learning 
A greenhand's ideas and resources when learning c++ primer<br>

**CHAPTER 1**<br>
>In 1.5.1 you should download  "Sales_item.h" at the same flie of your cpp files.<br>

>when using a header within stardard library,you should use "" instead of <><br>

>#include <bits/stdc++.h> &emsp; #include "Sales_item.h"<br>

>***Here give a code of 1.6***

```
#include <iostream>

#include "Sales_item.h"

int main()
{
    Sales_item total;
    if (std::cin>> total)
    {
        Sales_item trans;
        while(std::cin>>total)
        {
            if(total.isbn()==trans.isbn())
            {
                total+=trans;
            }
            else{
                std::cout<<total<<std::endl;
                total=trans;// renew the value of total--The next book.
            }
            std::cout<<total<<std::endl;//the last book 
   
        }
       
    }
    else 
     {
        std::cerr<<"NO DATA"<<std::endl;
        return -1;
            }
    return 0;
}
```
**CHAPTER 2**<br>
>In 2.2.2 you can learn the difference of declaration and definition.

```
extern int a;//declaration
int b;//definition
```

>declaration does not save the varibility in the memory,while definition will save the varibility in the memory.<br>
>so ,according to this spectifty,we could use a pointer to trace it and see what will happen.I think it is interesting.<br>
***Here is the code***<br>
```
#include <iostream>    
int main()    
{    
    
   extern int b ;    
   int *local= &b;    
   std::cout<<local<<std::endl;    
   return 0;    
}    
```
