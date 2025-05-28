# c++primer-learning 
A greenhand's ideas and resources when learning c++ primer<br>

**CHAPTER 1**<br>
>In 1.5.1 you should download  "Sales_item.h" at the same flie of your cpp files.<br>

>when using a header within stardard library,you should use "" instead of <><br>

>#include <iostream>   #include <bits/stdc++.h>   #include "Sales_item.h"<br>

>***Here give a code of 1.6***

>#include <iostream>
>#include "Sales_item.h"    
>int main()    
>{    
>    Sales_item total;    
>    if (std::cin>> total)    
>    {    
>        Sales_item trans;    
>        while(std::cin>>total)    
>        {    
>            if(total.isbn()==trans.isbn())    
>            {    
>               total+=trans;    
>           }     
>            else
>            {     
>                std::cout<<total<<std::endl;     
>                total=trans;// renew the value of total--The next book.     
>            }       
>            std::cout<<total<<std::endl;//the last book     
>   
>       }      
>        
>    }     
>    else      
>     {      
>        std::cerr<<"NO DATA"<<std::endl;     
>        return -1;     
>     }      
>    return 0;    
>}    
