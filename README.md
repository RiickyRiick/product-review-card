# Frontend Mentor - Ricky's 'product preview card component' solution


<img scr="./design/desktop-preview.jpg"/>

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

This project tested my patience. I restarted the project four times, a total of five times, writing code for this design. 

The reason is that I didn't have a structure or plan my code ahead of time (i.e., trying to make sense of what I was about to execute). This, in return, made me disorganized throughout the project, and I began complicating simple solutions to complex tasks (more on this in the ### 'What I learned' section). I eventually got help from <a href="https://www.youtube.com/watch?v=9aDqk7jUMZQ" target="_blank">'Mr Coder'</a>, the other reason I wrote the code again. 

That said: 

(Same Day)
--I wrote the first execution of the code through my knowledge 
--Second execution, deleted everything, tried it all over again
--The third execution was trying to fix errors within the second execution
--Fourth execution, deleted everything again and followed along with Mr Coder 
____________________________________________________________________
(Next Day)
--Reviewed my notes and planned out my code, and deleted the code again
--Fifth execution, I coded the design with everything I've learnt from Mr Coder and used my other projects as reference points as well 

For me, there is a significant advantage to holding yourself accountable when following a video alone. I test myself after watching the video to fully grasp the definitions and concepts, which helps me stay honest and continue learning. 

Happy coding & Blessings to all!


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

* I usually speak first about HTML and then CSS afterwards, but on this project, I need to discuss both simultaneously, since there was a significant correlation between them. Separating them would be too much of a hassle to try to make sense of things 

HTML & CSS: 

My HTML process started super disorganized by not creating proper class names and not using HTML semantics, and making unnecessary groupings that led to the complex implementation of the Flexbox Rule:

--I was grouping 'PERFUME, the Product name, and the description' all in one container. 
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
I wasn't seeing proper spacing around my items within my .card since they were not grouped correctly, so only two items created the space. 

--Now, before I corrected this mistake, I went even further, adding more errors by trying only to fix the CSS and not the HTML:

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

...I also did this for the price section and the button. It was a pain once I had to shrink the screen size down. Nothing remained within the containers, as everything was positioned out of place.

I corrected this by creating five items for the Flexbox to respond appropriately, and gave 
The proper names:

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

... This then worked like a charm, spacing all items out evenly. 

--Another difficult task I had was putting the img and content side by side using Flex-box to .card. At first I used CSS Grid, but it's easier using Flexbox:

```css
.card {
  display: flex;
}
```
...this did place the image and content next to each other. However, I was struggling to make everything responsive. In the end, this made things more complicated for me (perhaps it could still have worked), despite how easy it was to use. I then used CSS Grid again since it made sense to use it after seeing <a href="https://www.youtube.com/watch?v=9aDqk7jUMZQ" target="_blank">'Mr Coder's</a> explanation for it: 

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

--After all this, everything else was very easy to execute, i.e., fonts, color, font size, line-height, and the rest of the small details. 






### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Desktop-first workflow

### What I learned

The main takeaways I learned from this project were how to:

--Properly name the tags 
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


