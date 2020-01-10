## Collection Framework

### Purpose: 
     >   To represent many values by using single object. 
     
**Problem**: To represent 10k values we declare 10k variables. By doing this the readability of the program is going to be down and this is worst kind of programming. To overcome this, we can go for arrays and collections.

**Arrays**: `Student[] s = new Student[10000];`

We can represent huge no of homogeneous type of elements by using single object(variable) with arrays.

#### Problems with Arrays:
1. Fixed in Size: Once we create an array with some size there is no chance of increasing or decreasing the size of that array based on our requirement.
2. Hold Homogeneous Elements: Arrays can hold only homogeneous type of elements.
   Ex: `s[0] = new Student();--(valid) s[1] = new Customer();` --(CE: incompatible types found: Customer required: Student) Here the          problem is that s[1] is expecting Student object but we are providing Customer object. 
   Note: We can solve this problem by using object type arrays. `Object[] a = new Object(10000); a[0] = new Student();`-(valid) `a[1] = new Customer();`--(valid) 
3. _No Readymade Method Support_: Arrays are not implemented based on some standard data structure. So, it is developer’s responsibility to write the code for every requirement like storing the elements based on some sorting order, search for an element is there or not in the array etc. 
> Note: 1. To store the elements based on some sorting order we go for *TreeSet*. 
        2. *contains()* method is available in Collections to search an element.
4. To use arrays, it is better to know the size in advance, which is may not possible always.
   Ex: al >  Index  0 1 ………. 9999999 Suppose, we have 1 Crore elements in an ArrayList. 
   If we want to insert a new element, then a new ArrayList is created with 1Cr + 1 size, all 1Cr elements are copied from old ArrayList       to 1 2 …………… 1 Crore
2. new ArrayList with the same reference variable (al), now the old object is eligible for garbage collection and the new element is inserted to new ArrayList. It takes huge amount of time.



