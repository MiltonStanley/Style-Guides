Ruby Style Guide
================
Adapted in large part from http://github.com/styleguide/ruby


* [Project Structure](#project_stucture)
* [Program Structure](#program_structure)
  * [Header statement](#header_statement)
  * [Require declarations](#require_declarations)
  * [Constant declarations](#constant_declarations)
  * [Class declarations](#class_declarations)
  * [Main program](#main_program)
* [Constant](#constants)
* [Class](#class)
* [Method](#methods)


<a id="project_structure">Project Structure</a>
-----------------------------------------------
1. Main directory hosts the parent program and any config files.
2. ./lib hosts all custom 'require' files
  - Except for the smallest scripts, this includes separate files for classes.
3. ./samples holds all data required for testing program
4. ./tests holds unit tests

<a id="program_structure">Program Structure</a>
-----------------

<h3> <a id="header_statement">Header statement</a></h3>
  1. Program name
  2. Version id - MAJOR.MINOR.PATCH:
    * Major number - significant rewrite of code base or user interaction
    * Minor number - minor changes to code or user interaction
    * Patch number - incremented for each patch/fix released
  3. Purpose of program
  4. Lead developer of THIS program
  5. Overall project name
  6. Any unusual requirements (external libraries, etc.)

Example:

    =begin

    Ruby Style Guide
    v 0.1.0
    Style guide for my own Ruby development
    Milton Stanley
    Style Guide project
    
    =end

<h3><a id="require_declarations">Require declarations</a></h3>
  * Begins with one line saying '### REQUIRE DECLARATIONS' in all caps, isolated above and below with one line. This
  is useful for searching, as more than one # looks terrible and cluttered (so don't use more, except as detailed here.)
  * Public/well-known requires are listed first (in alphabetical order)
  * Custom requires from current project written next (in alphabetical order)

Example:

    =end

    ### REQUIRE DECLARATIONS

    require 'jruby'
    require 'ruby_on_rails'
    require './look_ma_I_made_this'
    require './lib/fancy_module_i_designed'
    require './zztop'

<h3><a id="constant_declarations">Constant declarations</a></h3>
  * Again, this section begins with one line reading '### CONSTANT DECLARATIONS' for easy searching.
  * Listed in alphabetical order
  * Located here to make it easier to find and change as needed. More details at [constants](#constants) regarding
  naming, usage, and other related styles issues.


Example:

    require './zztop'

    ### CONSTANT DECLARATIONS

    ALLERGIES = true
    PI = 3   // physicist use
    ZEBRA = 'unicorn, spiral horn melted onto body'


<h3><a id="class_declarations">Class declarations</a></h3>
  * Ideally, class declarations are in their own files (one per class), and should only be
  included here if they are very short or small.
  * Section begins with '### CLASS DECLARATIONS' in ALL CAPS, separated above and below by one line.
  * Each class should be separated from its neighbors by two lines.
  * If they are included here, they should be in alphabetical order by class. More [here](#class)
    * Further, each method of each class should be listed in alphabetical order. More [here](#methods)
    * Each method is separated by one line.

Example:

    ZEBRA = 'unicorn, spiral horn melted on body'

    ### CLASS DECLARATIONS

    class Foo

      def get_value
        @value
      end

      def set_value(_value)
        @value = value
      end

    end


    class Bar

      def fizzbum?(wuh)
        puts "fizzbumming with a #{wuh}!"
      end

    end


<h3><a id="main_program">Main program</a></h3>
  * Begins with single line '### MAIN PROGRAM', separated above and below by one line

Example:

    end

    ### MAIN PROGRAM

    puts "Why bother?"
    Process.exit!

