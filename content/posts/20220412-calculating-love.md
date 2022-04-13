---
title: "Calculating Love"
date: 2022-04-13T11:21:54+10:00
draft: false
categories:
  - learning
  - love
  - date 
  - time
---

This year I turned 44 in February and in April will celebrate 22 years of marriage! so much love but rather than getting supper excited about love my maths brain instantly realised that at some point this year i would have been married for half my adult life... but which day would I be able to celebrate this milestone? When would my husband also have this day for himself? Hmmm starts to sound like a coding challenge coming on.....

I wanted to take the opportunity to use some TDD and be able to solve this problem a number of ways I set out to set up a rspec test after I had got my head around the problem. The maths was basic but after a 4 week coding break I really needed to "solve" the problem to see how to write the test. A little back to front but was a great way to get my learning momentum started again. I solved the problem

``` ruby 
  def self.half_life(wed:, dob:)
    wd_seconds = Date.iso8601(wed).strftime('%s').to_i
    dob_seconds = Date.iso8601(dob).strftime('%s').to_i
    tl_seconds = wd_seconds - dob_seconds
    half_life_seconds = wd_seconds + tl_seconds
    half_date = Time.at(half_life_seconds).strftime('%Y-%m-%d')
    "Spouse: On #{half_date} half life spent in marriage"
  end
```
Having one solution that I can visualise gave me the to confidence to write the basic test framework...

```ruby
# frozen_string_literal: true

require 'wedding_calculator'

RSpec.describe WeddingCalculator do
  it 'processes a half life date from a marriage date and dob of spouse 1' do
    expect(WeddingCalculator.half_life(wed: '2000-01-01', dob: '2000-01-01')).to eq 'Spouse: On 2000-01-01 half life spent in marriage'
  end
  it 'processes a half life date from a marriage date and dob of spouse 1' do
    expect(WeddingCalculator.half_life(wed: '2000-01-02', dob: '2000-01-01')).to eq 'Spouse: On 2000-01-03 half life spent in marriage'
  end
  it 'processes a half life date from a marriage date and dob of spouse 1' do
    expect(WeddingCalculator.half_life(wed: '2000-04-29', dob: '1978-02-21')).to eq 'Spouse: On 2022-07-06 half life spent in marriage'
  end
end
```
With the test created I have now created the framework for some coding practice and look forward to solving the problem of love in a few more ways and will also look to develop more tests for love...

#### Sarah On 2022-07-06 half life spent in marriage
#### Michael On 2024-10-28 half life spent in marriage