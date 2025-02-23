# ArrayList-Solved
ArrayList Solved

**Download Link:https://programming.engineering/product/arraylist-solved/**

Description
5/5 – (2 votes)
You are to code an ArrayList, which is a list data structure backed by an array where all of the data is contiguous and aligned with index 0 of the array.

The ArrayList must follow the requirements stated in the javadocs of each method you must implement.

A constructor stub is provided for you to ll out.

Capacity

The starting capacity of the ArrayList should be the constant INITIAL CAPACITY de ned in ArrayList.java.

Reference the constant as-is. Do not simply copy the value of the constant. Do not change the constant. If, while adding an element, the ArrayList does not have enough space, you should regrow the backing array to twice its old capacity. Do not resize the backing array when removing elements.

Adding

You will implement three add() methods. One will add to the front, one will add to the back, and one will add to anywhere in the list given a speci c index. When adding to the front or the middle of the list, subsequent elements must be shifted back one position to make room for the new data. See the javadocs for more details.

Removing

You will also implement three remove() methods – from the front, the back, or anywhere in the list given a speci c index. When removing from the front or from the middle of the list, the element should be removed and all subsequent elements should be shifted forward by one position. When removing from the back, the last element should be set to null in the array. All unused positions in the backing array must be set to null. See the javadocs for more details.

Amortized E ciency

The e ciency of methods and algorithms in this course is often analyzed using a \per operation” analysis. That is, what is the worst this algorithm can do on any one instance? However, there are times where this type of analysis is unrealistically pessimistic. For example, in this homework, the addToBack() method is O(1) for the most part except in the case of resizing, which is O(n). However, a resize operation is rare enough that it’d be misleading to say that the method is O(n).

In cases like this, we use an amortized analysis. This type of analysis adds up the cost of a series of operations and then averages the cost. Here, the resize step is O(n), but since we double the capacity whenever the array gets full, we will not need to resize for another n add operations. So, putting that together with the common, cheap O(1) operations, we get O(1) using this analysis. Whenever this type of analysis is used, we will pre x the Big-O with the word amortized.

Equality

There are two ways of de ning objects as equal: reference equality and value equality.

Reference equality is used when using the == operator. If two objects are equal by reference equal-ity, that means that they have the exact same memory locations. For example, say we have a Person object with a name and id eld. If you’re using reference equality, two Person objects won’t be considered equal unless they have the exact same memory location (are the exact same object), even if they have the same name and id.

Value equality is used when using the .equals() method. Here, the de nition of equality is custom

Homework 1: ArrayList Due: See Canvas

made for the object. For example, in that Person example above, we may want two objects to be con-sidered equal if they have the same name and id.

Keep in mind which makes more sense to use while you are coding. You will want to use value equality in most cases in this course when comparing objects. Notable cases where you’d use reference equality include checking for null or comparing primitives (in this case, it’s just the == operator being overloaded).

Di erences between Java API and This Assignment

Some of the methods in this assignment are called di erent things or don’t exist in Java’s ArrayList class. This won’t matter until you tackle coding questions on the rst exam, but it’s something to be aware of. The list below shows all methods with a di erent name and their Java API equivalent if it exists. The format is assignment method name ) Java API name.

addAtIndex(int index, T data) ) add(int index, T data)

addToFront(T data) ) no explicit method

addToBack(T data) ) add(T data)

removeAtIndex(int index) ) remove(int index)

removeFromFront() ) no explicit method

removeFromBack() ) no explicit method

Homework 1: ArrayList Due: See Canvas

Grading

Here is the grading breakdown for the assignment. There are various deductions not listed that are incurred when breaking the rules listed in this PDF and in other various circumstances.

Methods:

constructor

1pts

addAtIndex

15pts

addToFront

11pts

addToBack

11pts

removeAtIndex

11pts

removeFromFront

7pts

removeFromBack

7pts

get

6pts

isEmpty

3pts

clear

3pts

Other:

Checkstyle

10pts

E ciency

15pts

Total:

100pts

Provided

The following le(s) have been provided to you. There are several, but we’ve noted the ones to edit.

ArrayList.java

This is the class in which you will implement the ArrayList. Feel free to add private helper methods but do not add any new public methods, inner/nested classes, instance vari-ables, or static variables.

ArrayListStudentTest.java

This is the test class that contains a set of tests covering the basic operations on the ArrayList class. It is not intended to be exhaustive and does not guarantee any type of grade. Write your own tests to ensure you cover all edge cases.

Deliverables

You must submit all of the following le(s). Make sure all le(s) listed below are in each submission, as only the last submission will be graded. Make sure the lename(s) matches the lename(s) below, and that only the following le(s) are present. If there are multiple les, do not zip up the les before submitting; submit them all as separate les.

Once submitted, double check that it has uploaded properly on Gradescope. To do this, download your uploaded le(s) to a new folder, copy over the support le(s), recompile, and run. It is your sole responsibility to re-test your submission and discover editing oddities, upload issues, etc.

ArrayList.java
