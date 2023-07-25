## 1. Write code that executes asynchronously

Our codes are written asynchronously to catch errors and allow time to fetch API response.

```
async () => { 
    try {
        const response = await fetch(url)
    } 
    
    catch(error) {
        console.error(error);
    }
```

## 2. Use callbacks to access values that aren’t available synchronously


## 3. Use promises to access values that aren’t available synchronously

<img width="465" alt="image" src="https://github.com/yuqingwwang/fac-portfolio/assets/44486576/f35dc33b-5f88-4c8d-a2b3-972f2f94786c">

## 4. Use the fetch method to make HTTP requests and receive responses

## 5. Configure the options argument of the fetch method to make GET and POST requests

## 6. Use the map array method to create a new array containing new values

## 7. Use the filter array method to create a new array with certain values removed

## 8. Access DOM nodes using a variety of selectors

## 9. Add and remove DOM nodes to change the content on the page

## 10. Toggle the classes applied to DOM nodes to change their CSS properties

## 11. Use consistent layout and spacing

After coding different pages on our own, we came together to ensure the coherence of our layout and styles.

## 12. Follow a spacing guideline to give our app a consistent feel

We used 2 spaces for indentation.

## 13. Debug client side JS in our web browser

## 14. Use console.log() to help us debug our code

We made constant use of console.log() to debug our codes' handling of edge cases (e.g. when it's past midnight, there's no depature information, we need to display a meaningful message to the user).
