#####1. Which version control systems are you familiar with?
 * Git - For version control systems
 * Github - For GUI and collaborating

#####2. If you have 5 different stylesheets, how would you best integrate them into the site?
 * Combine all stylesheets into one file

#####3. How would you optimize a website's assets/resources?
 * Name assets
 * CDN (Content Deliver Network)
 * CSS Sprites (still learning more on this)
 * Optimize images
 * Avoid in-line CSS
 * Avoid in-line JavaScript

#####4. Explain some of the pros and cons for CSS animations versus JavaScript animations.
 * CSS animations provide better performance and they are simpler while JavaScript animations are more customizable

#####5. What are data- attributes good for?
 * Data attributes are good for storing custom data private to the page or application, for which there are no other appropriate attributes or elements

#####6. Whys is it generally a good idea to position CSS ```<link>```s between ```<head></head>``` and JS ```<script>```s just before ```</body>```? Do you know any exceptions?
 * Styles are loaded before the page is rendered. Prevents users from seeing a white screen

#####7. Create a for loop that iterates up to 100 while outputting 'fizz' at multiples of 3, 'buzz' at multiples of 5, and 'fizzbuzz' at multiples of 3 and 5.
   ```javascript  
   var i = 0;

   while (i <= 100) {
     if (i%3 === 0 && i%5 === 0) {
       console.log('fizzbuzz');
     } else if (i%3 === 0 ) {
       console.log('fizz');
     } else if (i%5 === 0 ) {
       console.log('buzz');
     }
     i++;
   }
  ```

#####8. For the image below, write the CSS for the button. Also, write a click handler to change the text in the input box.
  ```HTML  
    <button>CLICK ME</button>
   ```
  ```css  
     button {
       background-color: red;
       border: 1px solid black;
       color: white;
       border-radius: 8px;
     }
  ```
======
  ```HTML
    <body>
      <input value='I am text'>
    </body>
  ```
  ```javascript
    $(document).ready(function(){
      $('input').click(function() {
        $(this).val('New text');
      })
    })
  ```

#####9. Write the HTML markup and CSS for the image below:
  ```HTML  
    <div class='wrapper'>

      <div class='inside-box-one'>
      </div>

      <div class='inside-box-two'>
      </div>

    </div>

    <div class='bottom-box'>
    </div>
  ```
  ```CSS  
    .wrapper {
       width: 100%;
       border: 1px solid black;
       text-align: center;
    }

    .inside-box-one {
       width: 40%;
       height: 150px;
       border: 1px solid black;
       margin: 25px 25px 25px 0;
       vertical-align: top;
       display: inline-block;
    }

    .inside-box-two {
       width: 40%;
       height: 450px;
       border: 1px solid black;
       margin: 25px 0 25px 25px;
       display: inline-block;
    }

    .bottom-box {
       width: 100%;
       height: 100px;
       border: 1px solid black;
       margin: 25px 0 0 0;
    }
  ```

#####10. Have you used a different templating language before?
 * Ruby/.erb

#####11. What is the difference between classes and ID's in CSS?
 * Classes (.) are used for repeated elements in a document
 * IDs (#) are used for unique elements and cannot be repeated in a document

#####12. Describe Floats and how they work.
 * Floats allow you to wrap (either left or right) text around images
 * You can manipulate other elements to do the same so that for example, two divs can be side by side

#####13. Describe the z-index.
 * Specifies the stack order of an element and only work on positioned elements (They are like layers in photoshop)

#####14. Explain CSS sprites, and how you would implement them on a page or website.
 * A CSS sprite contains many different images combined into one
 * This allows you to load parts of the image later on
 * This is significant because although the initial image sprite may be larger than the sum of the the images by themselves, once the sprite has been loaded it is much faster to access parts of it than making a bunch of new requests

#####15. How would you approach fixing browser-specific styling issues?
 * Use a CSS reference, such as [caniuse] (http://caniuse.com/), to identify if the feature I am trying to use is compatible with the browser I am having problems with
 * Fix the bug if there is one or find the closest alternative
 * Last resort should be to remove the feature because a developer should always strive for all users to share the same experience

#####16. Have you ever used a grid system, and if so, what do you prefer?
 * No, I have never used a grid system as it relates to web development
 * I have however, used them in graphic design and I understand how they benefit design in general
  * Grids Provide a template to follow throughout a project
  * They set rhythm and emphasis which guide a user as they navigate a site
  * If you know how to use a grid then you know how to break them and create more interesting designs while still having a solid foundation

#####17. Have you used or implemented media queries or mobile specific layouts/CSS?
 * Yes, I have used media queries (```@media only screen and (min-width: 960px) {}```) when working on responsive websites

#####18. What are the advantages/disadvantages of using CSS preprocessors?
 * Advantages
  * Re-usable code (mixins)
  * Faster development
 * Disadvantages
  * More levels of abstraction
  * Cannot live edit
  * Can screw up CSS easily

#####19. How would you implement a web design comp that uses non-standard fonts?
 * Make sure the font is licensed for web use
 * Convert all desired weights and styles to proper format (EOT, OTF, TTF)
 * Include them in your file
 * Add ```@font-face {}``` to stylesheet

#####20. Describe pseudo-elements and discuss what they are used for.
 * They are selectors that use ```:``` or ```::``` and are used to style specific parts of an element.
 * For example: Capitalizing the first letter in a paragraph

#####21. What does ```* { box-sizing: border-box; }``` do? What are its advantage?
 * Allows you to go change the box model from declaring the height/width of an element and then adding padding and margin to it and thus increasing it's true width but not the value width, to allowing you to declare the exact height/width of an element and subtracting from inside as you add padding, margin, and border

#####22. List as many values for the ```display``` property as you can remember.
 * ```inline```
 * ```block```
 * ```flex```
 * ```inline-block```
 * ```inherit```

#####23. What is the difference between ```inline``` and ```inline-block```?
 * ```inline```
  * Respect left and right margins, but not top and bottom
  * Cannot have a width and height set
  * Allow other elements to their left and right
 * ```inline-block```
  * Respect top & bottom margins and padding
  * Respect height and width
  * Allow other elements to their left and right
  * Only as wide as it's content

#####24. What's the difference between a relative, fixed, absolute and statically positioned element?
 * ```static```
  * The default position of all elements in an HTML document
 * ```relative```
  * It allows you to manipulate an element relative to where it traditionally appears
  * It also lets you use the z-index
 * ```fixed```
  * An element positioned relative to the browser window itself. Meaning that it's position won't change as you scroll
 * ```absolute```
  * Allows you to place an element exactly where you want it in relation to it's parent element
  * It removes the flow of the element the positioning is applied to

#####25. How is responsive different from adaptive design?
 * Responsive
  * Adjust to the size of the screen as you resize the website using CSS media queries to change styles based on the device
 * Adaptive
  * Have different styles depending on the device that is seeing the website

#####26. Explain how ```this``` works in JavaScript.
 * ```this``` refers to scope. The example below best represents how I undestand it to work. It acts similarly to ```self``` in ruby.
  ```javascript
    var contact = {
      firstname: 'Joe',
      printName: function() {
        console.log(this.firstname);
      }
    }
    var newContact = contact;
    contact.printName();
    newContact.printName();
  ```

#####27. Explain what is the difference between .call and .apply?
 * Similarities
  * They are both functions you call on other functions
  * They both execute in the scope they are called on
 * Differences
  * ```.call``` executes the other arguments that are passed on to it as they are
  * ```.apply``` expects an array

#####28. Explain AJAX in as much detail as possible.
 * Asynchronous JavaScript And XML
 * A technique that allows you to send and retrieve data in the background without refreshing a web page
 * The requests as far as a server is concerned is identical to a regular HTTP request
 * I used AJAX in my application [polyguin] (http://www.polyguin.com/)
  * When users make posts they are automatically displayed on the page when the click 'post'
  * New posts created by other users are being loaded into the page every 5 seconds without having to reload the page

#####29. What is the difference between an attribute and a property?
 * Attributes
  * Are always strings
  * They are in the HTML not in the DOM
  * You can set custom attributes
 * Properties
  * Can be boolean, strings, numbers, etc...
  * You can access them in JavaScript

#####30. Name 3 ways to decrease page load (perceived or actual time).
 * Only one stylesheet
 * Use CSS sprites
 * Minify code
 * Prefetching
 * Use the proper file formats for images (.GIFs, .JPGs, .PNGs etc...)

#####31. What is the difference between == and ===?
 * ```==``` Abstract Equality Comparison
 * ```===``` Strict Equality Operator
  ```JavaScript
    console.log(3 == '3') // true
    console.log(3 === '3') // false
  ```

#####32. Explain what a single page app is.
 * Single-Page Applications (SPAs) are web apps that load a single HTML page and dynamically update that page as the user interacts with the app
 * Either all necessary code is retrieved with a single page load or resources are being dynamically loaded as the user interacts with page
 * SPAs involve dynamic communication with the web server behind the scenes

#####33. What tools and techniques do you use debugging JavaScript code?
 * ```console.log```
 * Breakpoints
 * Firebug

#####34. Explain the difference between synchronous and asynchronous functions.
 * Synchronous functions run each task one after the other (Waterfall Metaphor)
 * Asynchronous functions can run multiple tasks at the same time without having to wait for other task to complete (Boomerang Metaphor)

#####35. What are advantages/disadvantages to testing code?
 * Advantages
  * Find bugs earlier
  * Better simple, elegant code (refactored)
  * Test serve as documentation
  * Easier to maintain
 * Disadvantages  
  * Time and effort up-front
  * Takes effort to maintain

#####36. What tool's would you use to test your code's functionality?
 * Develop tests using Jasmine/Mocha

#####37. What tools would you use to find a performance bug in your code?
 * Good test cases
 * Have good data to test
 * Try different test environments

#####38. Do your best to describe the process from the time you type in a website's URL to it finishing loading on your screen.
 1. Type URL in the browser
 2. The browser looks up the IP address for the domain name
 3. Broswer sends an HTTP request to the web server
 4. The server redirects
 5. The browser follows the re-direct
 6. The server sends back a HTML response
 7. The browser begins loading the HTML requesting different links, assets etc... as it renders
