# Kotlin-important-functions-on-Collections-

1) How to create Map from array or list or set [associate()]

        val array: Array<String> = arrayOf("Android", "Kotlin", "IOS","Swift")
        val list = array.asList()
        val set = array.toSet()
        
        val mapFromArray = array.associateBy {
            it
        }

        val mapFromList = list.associate {
            Pair(it, it.length)
        }

        val mapFromSet = set.associate {
            Pair(it, it.length)
        }
  --------------------------------------------------------------------------
  
  2) How to get index of last element in array or list  [lastIndex]
  
  In Java, we get last index array.length -1 in case Array and list.size() - 1 in case of List
  but in Kotlin we get lastIndex property with array and list.
  
        val array: Array<String> = arrayOf("Android", "Kotlin", "IOS","Swift")
        val lastIndexInArray = array.lastIndex
        
        val list = array.asList()
        val lastIndexInList = list.lastIndex
  
  --------------------------------------------------------------------------
  
  3) How to check wheather all elements in Collection are satisfying condition . [all()]
  
  this function return true when all elements in collection fullfilling mentioned condition
  
        val personAgeList = listOf<Int>(23,21,27,30,36,19)
        val isAllPersonAboveEighteen = personAgeList.all {age ->
            age > 18
        }
 --------------------------------------------------------------------------
 
 4) How to check wheather any element in Collection is following condition. [any()]
 this function check, if that collection contains any element that fullfill mentioned condition
 
        val personList = listOf<Int>(25,21,28,13,6,29)
        val isAnyTeenager = personList.any{age ->
            age in 13..19
        }
        
note: this function is different from any() function that tells Collection contains any element or not.
--------------------------------------------------------------------------
5) chunked function

        val personList = listOf<Int>(25,21,28,13,6,29,33,34,56,45)
        val list = personList.chunked(5) //list will have two elements. first element will be list of first 5 elements in personList. Second element will be list of next 5 elements.
--------------------------------------------------------------------------   
   
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
