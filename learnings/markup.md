## 1. Structure a site using semantic HTML to aid accessibility
![code snippets from index.html](https://github.com/yuqingwwang/fac-portfolio/assets/44486576/113223ad-d20c-451e-874f-8c2e5d2bfd59)
 
For the [Monster Inc](https://github.com/fac28/monster-inc) Project, we made use of semantic elements in our HTML files such as \<header>, \<footer> and \<nav> to describe the function of each element. 
  
We did use the non-semantic \<div> tag with a class or id attribute quite often, which harmed the readability and accessibility of our codes. In the future, we should change them into more descriptive tags such as \<section> and \<article>. 

## 2. Ensure a web page is readable for screen readers
We tested our web page on Mac's VoiceOver to make sure all elements are readbale and descriptive.

## 3. Ensure our UI has sufficient colour contrast so that everyone can perceive it comfortably
Here is the [colour pallette](https://coolors.co/ebebe9-ca4335-030305-c9c9c8-ea150e) we created for our webpage.

We used colours with sufficient contrasts, such as black texts on a white background to increase the readability of our page.

## 4. Use various tools to check that our website meets accessibility criteria
The tool we used was [Lighthouse](https://developer.chrome.com/docs/lighthouse/overview/) in Chrome DevTools


## 5. Use CSS media queries to ensure our content is always presented effectively on screens of different sizes
We used media queries for three scenarios: small(max-width: 800px), medium (min-width: 800px) and large (min-width: 1200px) screens. 

## 6. Demonstrate a mobile-first approach to building a website
Here is a snippet of how we made sure all content is displayed properly on mobile screens, by updating the font sizes and column numbers.

```
@media  screen and (min-width: 800px) {

  h1 {
    font-size: 4rem;
  }

  .banner-grid {
    grid-template-columns: 1fr 1fr;
  }

  .description-box p {
    margin: 1rem;
  }

  .banner p {
    font-size: 2rem;
  }

  .margin-top-lg {
    margin-top: 5rem;
  }

}
```

<!-- 
## 7. Use CSS variables to apply repeated colours to HTML elements

## 8. Use CSS Flexbox to style children in a single-direction layout (ie a row or a column)

## 9. Use CSS Grid to style children in two-direction layout

## 10. Ensure our Git commit history tells a coherent story

## 11. Use the appropriate input types in HTML forms for gathering different types of information -->
