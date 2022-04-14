---
title: "Building out code to execute from a ruby file"
date: 2022-04-12T15:38:01+11:00
draft: false
categories:
  - learning
  - love
  - date
  - time

---
## Creating code to read in command line arguments
I am a very visual learner and need visual feedback when coding to "see" what the code and the data is doing. Using commands such as `irb` ("interactive Ruby") in the terminal is a powerful and fast technique that helps to understand the action of a given method, what it returns and how it iteracts with data while `RSpec` tests really help to build out a complete and robust solution. But I really want to see how my code is working as I build out a solution in a quick and straight forward way. For example when I have a ruby class and want to run it ad-hoc with various parameters. To do this I need to create some executable code that is easily run in the terminal. Here is my guide on how to do this.....I am using my [wedding calculator tool](/posts/20220412-calculating-love/) in the example

### Generating an executable ruby file
If you ever want to see the list of command-line options that are available for the ruby command in the terminal you can simply type

``` sh
ruby -h
 ```

To build my code and try to "get it to work" I build up the code and view effects using `pp` (pretty print) which will print to the terminal as I go...
- `-e`  command-line option that executes the code
- [`ARGV`](https://ruby-doc.org/core-3.1.0/ARGF.html) creates an array from the arguments passed to your script

---

``` sh
ruby -e 'pp ARGV'

=> []
```

Returns an empty array, as there are no parameters passed in.

---

``` sh
ruby -e 'pp ARGV' 2000-01-01 2000-01-01

=> ["2000-01-01", "2000-01-01"]
```

Returns an array with the 2 arguments that are passed into the script.

---

``` sh
ruby -e 'pp WeddingCalculator.half_life(wd: ARGV[0], dob: ARGV[1])' 2000-01-01 2000-01-01

=> uninitialized constant WeddingCalculator (NameError)
```

returns an **`ERROR`** - this prompts us to actually include the ruby class we are calling

``` ruby
require "wedding_calculator"
```

---

``` sh
ruby -e 'require "wedding_calculator";\
  pp WeddingCalculator.half_life(wd: ARGV[0], dob: ARGV[1])' 2000-01-01 2000-01-01

=> cannot load such file -- wedding_calculator (LoadError)
```

**`ERROR`** ruby does not know where to find the file called
`wedding_calculator`. Typically this is in a `lib/*` location and in this
example it is the file `lib/wedding_calculator.rb`. Looking at the `ruby -h`
options we see that

```
-Idirectory     specify $LOAD_PATH directory
```

sounds like it may help us where to load the file from, in our case replacing
`directory` with the actual directory `lib`

---

``` sh
ruby -Ilib -e 'require "wedding_calculator"; \
  pp WeddingCalculator.half_life(wd: ARGV[0], dob: ARGV[1])' 2000-01-01 2000-01-01
```

---

``` sh
ruby -Ilib -e 'require "wedding_calculator"; \
   pp WeddingCalculator.half_life(wd: ARGV[0], dob: ARGV[1])' 2000-01-01 2000-01-01

=> "2000-01-01"
```

**_WOOHOO Success_**
Now we need to take this code and store it to run anytime....

### Putting the code into an executable script

Create a bin directory and run.rb file.....

``` sh
mkdir bin
touch bin/run.rb
```

add the code solution to the run.rb file

``` ruby
#!/usr/bin/env ruby
# frozen_string_literal: true

# (this does the -e below)
# once off change file to exercutable for a invisible list ls -l
# chmod +x bin/run.rb

# the code solution:
#   ruby -Ilib -e 'require "wedding_calculator"; \
#     pp WeddingCalculator.half_life(wd: ARGV[0], dob: ARGV[1])' 2000-01-01 2000-01-01

$LOAD_PATH << File.join(__dir__, '..', 'lib')

require 'wedding_calculator'

pp WeddingCalculator.half_life(wed: ARGV[0], dob: ARGV[1])

# to run in terminal bin/run.rb 2000-01-01 2000-01-01

# this is my example of being able to run a ruby file in the command line
```

### Running the new script

``` sh
bin/run.rb

=> zsh: no such file or directory: bin/run.sh
```

which means time for some investigation, lets "List files in the long format"

---

``` sh
ls -l bin

-rw-r--r--  1 sarahalexander  staff  313 Apr 12 17:49 run.rb
```

this output indicted that the files are `r = readable`, `w = writable` but no sign of any `x = executable` so now we need to change the state of the file to allow executable status of the file.

---

``` sh
chmod +x bin/run.rb
```

- `chmod` command (change mode) Modifies File Permissions and `+x` adds the executable state to the run.rb file
and now lets check out the status.....

---

``` sh
ls -l
-rwxr-xr-x  1 sarahalexander  staff  313 Apr 12 17:49 run.rb
```

**WOOHOO an x!**

---

``` sh
bin/run.rb

=> nil
```

And yes we need to pass two arguments

---

``` sh
bin/run.rb 2000-01-01 2000-01-01

=> "2000-01-01"
```

**_The solution appears_**
