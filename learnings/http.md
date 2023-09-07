## 1 & 2. Write code that executes asynchronously <br> Use callbacks to access values that aren’t available synchronously


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

Another example is the handleSubmit function which is used as a callback for the submit event of a form. This callback is executed when the form is submitted, but it relies on user input and form submission, which are asynchronous actions.

## 3. Use promises to access values that aren’t available synchronously

<img width="465" alt="image" src="https://github.com/yuqingwwang/fac-portfolio/assets/44486576/f35dc33b-5f88-4c8d-a2b3-972f2f94786c">

## 4. Use the fetch method to make HTTP requests and receive responses

We mainly focused on fetching departure information from TfL's API. From there, we selected the features we're interested in and formatted them before displaying the results. 

## 5. Configure the options argument of the fetch method to make GET and POST requests

We have not explicitly configured the options argument of the fetch method to make GET requests and our GET relies on the default behavior of the fetch method.

To improve this, we can do: 

```
function getDepartureTimes(station) {
  // ...
  const requestOptions = {
    method: 'GET', 
  };

  fetch(url + "/" + station_id, requestOptions)
    .then((response) => {
      if (response.ok) {
        return response.json();
      } else {
        console.log(response.status);
        throw new Error("Error retrieving departure times");
      }
    })
    .then((departures) => {
      // ...
    })
    .catch((error) => {
      console.error(error);
    });
}
```
## 6. Use the map array method to create a new array containing new values

We used a for loop to iterate over the departure array. Instead, we can use the map method to create a new array of departureInfo objects. This approach is more concise and easier to read than using a for loop. It also eliminates the need to manually push each object into the departureInfoArray.

## 7. Use the filter array method to create a new array with certain values removed

The following function is made to create a selected list of stations

```
function handleSearch() {
  const searchTerm = searchInput.value.toLowerCase();
  const filteredStations = stations.filter(station => station.name.toLowerCase().includes(searchTerm));
  renderResults(filteredStations);
}
```

## 8, 9, & 10. Access DOM nodes using a variety of selectors <br> Add and remove DOM nodes to change the content on the page <br> Toggle the classes applied to DOM nodes to change their CSS properties

A good example is the [populateTable](https://github.com/fac28/trainspotting-api/blob/develop/js/utils/populateTable.js) function:

- The function uses selectors like inboundTable, outboundTable, tableHead, and tableBody to access and manipulate DOM nodes in the HTML document. It uses querySelector and querySelectorAll to find specific elements in the DOM.

- It adds and removes DOM nodes as needed to populate the table with new data. It clears the existing table contents using the clearTable function and then creates and appends new table rows (<tr>) and cells (<td>) based on the data in the array.

- While the primary purpose of this function is to populate tables, it also applies CSS properties conditionally. For example, it adds the hide-on-small-screen class to certain cells to hide them on smaller screens. This demonstrates the ability to toggle CSS classes to change the appearance of DOM nodes based on specific conditions.

## 11. Use consistent layout and spacing

After coding different pages on our own, we came together to ensure the coherence of our layout and styles.

## 12. Follow a spacing guideline to give our app a consistent feel

We used 2 spaces for indentation.

## 13 & 14. Debug client side JS in our web browser <br> Use console.log() to help us debug our code

We made constant use of the browser and console.log() to debug our codes' handling of edge cases (e.g. when it's past midnight, there's no depature information, we need to display a meaningful message to the user).
