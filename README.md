# implement List.indexOf

`while`-style and recursive implementations at the top of
OrderedList_inArraySlots.java

[Java API on the `indexOf` method](https://docs.oracle.com/javase/10/docs/api/java/util/List.html#indexOf(java.lang.Object))

based on [solutionsHolmes/5D_genericTypes/OrderedList_inArraySlots_v2/](https://github.com/stuyvesant-cs/solutionsHolmes/tree/master/5D_genericTypes/OrderedList_inArraySlots_v2)
as of 2019-04-10 04:48

Problem: To find the index of an element in an ordered list.

Recursive Abstraction: When asked to find the index of an element, the recursive abstraction can find the index of that element in one half of the ordered list.

6 Parts of A Recursive Solution:

Decisions: 
- if (low > hi)
- if( comparison == 0) 

Solution to Base Cases: 
Base Case 1 (if (low>hi)):
return -2
Base Case 2 (if( comparison == 0)):
return pageToCheck

Solution to Recursive Cases:
Recursive Case 1 (if( comparison < 0)):
-No combining operator or leftover.
-Recursive Abstraction --> return indexOf_recursive( findMe, low, pageToCheck -1)
Recursive Case 2 (if( comparison > 0)):
-No combining operator or leftover
-Recursive Abstraction --> return indexOf_recursive( findMe, pageToCheck +1, hi)
