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