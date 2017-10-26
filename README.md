#Image Gallery

Create an `<img>` `#gallery` using the assets provided. When a user `click`s on one of the `.thumb` images, override the `src` of the default `#main` image with the `src` of the image that was clicked.

1. First consider that we only have three thumbnails. Create a separate event listener for each of the three thumbnail's `id`
2. Now consider that selecting all three elements using `querySelectorAll()` and traversing the resulting array with a `for` loop would be more efficient code-wise. Use the keyword `this` to target the current `.thumb` element while within the loop
3. Try the same approach, but using forEach() instead. Consider how much cleaner this code appears.
4. Realizing our inefficiencies (adding multiple listeners that do the same thing) we could approach this by capturing a click of the parent `#gallery` and then capturing the data from the `event.target` which is likely an image
   - Close the "likely" loop by checking that the `event.currentTarget` is _not exactly the same_ (`!==`) as the `event.target`
   - Ensure we are no longer propagating up the DOM tree beyond this point
