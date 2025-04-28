# Frontend Mentor - Ricky's 'product preview card component' solution

<figure>
<img scr="./design/desktop-preview.jpg"/>
<figcaption>Desktop Preview</figure>

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 



## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

This project defintely tested my patience. I restarted the project 4x; a total of 5x writing code for this design. 

Reason being, I didn't have any structure or planned my code ahead of time (i.e., trying to make sense 

of what I'm about to execute). This in return, made me disorganized throughout the project and I began complicating 

simple solutions to even more difficult tasks (more on this in the ### 'What I learned' section). I eventually got 

help from <a href="https://www.youtube.com/watch?v=9aDqk7jUMZQ" target="_blank">'Mr Coder'</a>, the other reason I wrote the code again. 

That said: 

(Same Day)
--I wrote the first execution of the code through my own knowledge 
--Second execution, deleted everything tried it all over again
--Third execution was trying to fix errors within the second execution
--Fourth execution, deleted eveything again and followed along Mr Coder 
____________________________________________________________________
(Next Day)
--Reviewd my notes and planned out my code and deleted the code again
--Fifth execution I coded the design with eveything I've learnt from Mr Coder and used my other projects as reference points as well 

For me, there is such an adavantage when you hold yourself accountable when following a video along. I tend to test myself after the 

video in order for me to fully grasp the definitions and concepts, helping me to always stay honest and to continue learning. 

Happy coding & Blessings to all 


### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Screenshot

<img src="./My Desktop Design.png"/>
<img src="./My Mobile Design.png"/>


### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

* I usually speak first on HTML and the CSS afterwards, but on this project I need to speak about both at the same, since there was so much correlation between them. Seperating them would be too much of a hassle to try and make sense of things 

HTML & CSS: 

My HTML process started off super disorganized by not creating proper class names nor using HTML semantics, and making unecessary groupings that led to difficult implementation of the Flexbox Rule:

--I was grouping 'PERFUME, the Product name and the description' all in one container. 
I then grouped the 'price and button' all in one container, which ended up not being 
as effective:

```html

<div class="card">
  <div class="top-header">
    <h6>Perfume</h6>

    <h2>Gabrielle Essence Eau De Parfum</h2>

    <p>A floral, solar and voluptuous interpretation composed by Olivier Polge, Perfumer-Creator for the House of CHANEL.</p>
</div>

  <div class="bottom-header"> 
    <section class="price">
      <p>$149.99</p>
      <p class="cross-line">$169.99</p>
    </section>

    <button class="button">
      <img src="./images/icon-cart.svg" alt="icon-cart">
      <p>Add to Cart</p>
    </button>
  </div>
</div>
  ```



```css
.card {
display: flex; 
flex-direction: column; 
justify-content: space-around;
}
```
I wasn't seeing proper spacing-around my items within my .card since they were not grouped correctly, so the space was just created by 2 items. 

--Now before I corrected this mistake, I went even further adding more errors by trying to only fix the CSS and not the HTML:

```css
  .card > h6 {
    position: relative;
    bottom: 50px;
  }

  .card > h2 {
    position: relative;
    bottom: 50px;
  }
```

...take in mind I also did this for the .price section and the button. It was a pain once I had to shrink the screen size down. Nothing maintain itself within the containers, since everthing was positioned out placed, clearly.

I corrected this by creating 5 items in order for the Flexbox to repsond properly, and gave 
them proper names:

 (I also didn't realize that you can put classes within the HTML tags)

 ```html
  <article class="card-content">
        <h6 class="product">Perfume</h6>

        <h2 class="product-name">Gabrielle Essence Eau De Parfum</h2>

        <p class="product-des">A floral, solar and voluptuous interpretation composed by Olivier Polge,
          Perfumer-Creator for the House of CHANEL.</p>

        <section class="price">
          <p class="new-price">$149.99</p>
          <p class="old-price">$169.99</p>
        </section>

        <button class="button">
          <img src="./images/icon-cart.svg" alt="icon-cart">
          <p class="button-text">Add to Cart</p>
        </button>
      </article>
  ```

  ```css
  .card-content {
    padding: 35px;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
}
  ```

... this then worked like a charm; spacing all items out evenly. 

--Another difficult task I had was putting the img and content side by side using Flex-box to .card. At first I used CSS Grid but it easier using Flexbox:

```css
.card {
  display: flex;
}
```
...this did put the image and content next one another, however, I was struggling to make everything responsive. In the end, this was making things more complicated for me (maybe this could have still worked) despite how easy it was to use. I then used CSS Grid again since it made sense to use it after seeing <a href="https://www.youtube.com/watch?v=9aDqk7jUMZQ" target="_blank">'Mr Coder's</a> explanation for it: 

```css
.card {
    background-color: hsl(0, 0%, 100%);
    max-width: 600px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    border-radius: 13px;
    overflow: hidden;
}
```

--After all this eveything else was very easy to execute, i.e., fonts, color, font size, line-height, and the rest of the samll details. 






### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Desktop-first workflow

### What I learned

Main takeways I learned from this project were how to:

--properly name the tags 
--group items
--implement CSS Grid & Flexbox with one another

The CSS rules I learned were:

--overflow: hidden;
--display: inherit;
--transform: uppercase;


## Useful resources

These are all the helpful resources I used during this project:

--<a href="https://www.youtube.com/watch?v=9aDqk7jUMZQ" target="_blank">'Mr Coder Solution</a> 
--<a href="https://www.w3schools.com/html/html5_semantic_elements.asp" target="_blank">W3Schools: HTML Semantic Elements</a>

## Author

--Website: (https://www.rarroyoharo.com)<a href="https://www.rarroyoharo.com" target="_blank">rarroyoharo.com</a> 
--Frontend Mentor - [@RiickyRiick]<a href="https://www.frontendmentor.io/profile/RiickyRiick" target="_blank">@RiickyRiick</a> 



## Acknowledgments

- Mr Coder


