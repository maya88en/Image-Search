## Image Search App using React, Bootstrap, Vite

# npm run dev

https://github.com/user-attachments/assets/c5ebfc50-c171-4384-9eb4-2d567d67d988

# Add Search Input
The title of Image search is displayed inside a container class, which is a Bootstrap class, to add some margin to the left and right of the page.
Then a form is added with a type of search.

# Store Value
Now, store the value entered by the user somewhere in the component. As there is only one input field on the page, use the useRef hook instead of the useState hook.
Using the useRef hook does not re-render the component when its value changes, which is good for performance improvement. 
On the other hand, changing state re-renders the component, so all of the child components will also re-render.

## Inside the App.jsx file, declare the useRef hook as shown below:

const searchInput = useRef(null);

## Add import for useRef hook at the top of the file:

import React, { useRef } from 'react';

## Add a ref prop for the search input, like this:

<Form.Control
   type='search'
   placeholder='Type something to search...'
   className='search-input'
   ref={searchInput}
/>

# Handle the Form Submit Action
When we enter any search term in the search box and press the enter key, we want to add the search functionality.
To do so, add an onSubmit handler to the Form tag and create a handleSearch method. And assign it to the onSubmit prop.


# Reference: 
https://www.freecodecamp.org/news/how-to-build-an-image-search-app-using-react/

