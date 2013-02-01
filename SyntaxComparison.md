Language Syntax Comparison
==========================

Comparison of Syntax for different languages. Currently Ruby and C++ (will add others as I use them).
I CANNOT keep object instantiation straight when I bounce back and forth between Ruby and C++.

## Comments

### Ruby
#### Single-line

    # This is a comment

#### Multi-line
  
    =begin
    The =begin and =end CANNOT be indented. It's ugly, I know - one of my
    biggest disappointments with Ruby.
    =end

### C++
#### Single-line

    // This is a comment

#### Multi-line

    /* This is a 
       Multi-line
       Comment
     */

## Functions

### Ruby
#### Declaring/Defining

    def function_no_params  # Don't have to include parentheses
      #some code
    end

    def function_two_params(parameter1, parameter2)
      # some code here
    end

#### Calling

    function_no_params # Can omit parentheses, but buggy - is it a variable, or function name?
    function_no_params() # Not as pretty, but interpreter knows it's a function now

    function_two_params(one, two)
    function_two_params one, two # Can omit pararentheses when calling, BUT can cause issues

### C++
#### Declaring

    int double(int); // Used to let compiler know what you're talking about before defining

#### Defining

    int double(int a) {   // returnType functionName(paramType paramName[, type2 name2, etc...])
      return 2 * a;       // MUST match returnType above
    }

#### Calling
    double(4); // not real useful, as return doesn't go anywhere
    fourTimesTwo = double(4); // better, but obviously function-specific