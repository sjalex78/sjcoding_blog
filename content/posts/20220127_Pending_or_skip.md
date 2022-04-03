---
title: "Pending or skip for RSPEC tests"
date: 2022-01-27T08:04:13+11:00
draft: true
categories:
  - learning
  - rspec
  - test driven development
  - ruby
---

### Skip or Pending?

failed test 
``` ruby

An error occurred while loading ./spec/model/shopping_cart_spec.rb.
Failure/Error:
  RSpec.describe ShoppingCart do
  
    it "should calculate correct price for item without discount" do
      # skip
      cart = ShoppingCart.new(Customer.new("test"), [] << Product.new(100, "no_discount_ABCD", "T"))
      order = cart.checkout()
  
      expect(order.total_price).to eq 100.0
    end

NameError:
  uninitialized constant ShoppingCart
# ./spec/model/shopping_cart_spec.rb:5:in `<top (required)>'
No examples found.

Finished in 0.00007 seconds (files took 0.13678 seconds to load)
0 examples, 0 failures, 1 error occurred outside of examples

```