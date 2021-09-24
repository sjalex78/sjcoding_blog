---
title: Control flow in Ruby
author: Sarah

date: 2021-07-07T23:03:18+00:00
url: /2021/07/08/control-flow-in-ruby/
categories:
  - Uncategorized
tags:
  - elsif
  - if

---
Woah this is when my maths logic really needs to boot in. The if, else, elsif, unless can really start to get tricky when considering you combine a whole heap of operators&#8230; particularly the and ones! 

<blockquote class="wp-block-quote">
  <p>
    <strong>&&</strong> aka same as
  </p>
  
  <p>
    <strong>!! </strong>aka inclusive
  </p>
  
  <p>
    <strong>! </strong>aka not
  </p>
  
  <cite>and operators can get a bit tricky with your logical grey matter 😉</cite>
</blockquote>

<div class="wp-block-group">
  <div class="wp-block-group__inner-container">
    <div class="wp-block-group">
      <div class="wp-block-group__inner-container">
        <div class="wp-block-columns">
          <div class="wp-block-column" style="flex-basis:100%">
            <figure class="wp-block-gallery columns-3 is-cropped">
            
            <ul class="blocks-gallery-grid">
              <li class="blocks-gallery-item">
                <figure><a href="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-5.34.35-pm.png"><img loading="lazy" width="150" height="150" src="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-5.34.35-pm-150x150.png" alt="" data-id="1179" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-5.34.35-pm.png" data-link="https://sarahjalexander.com/?attachment_id=1179" class="wp-image-1179" /></a></figure>
              </li>
              <li class="blocks-gallery-item">
                <figure><a href="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-6.08.22-pm.png"><img loading="lazy" width="150" height="150" src="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-6.08.22-pm-150x150.png" alt="" data-id="1175" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-6.08.22-pm.png" data-link="https://sarahjalexander.com/?attachment_id=1175" class="wp-image-1175" /></a></figure>
              </li>
              <li class="blocks-gallery-item">
                <figure><a href="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-6.03.43-pm.png"><img loading="lazy" width="150" height="150" src="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-6.03.43-pm-150x150.png" alt="" data-id="1176" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-6.03.43-pm.png" data-link="https://sarahjalexander.com/?attachment_id=1176" class="wp-image-1176" /></a></figure>
              </li>
              <li class="blocks-gallery-item">
                <figure><a href="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-5.59.39-pm.png"><img loading="lazy" width="150" height="150" src="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-5.59.39-pm-150x150.png" alt="" data-id="1177" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-5.59.39-pm.png" data-link="https://sarahjalexander.com/?attachment_id=1177" class="wp-image-1177" /></a></figure>
              </li>
              <li class="blocks-gallery-item">
                <figure><a href="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-5.32.56-pm.png"><img loading="lazy" width="150" height="150" src="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-5.32.56-pm-150x150.png" alt="" data-id="1180" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-5.32.56-pm.png" data-link="https://sarahjalexander.com/?attachment_id=1180" class="wp-image-1180" /></a></figure>
              </li>
              <li class="blocks-gallery-item">
                <figure><a href="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-5.32.13-pm.png"><img loading="lazy" width="150" height="150" src="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-5.32.13-pm-150x150.png" alt="" data-id="1181" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-5.32.13-pm.png" data-link="https://sarahjalexander.com/?attachment_id=1181" class="wp-image-1181" /></a></figure>
              </li>
              <li class="blocks-gallery-item">
                <figure><a href="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-5.16.55-pm.png"><img loading="lazy" width="150" height="150" src="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-5.16.55-pm-150x150.png" alt="" data-id="1182" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-5.16.55-pm.png" data-link="https://sarahjalexander.com/?attachment_id=1182" class="wp-image-1182" /></a></figure>
              </li>
              <li class="blocks-gallery-item">
                <figure><a href="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-5.14.40-pm.png"><img loading="lazy" width="150" height="150" src="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-5.14.40-pm-150x150.png" alt="" data-id="1184" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-5.14.40-pm.png" data-link="https://sarahjalexander.com/?attachment_id=1184" class="wp-image-1184" /></a></figure>
              </li>
              <li class="blocks-gallery-item">
                <figure><a href="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-5.16.48-pm.png"><img loading="lazy" width="150" height="150" src="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-5.16.48-pm-150x150.png" alt="" data-id="1183" data-full-url="https://sarahjalexander.com/wp-content/uploads/2021/07/Screen-Shot-2021-07-07-at-5.16.48-pm.png" data-link="https://sarahjalexander.com/?attachment_id=1183" class="wp-image-1183" /></a></figure>
              </li>
            </ul></figure>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>