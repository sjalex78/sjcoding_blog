---
title: "A guide for creating respec tests "
date: 2022-01-14T11:44:53+11:00
draft: false

categories:
  - learning
  - rspec
  - test driven development
  - ruby

---

Having completed a boot camp and now rebooting my learning with [exercism](https://exercism.org/) I wanted to start creating my own tests for some "puzzle" ideas I want to develop. On the advise of a senior developer I created a [tennis game](https://github.com/sjalex78/learning/tree/main/tennis) and use rspec test to help drive this game development. Funny enough this is also a very topical sport to target with the Djokovic saga going on too..  

### Setting up a rspec test environment:

----

#### Create folders & implementation file 
Open a terminal
``` bash
 mkdir <game_name>
 mkdir <game_name>/lib
 cd <game_name>/lib
 touch game.rb 
```
####  Creating the rspec environment 
back in terminal
```bash
cd ..
code . #opens your project
bundle init
```

this will create a Gemfile 
* open Gemfile and modify
* remove *gem "rails"* and change to *gem "rspec"* 

<img src ="/images/blog/Gem_rspec.gif" width="300"/>

```bash
bundle
rspec --init
touch spec/<game>_spec.rb
```
 Now you have created a rspec test folder and test file
<game_name>/spec/<game>_spec.rb
### Creating a rspec test:
----
Open the <game_name>/spec/<game>_spec.rb file 
To have the spec file target the correct implementation file in this case the <game_name>.md place 
		require 'tennis' 
at the top file 
```ruby
RSpec.describe <Game> do
  it "what does the implemntation" do
    expect(method).to eq "expected outcome"
  end
end
```

Two test examples for my tennis game when you want the scores to be Test 1: "Deuce" or Test 2: "Love all"
```ruby
RSpec.describe Tennis do
  # Test 1
  it 'updates the score when server and receiver both win three points each' do
  tennis = Tennis.new
    # pending
    3.times{tennis.server_wins_point}
    3.times{tennis.receiver_wins_point}
    expect(tennis.score).to eq 'Deuce'
  end
  # Test 2
  it 'reports the starting score ' do
    tennis = Tennis.new
    expect(tennis.score).to eq 'love all'
  end
end
```


### Running a rspec test:

----
back in terminal to run the rspec test:
```bash
rspec <game>_spec.rb
```

#### **Passing and Failed Tests**
Now that we have a test we can use the tests to drive our developer enironment we want to turn RED into GREEN
| <img src="/images/blog/pass_test.jpg" width="400"/> | <img src="/images/blog/failed_test.jpg" alt="drawing" width="400"/> |
|:--| :--|
| Green </br> Passed Tests  | RED </br> Failed test need some more work |

### Extra nice to know about a rspec tests:

----
* **eq** means an equality match but there are [others](https://relishapp.com/rspec/rspec-expectations/docs/built-in-matchers) you can use in the rspec test .
* note: method may need to be a class.method eg Tennis.score
* use pending to skip a given test