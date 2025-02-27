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
3. I corrected it that way because I know that method close() is called and added to array logger. Also, methods of resources are called in the opposite order of their creation.
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
3. DerivedFromBaseClassForOverridingCallingSuper.getName() is invoked but used the superclass method getName() by the keyword super.getName(). 
4. None.

#### should_use_caution_when_dealing_with_array_type
1. This is about array types and try-catch blocks.
2. Test failed because expected is boolean type.
3. The value of willThrow is true because arrayWithBaseType is null.
4. None.

#### should_not_make_you_confused
1. This is about nesting derivation from parent classes.
2. Test failed because expected is not null.
3. I answered it this way because getName() is overriden by using the @Override annotation.
4. None.

#### should_not_make_you_confused_2
1. This is about deriving methods from parent class. 
2. Test failed because expected is not null.
3. Since method is not existing in current class, then compiler checks from parent class.
4. None.

#### should_use_instance_of_to_determine_inheritance_relationship
1. This is about using instanceof to determine inheritance relationship.
2. Test failed because expected is not empty.
3. The object nested is an instance of NestedDerivedClassWithName and since NestedDerivedClassWithName is a child class of parent DerivedFromBaseClassWithName and BaseClassWithName
then by extension, object nested is an instance of these parent classes.
4. None.

#### should_use_instance_of_only_in_inheritance_relationship
1. This is about using instanceof to determine inheritance relationship.
2. Test failed because expected is not empty.
3. The object integer, although explicitly indicated as of type Object, is not an instanceof Long since Integer is not a child class of Long. 
4. None.

#### should_write_perfect_equals_1
1. This is about checking values from an object and from which class they are made of.
https://docs.oracle.com/javase/7/docs/api/java/lang/Object.html
2. Test failed because method is not implemented.
3. I am aware that intelliJ is able to generate overriden equals() and hashcode() for the developer to use. Also, as per my readings, whenever we override either equals or hashcode,
we should override them both.
4. None.

#### should_write_perfect_equals_2
1. Same as above.
2. Same as above.
3. Same as above.
4. None.

#### should_write_perfect_equals_3
1. Same as above.
2. Same as above.
3. Same as above.
4. None.

#### should_write_perfect_equals_4
1. Same as above.
2. Same as above.
3. Same as above.
4. None.

#### should_write_perfect_equals_5
1. Same as above.
2. Same as above.
3. Same as above.
4. None.

#### should_write_perfect_equals_6
1. Same as above.
2. Same as above.
3. Same as above.
4. None.

#### should_write_perfect_equals_7
1. Same as above.
2. Same as above.
3. Same as above.
4. None.

## ObjectTest
#### should_point_to_the_same_object
1. This is about object identity.
2. Test failed because it is not empty.
3. Both objectReference and sameReference are pointing to the address in memory and thus they are the identical objects.
4. None.

#### should_point_to_different_object
1. This is about object identity.
2. Test failed because it is not empty.
3. Both goodDay and sameDay are pointing to different address in memory and thus they are different objects.
4. None.

#### should_initialized_to_default_value
1. This is about object initial values.
https://www.javaworld.com/article/2076614/object-initialization-in-java.html
2. Test failed because they do not have initial values.
3. If not initialized, variables are assigned default values based on their types.
4. None.

#### should_pass_by_value
1. This is about passing objects by value.
2. Test failed because it is not empty.
3. Original value is retained since it was not actually updated.
4. None.

#### should_pass_by_value_continued
1. This is about passing objects by value.
2. Test failed because it is not empty.
3. Object sameReference is equal to objectReference.
4. None.

#### should_modify_internal_state
1. This is about updating a created object.
2. Test failed because it is not empty.
3. The object is updated because it was the object that was passed and updated inside the method tryingToUpdateState().
4. None.

#### should_choose_method_at_compile_time
1. This is about method overloading.
2. Test failed because it is not empty.
3. The method that was triggered is the method that matched the number of parameter as well as the parameter type, in our case methodWithOneParameter(Object value).
4. None.

#### should_choose_the_most_specific_overload
1. This is about method overloading.
2. Test failed because it is not empty.
3. The method that was triggered is the method that matched the number of parameter as well as the parameter type, in our case methodWithTwoParameters(String string, Integer integer).
Method overloading also try to match the most specific object type.
4. None.

#### should_calling_another_constructor
1. This is about method overloading and keyword this().
2. Test failed because it is not null.
3. The method that was triggered is CallingAnotherCtor() however, this constructor invoked the other constructor passing another parameter: CallingAnotherCtor(String name).
4. None.

#### should_get_initialization_ordering
1. This is about initializers in Java.
2. Test failed because array is not null.
3. The method that was triggered in this order: initializer -> superclass constructors -> current class constructor.
4. None.

#### should_get_message_of_var_length_parameters
1. This is about unknown length of parameter handled in Java methods.
2. Test failed because array is not empty.
3. This is just a simple concatenation of given parameters.
4. None.

#### should_get_message_of_var_length_parameters_2
1. Just an extension of the above test.
2. Test failed because array is not empty.
3. This is just a simple concatenation of given parameters but this time type is given which is not a problem since all objects in Java
are derived from class Object. So, declaring new Object[] is not a problem.
4. None.