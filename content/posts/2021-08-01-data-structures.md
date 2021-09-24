---
title: Data Structures
author: Sarah

date: 2021-08-01T01:02:56+00:00
url: /2021/08/01/data-structures/
categories:
  - Uncategorized

---
 

After a small (lockdown induced break&#8221; I have started again now with a deadline set I am ploughing through. I am battling myself as a learner as my role as a teacher has sarted to be un undoing. I am frustrated with not completley understanding it and struggling with not having the language fluenency to help myself. I can read chemistry, biology, science, gardening, parently&#8230;. this Ruby language is new so I feel slow and clumsy. 



Today my Hash.new, .each and putting data from arrays and array of arrays was on the menu.<figure class="wp-block-gallery columns-2 is-cropped">

<ul class="blocks-gallery-grid">
  <li class="blocks-gallery-item">
    <figure><img loading="lazy" width="300" height="145" src="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.54.44-am-300x145.png" alt="" data-id="1210" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.54.44-am.png" data-link="https://sarahjalexander.com/?attachment_id=1210" class="wp-image-1210" srcset="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.54.44-am-300x145.png 300w, https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.54.44-am.png 624w" sizes="(max-width: 300px) 100vw, 300px" /></figure>
  </li>
  <li class="blocks-gallery-item">
    <figure><img loading="lazy" width="300" height="221" src="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.50.50-am-300x221.png" alt="" data-id="1211" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.50.50-am.png" data-link="https://sarahjalexander.com/?attachment_id=1211" class="wp-image-1211" srcset="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.50.50-am-300x221.png 300w, https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.50.50-am.png 464w" sizes="(max-width: 300px) 100vw, 300px" /></figure>
  </li>
  <li class="blocks-gallery-item">
    <figure><img loading="lazy" width="300" height="102" src="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.48.05-am-300x102.png" alt="" data-id="1212" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.48.05-am.png" data-link="https://sarahjalexander.com/?attachment_id=1212" class="wp-image-1212" srcset="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.48.05-am-300x102.png 300w, https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.48.05-am.png 474w" sizes="(max-width: 300px) 100vw, 300px" /></figure>
  </li>
  <li class="blocks-gallery-item">
    <figure><img loading="lazy" width="300" height="132" src="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.45.56-am-300x132.png" alt="" data-id="1213" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.45.56-am.png" data-link="https://sarahjalexander.com/?attachment_id=1213" class="wp-image-1213" srcset="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.45.56-am-300x132.png 300w, https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.45.56-am.png 766w" sizes="(max-width: 300px) 100vw, 300px" /></figure>
  </li>
  <li class="blocks-gallery-item">
    <figure><img loading="lazy" width="300" height="93" src="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.08.04-am-300x93.png" alt="" data-id="1214" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.08.04-am.png" data-link="https://sarahjalexander.com/?attachment_id=1214" class="wp-image-1214" srcset="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.08.04-am-300x93.png 300w, https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.08.04-am.png 611w" sizes="(max-width: 300px) 100vw, 300px" /></figure>
  </li>
  <li class="blocks-gallery-item">
    <figure><img loading="lazy" width="300" height="57" src="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.04.34-am-300x57.png" alt="" data-id="1215" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.04.34-am.png" data-link="https://sarahjalexander.com/?attachment_id=1215" class="wp-image-1215" srcset="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.04.34-am-300x57.png 300w, https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.04.34-am.png 472w" sizes="(max-width: 300px) 100vw, 300px" /></figure>
  </li>
  <li class="blocks-gallery-item">
    <figure><img loading="lazy" width="241" height="45" src="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-9.10.25-am.png" alt="" data-id="1216" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-9.10.25-am.png" data-link="https://sarahjalexander.com/?attachment_id=1216" class="wp-image-1216" /></figure>
  </li>
  <li class="blocks-gallery-item">
    <figure><img loading="lazy" width="300" height="114" src="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-9.13.30-am-300x114.png" alt="" data-id="1217" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-9.13.30-am.png" data-link="https://sarahjalexander.com/?attachment_id=1217" class="wp-image-1217" srcset="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-9.13.30-am-300x114.png 300w, https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-9.13.30-am.png 400w" sizes="(max-width: 300px) 100vw, 300px" /></figure>
  </li>
  <li class="blocks-gallery-item">
    <figure><img loading="lazy" width="300" height="71" src="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.12.56-am-300x71.png" alt="" data-id="1218" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.12.56-am.png" data-link="https://sarahjalexander.com/?attachment_id=1218" class="wp-image-1218" srcset="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.12.56-am-300x71.png 300w, https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.12.56-am.png 739w" sizes="(max-width: 300px) 100vw, 300px" /></figure>
  </li>
  <li class="blocks-gallery-item">
    <figure><img loading="lazy" width="300" height="137" src="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.39.50-am-300x137.png" alt="" data-id="1219" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.39.50-am.png" data-link="https://sarahjalexander.com/?attachment_id=1219" class="wp-image-1219" srcset="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.39.50-am-300x137.png 300w, https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.39.50-am.png 640w" sizes="(max-width: 300px) 100vw, 300px" /></figure>
  </li>
  <li class="blocks-gallery-item">
    <figure><img loading="lazy" width="300" height="117" src="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.40.55-am-300x117.png" alt="" data-id="1220" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.40.55-am.png" data-link="https://sarahjalexander.com/?attachment_id=1220" class="wp-image-1220" srcset="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.40.55-am-300x117.png 300w, https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.40.55-am-768x298.png 768w, https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-10.40.55-am.png 793w" sizes="(max-width: 300px) 100vw, 300px" /></figure>
  </li>
  <li class="blocks-gallery-item">
    <figure><img loading="lazy" width="300" height="62" src="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-9.15.16-am-300x62.png" alt="" data-id="1221" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-9.15.16-am.png" data-link="https://sarahjalexander.com/?attachment_id=1221" class="wp-image-1221" srcset="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-9.15.16-am-300x62.png 300w, https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-9.15.16-am.png 514w" sizes="(max-width: 300px) 100vw, 300px" /></figure>
  </li>
  <li class="blocks-gallery-item">
    <figure><img loading="lazy" width="300" height="96" src="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-9.34.06-am-300x96.png" alt="" data-id="1222" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-9.34.06-am.png" data-link="https://sarahjalexander.com/?attachment_id=1222" class="wp-image-1222" srcset="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-9.34.06-am-300x96.png 300w, https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-9.34.06-am.png 462w" sizes="(max-width: 300px) 100vw, 300px" /></figure>
  </li>
  <li class="blocks-gallery-item">
    <figure><img loading="lazy" width="455" height="116" src="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-9.38.40-am.png" alt="" data-id="1223" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-9.38.40-am.png" data-link="https://sarahjalexander.com/?attachment_id=1223" class="wp-image-1223" srcset="https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-9.38.40-am.png 455w, https://sarahjalexander.com/wp-content/uploads/2021/08/Screen-Shot-2021-08-01-at-9.38.40-am-300x76.png 300w" sizes="(max-width: 455px) 100vw, 455px" /></figure>
  </li>
</ul></figure>