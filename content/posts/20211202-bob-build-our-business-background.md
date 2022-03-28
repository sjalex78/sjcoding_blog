---
title: "Developing BOB"
date: 2021-12-02T11:25:06+11:00
draft: false
---

## So who is BOB?

  Bob stands for BUILD OUR BUSINESS and is an app designed to help businesses to find, store and share software business tools ideas. BOB was developed in the last weeks of Le Wagon Boot Camp batch #757 by Le Wagon sudents: [Sarah](https://github.com/sjalex78/), [Yan](https://github.com/yansunnyboy/) and [Emmanual](https://github.com/Mdg32). 

  Would you like to Explore the app BOB online [Click HERE](https://le-bob-app.herokuapp.com/) please note for best experience check it out in mobile view!

### The Problem

> <ins> **Target:** </ins> People looking for software to leverage to grow their businesses & complete tasks more efficiently.  
 <ins> **Pain:** </ins> Business owners & freelancers spend precious time trying to find the right software to use to complete their next task.  
<ins> **Solution:** </ins> An all-in-one business software Wiki application with relevant software categorised for ease of access.  
<ins> **Originality:** </ins> Rather than scouring blog posts and review sites on search engines, they can access relevant info in one place.

### Product Overview
After and increible fortnight of huge learning curves, long nights coding and moments of panic our team uas able to finish the BOB app and present at the batch #757 [pitch night](/posts/presenting-bob/)! 

> | <img src="/images/bob/FindingProductCreateList.gif" alt="drawing" width="300"/> | <img src="/images/bob/UpvoteProducts.gif" alt="drawing" width="300"/> |
|:--| :--|
| Fig 1. BOB Find Products </br> - Save Products- Create a List  | Fig 2. BOB Upvote Products </br> - On Saved Lists |

## Backend

### Gems

BOB utilized a number of gems in addition to general rails gems to help with the functionality of the final product: 
> | <ins> Gem </ins> | <ins> Function for BOB </ins> | <ins> Detail </ins> |
| :---------  | :---------------  | :--------------- | 
|['acts-as-taggable-on'](https://github.com/mbleigh/acts-as-taggable-on) <br />  --- |To categorise Products <br />  ---  |  used to categorise products, enable multiple <br />  categorgies to be allocated to one product <br />  --- |
| ['pagy'](https://ddnexus.github.io/pagy/api/pagy.html#gsc.tab=0) <br />  --- | Use to paginate <br />  --- | particularly useful when we were in development <br /> and wanting to easily navigate from different views <br />  ---  |
| ['acts_as_votable'](https://github.com/ryanto/acts_as_votable) <br />  ---  | used to vote of products <br /> in a list  <br />  ---  | Enbles many colaborators of a list to <br /> to vote on a product on a list <br />  ---  |
| ['stimulus-rails'](https://github.com/hotwired/stimulus-rails) <br />  ---  | a javascript library tied into <br /> rails library  <br />  --- | when product was pressed the "to add" number <br /> was automatically updates without having to update <br />the server <br />  --- |
| ['rqrcode'](https://github.com/whomwah/rqrcode) <br />  --- | qr code generation <br />  ---   | let BOB generate a QR Code to share a given list <br />  --- |
| ['jwt'](https://github.com/jwt/ruby-jwt)  <br />  ---     | jwt for token signing <br />  --- | worked wth qrqrcode gem let BOB generate <br /> a QR Code to share a given list  <br />  --- | 


### The Model Structure
Our model was made up of 5 tables and data for the product cards scrapped from [Product Hunt](https://www.producthunt.com/).
> <img src="/images/portfolio/bob_db_schema.jpg" alt="drawing" width="300"/>


## The User Experience

When faced with creating an app with 3 enthusiastic juniors what the app looks like becomes a challenge. Load of ideas and how do we consolidate and agree on the final visuals? As a group we had a number of design sessions starting with crazy eights, some good old manual wireframing and also hunting for inspiration on the web. The final 

### BOB Design
Our final design utilized the ideas generated form our crazy eights, wireframe work and inspirations (see below). The bright colours and simple designed aimed to have a minimalist look for a mobile app. simple bright colours to create a "brand" presence.....

> <img src="/images/portfolio/bob_landing_page.png" alt="drawing" height="500"/> 



### Crazy Eights  
An early initative was to undertake some crazy eight to help the group decide in the "look" for BOB. [Want to know what CRAZY 8's is all about?](https://designsprintkit.withgoogle.com/methodology/phase3-sketch/crazy-8s#:~:text=Crazy%208's%20is%20a%20core,of%20solutions%20to%20your%20challenge.)

> | <img src="/images/bob/sarah_ideas.jpeg" alt="drawing" height="300"/> | <img src="/images/bob/yan_Ideas.jpg" alt="drawing" width="300"/> | <img src="/images/bob/emmanual_ideas.jpg" alt="drawing" height="300"/> |
|:--| :--| :--|
| Sarah's Crazy Eights | Yan's Crazy Eights | Emmanual's Crazy Eights|


### Wireframe... paper style 
Design is hard and when it came crunch time we reverted to good old paper and pen... 
> "A Paper wireframe is a sketch or drawing that represents the skeleton of a website or an app interface. As the name suggests, it is often done on a sheet of paper or a whiteboard using a pencil or a pen for rapid simulation and testing. The designers translate their ideas into a sheet of paper to represent how the digital product would appear in the end. This way, the designers can communicate their ideas to developers, managers, and relevant stakeholders with a sketch on a sheet of paper." [Peter Martinez] (https://mockitt.wondershare.com/wireframe/paper-wireframe.html)

> <img src="/images/bob/IMG_8664.jpg" height="300"/> <img src="/images/bob/IMG_8666.jpg" height="300"/> <img src="/images/bob/IMG_8665.jpg" height="300"/> <img src="/images/bob/IMG_8667.jpg" height="300"/> <img src="/images/bob/IMG_8668.jpg" height="300"/> <img src="/images/bob/IMG_8669.jpg" height="300"/> <img src="/images/bob/IMG_8670.jpg" height="300"/> <img src="/images/bob/IMG_8672.jpg" height="300"/>
 
 At a critical point in production a one hour session deciding on the user flow and user interfact design enabled us as a team to work of differnt areas of the deig co-currently with the same "image" in our minds.
### Inspirations
 The internet can be a terrific space for inspiration and yet overwhelming without other ideas in mind... we utilized the following to help focus on functionality rather than spending lots of time on front end when the deadline mattered. This design underpinned the final design was found on [Canva](https://www.canva.com/design/DAEuwg41S6M/UQi5an9_FbdMYTLUa1r-Cw/view?utm_content=DAEuwg41S6M&utm_campaign=designshare&utm_medium=link&utm_source=viewer)
> <img src="/images/portfolio/inspiration_user_interface.png" height="300"/>


## The Team
Our team was made of a dynamic group of individuals for a wide variety of backgrounds from engineering, education to bussiness. It was ultimately a terrific diversity that helped to shape the final product...

<img src="/images/portfolio/20211203_LeWagon_0116.jpg" alt="drawing" width="300"/> <img src="/images/bob/20211203_le_Wagon_15.jpg" alt="drawing" width="300"/>  <img src="/images/portfolio/20211203_LeWagon_0119.jpg" alt="drawing" width="300"/> 

## Pitch Night 

{{< youtube id="dd8ovS0jiLw" autoplay="true" >}}

