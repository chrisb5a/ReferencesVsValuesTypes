# ReferenceVsValueTypes 


    -What each is (reference and value type)
    
    A value type is one of two categories of variable that exist in swift. Value types hold their values within their own memory. For example:
       int i = 100 means that i contains the value 100 (stored on the stack)
       Value type examples are:
       bool, byte, char, decimal, double, enum, float, int, long, sbyte, short,struct, uint, ulong, ushort    
    
    A reference is the other category of swift variable.
        A reference type holds a single copy of its data.Reference types hold reference address to the object but not the object itself. Reference types can be classes, Objects, Arrays, Indexers, Interfaces etc. reference types points to the location of the of the stored data which value exists on the heap. For example:  
        
        class C { var data: Int = -1 } 
        means that c() holds and points to the address of the its data (which is -1)  but C is not 'directly' equal to -1
        
        
     
    
    -how are they different 
    
    The difference between reference types and value type as the previous answer shows resides mainly in the storage and access to the data. This leads further to the following differences. Let us say I define int i = 1 and int j = 1000. When I make j = i and print(i,j), the output is 1 1. Here I have made the value j equal to the value i which is 1 and i remained with the value 1.
    
    Now if I have class I{ var data= int 1  }. In the class A, we have data that point to a value that is 1, we call it addr1 (points to 1). Note that it is easy to get confused as we do not explicitely (or did not declare) write the in between steps of creating an adress for data and making it point to its value, -1. 
    J = I() makes J essentially the class I. J has the same attribute has I() and same address allocation process. If one writes and excutes J.data = 1000, now addr1 points to 1000. The address has been changed. If we write execute print(I.data, J.data), the output is 1000 1000. We have written in addr1 a reference to the value 1000.
    
    
    
    
    -how they are utilized in iOS, Swift, and ObjC
    
    As a rule of thumbs reference types are used to model entities with their identity. For example a company could well be represented by a class with its employees names, id numbers, hiring date etc.
    While value type are preferrably used to encapsulate rules and logic. for example, how can one change the id number of an employee.
    
    
    
    -pros and cons to either 
    
        reference type:
        - pros:
        for large data
        object manipulation using reference rather than objects (davantageous for large objects )
        Faster execution for large object
        Save memory with large object
        
        
        - cons: 
        mutability = hard to modify variables
        
        
        value types:
        
        -pros: 
        for small data
        rapid execution (garbage collector of deleted values of reference need to be tracked, no reference and allocation)
        less memory usage for values type that are relatively short
        mutability 
        
        -cons
        No inheritance 
        
        

    
        
        


