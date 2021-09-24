---
title: Creating a Histogram Lockdown 6.0
author: Sarah

date: 2021-08-07T05:58:00+00:00
url: /2021/08/07/creating-a-histogram-lockdown-6-0/
categories:
  - Coding
  - methods
  - ruby
  - string
  - Uncategorized

---
 

Today was the first day of the 6th Lockdown for Melbourne. There is some solis in learning to code in amongst the croazy homeschooling and teaching&#8230;. I also have a deadline to try to get this pre learning done by the end of August. My struggle is coming down to a lack of practice and getting stuck on blocks. 

My Code today cuts up a string, creates an array and looks at the frequency of word in a given input&#8230;&#8230;.<figure class="wp-block-gallery columns-3 is-cropped">

<ul class="blocks-gallery-grid">
  <li class="blocks-gallery-item">
    <figure><img loading="lazy" width="913" height="160" src="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-06-at-2.38.49-pm.png" alt="" data-id="1230" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-06-at-2.38.49-pm.png" data-link="https://sarahjalexander.com/?attachment_id=1230" class="wp-image-1230" srcset="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-06-at-2.38.49-pm.png 913w, https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-06-at-2.38.49-pm-300x53.png 300w, https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-06-at-2.38.49-pm-768x135.png 768w" sizes="(max-width: 913px) 100vw, 913px" /></figure>
  </li>
  <li class="blocks-gallery-item">
    <figure><img loading="lazy" width="934" height="504" src="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-06-at-3.37.09-pm.png" alt="" data-id="1229" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-06-at-3.37.09-pm.png" data-link="https://sarahjalexander.com/?attachment_id=1229" class="wp-image-1229" srcset="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-06-at-3.37.09-pm.png 934w, https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-06-at-3.37.09-pm-300x162.png 300w, https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-06-at-3.37.09-pm-768x414.png 768w" sizes="(max-width: 934px) 100vw, 934px" /></figure>
  </li>
  <li class="blocks-gallery-item">
    <figure><img loading="lazy" width="809" height="226" src="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-06-at-2.43.41-pm.png" alt="" data-id="1231" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-06-at-2.43.41-pm.png" data-link="https://sarahjalexander.com/?attachment_id=1231" class="wp-image-1231" srcset="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-06-at-2.43.41-pm.png 809w, https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-06-at-2.43.41-pm-300x84.png 300w, https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-06-at-2.43.41-pm-768x215.png 768w" sizes="(max-width: 809px) 100vw, 809px" /></figure>
  </li>
  <li class="blocks-gallery-item">
    <figure><img loading="lazy" width="451" height="364" src="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-06-at-3.30.07-pm.png" alt="" data-id="1232" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-06-at-3.30.07-pm.png" data-link="https://sarahjalexander.com/?attachment_id=1232" class="wp-image-1232" srcset="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-06-at-3.30.07-pm.png 451w, https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-06-at-3.30.07-pm-300x242.png 300w" sizes="(max-width: 451px) 100vw, 451px" /></figure>
  </li>
  <li class="blocks-gallery-item">
    <figure><img loading="lazy" width="442" height="452" src="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-06-at-3.36.18-pm.png" alt="" data-id="1233" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-06-at-3.36.18-pm.png" data-link="https://sarahjalexander.com/?attachment_id=1233" class="wp-image-1233" srcset="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-06-at-3.36.18-pm.png 442w, https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-06-at-3.36.18-pm-293x300.png 293w" sizes="(max-width: 442px) 100vw, 442px" /></figure>
  </li>
  <li class="blocks-gallery-item">
    <figure><img loading="lazy" width="3" height="1" src="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-06-at-3.30.00-pm.png" alt="" data-id="1234" data-link="https://sarahjalexander.com/?attachment_id=1234" class="wp-image-1234" /></figure>
  </li>
</ul></figure>