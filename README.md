# preview-card-challenge# Frontend Mentor - Stats preview card component solution

This is a solution to the [Stats preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size


### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS
- Flexbox
- Mobile-first workflow

### What I learned


This is the first Frontend Mentor challenge I finished, so there is much room for improvement. Through completing this project, I learned about CSS properties I hadn't encountered before (such as mix-blend-mode) and HTML attributes (such as srcset). In addition, I found myself struggling with responsive measurements and setting heights and widths of elements, particularly the image nested inside a div. I had to understand the specifics of how the height and width properties work with block vs inline elements.

Below is a snippet illustrating this concept. I initially had set ```height: 100%``` to both ```.card``` and ```.card-img-container```. However, since I had not explicitly set a height on ```.card```, the height was determined by the contents of the container, so the image height was never being contained. Eventually I changed it to the snippet below, where I explicitly set the height of ```.card```, and the image height is now contained inside its container.

```html
<div id="card" class="card">
	<div class="card-child card-img-container">
		<img srcset="images/image-header-mobile.jpg 654w, images/image-header-desktop 540w"
		sizes="(max-width:549px) 654px, 540px" 
		src="images/image-header-desktop.jpg" 
		alt="Employees in an office sitting at a table">
	</div>
</div>
```
```css
	.card {
		display: flex;
		flex-direction: row-reverse;
		max-width: 1000px;
		height: 28em;
	}

	.card-img-container {
		flex: 1 1 50%;
		height: 100%;
		min-height: 100%;
		min-width: 50%;
	}
```

### Continued development

This challenge was a good exercise in practicing layout and helping me discover the gaps in knowledge. In future projects I will continue practicing getting more comfortable with layout and spacing, and particularly with creating responsive designs.

**Note: Delete this note and the content within this section and replace with your own plans for continued development.**

### Useful resources

- [MDN Responsive Images](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images) - I referenced this while learning about and understanding how to use the srcset attribute. I was struggling to get the image to display correctly on both mobile and desktop views, and was able to achieve the result I wanted after reading this.
- [Stackoverflow - Why doesn't percentage height work?](https://stackoverflow.com/questions/5657964/css-why-doesn-t-percentage-height-work) - Since I wanted to make my measurements reponsive, I tried using a percentage on a height property, only to find that it didn't change anything. Although this post is quite old, I learned a lot from the in-depth explanation of the top answer and was able to understand why I wasn't able to set height with a percentage.

