---
title: Refactoring Ruby
author: Sarah

date: 2021-08-15T02:56:19+00:00
url: /2021/08/15/refactoring-ruby/
categories:
  - Uncategorized

---
 

So if you read this title without knowing that I am learning some Ruby programming you may have started to picture me chipping away at at large red rock (ruby) to create the desired shape for my latest pendent&#8230;. well perhaps 😉 

In some ways this visual could be true if the actual function of the object was not changed. In a nutshell Refactoring Ruby is basically analysing code and making changes that leaves it

<blockquote class="wp-block-quote">
  <p>
    CLEAN SIMPLe and EASY TO MAINTAIN
  </p>
</blockquote>

without effecting the function of the code!

A number of diferent ideas were intorduced and then I was given an opportunity to have a go! for example:

#loop6.times{puts &#8220;Melbourne in lockdown&#8221;}

or 

lockdown=6

&#8220;I am in lockdown&#8221;+ lockdown.to.s +&#8221;!!!!&#8221;

#changes to 

&#8220;I am in lockdown #{lockdown}!!!!&#8221;