---
title: "Building code for executing a ruby file"
date: 2022-04-12T15:38:01+11:00
draft: false
categories:
  - learning
  - love
  - date 
  - time

---
## Creating code to run a ruby file with parameters
I am a very visual learning and need the feedback when coding to "see" what the data is doing. Using commands such as irb("interactive Ruby") in the terminal is a powerful tool that helps to understand the action of given method to the data while rspec tests really help to build a solution. But I really want to see how my code is working as I build a solution in a quick and straight forward way. When I have a ruby file and want to pass it a few parameters. To do this I need to create some executable code that is easily run in the terminal. Here is my guide on how to do this.....I am using my [wedding calculator tool](/posts/20220412-calculating-love/) in the example 

### Generating the executable ruby code
If you every want to see the list of command-line options are available for the ruby command in the terminal you can simply type 
``` terminal
ruby -h 
 ```
 
To build my code and try to "get it to work" I build up the code using pp (pretty print) when will print to the terminal as I go...
- -e  command-line option that executes the code
- ARGV creates a special array

***
``` terminal
ruby -e 'pp ARGV'  --> []
```
Creates and empty array. 

***
``` terminal
ruby -e 'pp ARGV' 2000-01-01 2000-01-01 --> ["2000-01-01", "2000-01-01"]
```
2 arguments are added to the array. 
***
``` terminal
ruby -e 'pp WeddingCalculator.half_life(wd: ARGV[0], dob: ARGV[1])' 2000-01-01 2000-01-01
```
***error*** created "uninitialized constant WeddingCalculator (NameError)" this prompts to ***require "wedding_calculator"*** the name of the the solution file 
***
``` terminal
ruby -e -Ilib 'require "wedding_calculator" ; pp WeddingCalculator.half_life(wd: ARGV[0], dob: ARGV[1])' 2000-01-01 2000-01-01
```
***error*** created "uninitialized constant Ilib (NameError)"
THis error prompts the $LOAD_PATH directory is needed for the solution file "wedding_calculator" the order change, using the command-line option -Idirectory in this case Ilib (lib being the folder name) is added 
***
``` terminal
ruby -Ilib -e 'require "wedding_calculator" ; pp WeddingCalculator.half_life(wd: ARGV[0], dob: ARGV[1])' 2000-01-01 2000-01-01
```
***error*** created uninitialized constant Ilib (NameError) prompts the order of the command-line options (-e and -Ilib) the code need to got to the folder then execute thus we change the order of the commands
***
``` terminal
ruby -Ilib -e 'require "wedding_calculator" ; pp WeddingCalculator.half_life(wd: ARGV[0], dob: ARGV[1])' 2000-01-01 2000-01-01 --> "2000-01-01"
```
***WOOHOO Success***
Now we need to take this code and store it to run anytime....

### Storing the code
Create a bin directory and run.rb file.....

``` terminal
mkdir bin ➜  cd bin ➜  touch run.rb
```

add the code solution to the run.rb file
``` ruby 
#!/usr/bin/env ruby
# frozen_string_literal: true

# (this does the -e below)
# once off change file to exercutable for a invisible list ls -l
# chmod +x bin/run.rb

#  the code solution: ruby -Ilib -e 'require "wedding_calculator" ; pp WeddingCalculator.half_life(wd: ARGV[0], dob: ARGV[1])' 2000-01-01 2000-01-01

$LOAD_PATH << File.join(__dir__, '..', 'lib')

require 'wedding_calculator'

pp WeddingCalculator.half_life(wed: ARGV[0], dob: ARGV[1])

# to run in terminal bin/run.rb 2000-01-01 2000-01-01

# this is my example of being able to run a ruby file in the command line

```

### Running the new command
``` terminal
bin/run.rb
```
zsh: command not found: run.rb which means time for some investigation lets look at the "invisible files..."
***
``` terminal
ls -l --> rw-r--r--  1 sarahalexander  staff  313 Apr 12 17:49 run.rb
```
this output indicted that the files are r = readable, w= writable but no sign of any x = executable so now we need to change the state of the file to allow executable status of the file.
***
``` terminal
chmod +x run.rb
```
- chmod command Modifies File Permissions and +x adds the executable state to the run.rb file
and now lets check out the status.....
***
``` terminal
ls -l
```          
-rwxr-xr-x  1 sarahalexander  staff  313 Apr 12 17:49 run.rb
**WOOHOO an x!**
***
``` terminal
bin/run.rb 2000-01-01 2000-01-01 --> nil
```
And yes we need to pass two arguments
***
``` terminal
bin/run.rb 2000-01-01 2000-01-01 
```
"2000-01-01" ***The solution appears***
