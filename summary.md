# Summary

Please answer the following 4 questions for each unit test:
1. What is the knowledge point of the test? Where is the official document to the knowledge point?
2. Why the test failed at first?
3. Why you corrected the test that way?
4. Do you have further questions on this knowledge point?

## ExceptionTest
#### should_customize_exception
1. This is about familiarity with Exception superclass.
2. Test failed because NotImplementedException is not the exception expected.
3. I corrected it that way in order to invoke parent methods from superclass Exception.
4. None.

#### should_customize_exception_continued
1. This is about familiarity with Exception superclass.
2. Test failed because NotImplementedException is not the exception expected.
3. I corrected it that way in order to invoke parent methods from superclass Exception.
4. None.

#### should_be_careful_of_the_order_of_finally_block
1. This is about familiarity with how the finally block works. 
2. Test failed because integral max value is not what is expected.
3. I corrected it that way because I know that finally block will always be executed. 
4. None.

#### should_use_the_try_pattern
1. This is about familiarity with try-with-resources statement.
https://docs.oracle.com/javase/tutorial/essential/exceptions/tryResourceClose.html
2. Test failed because it is not empty.
3. I corrected it that way because the resource declaration in the try-with-resource statement automatically calls the method close() that is why
assertFalse it is closed but in actuality when invoked will not automatically call the method close() of interface Closeable.
4. None.

#### should_call_closing_even_if_exception_throws
1. This is about familiarity with try-with-resources statement.
https://docs.oracle.com/javase/tutorial/essential/exceptions/tryResourceClose.html
2. Test failed because logger is not empty.
3. I corrected it that way because I know that method close() is called and added to array logger.
4. None.

#### should_get_method_name_in_stack_frame
1. This is about getting method name in stack frame.
https://www.baeldung.com/java-name-of-executing-method
2. Test failed because NotImplementedException is not expected.
3. I corrected it that way because I need to concat the class and method name where method getCurrentMethodName() was invoked.
4. None.

## InheritanceTest
#### should_be_derived_from_object_class
1. This is about Java Class Hierarchy.
https://docs.oracle.com/javase/tutorial/java/IandI/subclasses.html
2. Test failed because the superclass from which all classes are derived is implicitly Object class.
3. I corrected it that way because class Object is the "is the root of the class hierarchy".
4. None.

#### should_call_super_class_constructor
1. This is about super and this keywords used inside constructors.
https://www.geeksforgeeks.org/difference-super-java/
2. Test failed because array should not be empty since constructors are called.
3. DerivedFromSuperClassWithDefaultConstructor() is called first, however, even though superclass constructor is not explicitly called, compiler automatically
calls the no-argument constructor SuperClassWithDefaultConstructor() of the superclass SuperClassWithDefaultConstructor. This is why it is safe to always write no-arg constructors.
Note that the indices of each elements inside array expected[] is important because it shows the order of the which the constructors are called.
4. None.

#### should_call_super_class_constructor_continued
1. This is about super and this keywords used inside constructors.
https://www.geeksforgeeks.org/difference-super-java/
2. Test failed because array should not be empty since constructors are called.
3. This is the same as above test but this time DerivedFromSuperClassWithDefaultConstructor() called this() which invokes the DerivedFromSuperClassWithDefaultConstructor()
which invokes the SuperClassWithDefaultConstructor() before adding string "DerivedFromSuperClassWithDefaultConstructor.constructor(int)" into the logger.
4. None.

#### should_call_super_class_constructor_more
1. This is about super and this keywords used inside constructors.
https://www.geeksforgeeks.org/difference-super-java/
2. Test failed because array should not be empty since constructors are called.
3. This test is just an extension of the first two tests. This time is uses the super(arg) to call the constructor of the superclass with argument.
4. None.

#### should_call_most_derived_methods
1. This is about method overriding.
2. Test failed because expected is not null.
3. DerivedFromBaseClassForOverriding overriden the method getName() of BaseClassForOverriding.
4. None.

#### should_call_super_class_methods
1. This is about method overriding.
2. Test failed because expected is not null.
3. DerivedFromBaseClassForOverriding overriden the method getName() of BaseClassForOverriding.
4. None.
