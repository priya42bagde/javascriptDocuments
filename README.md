# Learning documents for Javascript
For book download:- https://goalkicker.com/ <br/>
Udemy by colt Steele- JS DSA <br/>
https://learnersbucket.com/ <br/>
Namaste Javascript<br/>
Reactjs crash course- https://www.youtube.com/watch?v=w7ejDZ8SWv8 <br/>
Learning: https://www.youtube.com/c/CodingAddict/videos <br/>
https://developer.mozilla.org/en-US/docs/Web/JavaScript <br/>
https://javascript.info/<br/>

# Machine coding round tasks
Nested comments (hard) <br/>
Calendar App (hard) <br/>
Toast (easy) <br/>
Model <br/>
Tic tac toe implementation <br/>
JSCafe-To Do App <br/>
create a function to clearAllTimeouts <br/>
Microsoft Task <br/>
DOM Challenge: https://github.com/devkodeio/the-dom-challenge <br/>
Binary Search https://www.geeksforgeeks.org/binary-search/ <br/>
writing the Promise.all()<br/>
DSA question: Brackets pair-matching matching problem.<br/>
JavaScript Problem Solving: Flatten Array problem.<br/>
HTML, CSS question: It was a simple UI question, where I have to build 3 circles circumcised inside one other UI<br/>
System Design<br/>
tree traversal in various orders, stack, etc<br/>
Implement throttle and debounce without using setTimeout <br/>
Currying: https://jsfiddle.net/sagargiri8846/pkb0oyzd/90/ <br/>
How will you center a div in #css (both horizontally and vertically) <br/>

# Theory questions
What are interceptors? <br/>
React Fiber <br/>
Virtual DOM https://stackoverflow.com/questions/21965738/what-is-virtual-dom <br/>
https://www.educative.io/edpresso/what-is-an-event-loop-in-javascript<br/>
What is pipe and compose in js and its polyfill for compose: https://www.freecodecamp.org/news/pipe-and-compose-in-javascript-5b04004ac937/<br/>
https://developers.google.com/web/fundamentals/performance/critical-rendering-path<br/>
https://github.com/priya42bagde/javascript-interview-questions-2 <br/>
https://github.com/priya42bagde/javascript-questions <br/>
https://dev.to/ruppysuppy/redux-vs-context-api-when-to-use-them-4k3p <br/>
https://git-scm.com/docs/gittutorial <br/>
https://developer.mozilla.org/en-US/docs/Learn/Performance/What_is_web_performance <br/>
https://www.freecodecamp.org/news/what-exactly-is-client-side-rendering-and-hows-it-different-from-server-side-rendering-bd5c786b340d/<br/>
Currying: https://jsfiddle.net/sagargiri8846/pkb0oyzd/90/ <br/>
https://github.com/priya42bagde/javascript-interview-questions-2 <br/>
What is Browser Object model: The Browser Object Model (BOM) is a browser-specific convention referring to all the objects exposed by the web browser
Some of the examples of BOM objects are
document
location
history
navigator
screen 
<hr/>
What is prop-drilling?
Prop drilling refers to the process of sending props from a higher-level parent component to a lower-level child component.

Disadvantages:-
:- You need to refactor a lot when you change the structure of data passed
Eg:- {name:"Sagar Giri"}=> {fName:"Sagar", lName:"Giri"}.
Changing the data sent from first to second will make you refactor a lot.
:- Deleting a component will make you to change all the parent component's code increasing your work

How to rectify this issue
To rectify this we can use the state management applications like Redux and Context API.
The concept in state management application is that you have a global source of truth and all data will be directly called from it without passing it via props.
<hr/>
What is the difference between onload event and DOMContentLoaded event.

The DOMContentLoaded event is fired when the document has been completely loaded and parsed, without waiting for stylesheets, images, and subframes to finish loading and the load event is fired when the DOM, CSSOM and all other resources are loaded (can be used to detect a fully-loaded page).
<hr/>
DomContentLoad vs Onload?
The DOMContentLoaded event is fired when the document has been completely loaded and parsed, without waiting for stylesheets, images, and subframes to finish loading and the load event is fired when the DOM, CSSOM and all other resources are loaded (can be used to detect a fully-loaded page).
<hr/>
 What is Shadow Dom?
 https://developer.mozilla.org/en-US/docs/Web/Web_Components/Using_shadow_DOM

<hr/>
Why to put #javascript script tag in the bottom of HTML page?
This is a really basic rule, and one that should be super easy to follow most of the time, but why does it matter?
Put very shortly:
CSS blocks rendering, so you need to deal with it right away (i.e. at the top of the document, in your <head>).

JS blocks downloads, so you need to deal with these last to ensure that they don’t hold up anything else on the page.

CSS blocks rendering because of a browsers desire to render pages progressively; they want to render things as they get to them, and in order.

If styles are a long way down the page the browser can’t render that CSS until it gets to it. This is so that the browser can avoid redraws of styles if they alter something that was previously rendered further up the document. A browser won’t render a page until it has all the available style information, and if you put that style information at the bottom of the document you’re making the browser wait, blocking rendering.

So, you put your CSS at the top of the page so that the browser can start rendering right away.

JavaScript blocks downloads for a number of reasons (this is the browser being clever again) but firstly, we need to know how downloading assets in browsers actually happens; simply put, a browser will download as many assets as it can from a single domain in parallel. The more domains it is pulling from, the more assets can be downloaded, in parallel, at once.

JavaScript interrupts this process, blocking parallel downloads from any and all domains, because:

The script being called might alter the page, meaning the browser will have to deal with that before it can move on to anything else. In order for it to deal with that eventuality it stops downloading anything else in order to focus solely on that.
Scripts usually need to be loaded in a certain order for them to work, for example, loading jQuery before you load a plugin. Browsers block parallel downloads with JavaScript so that it doesn’t start downloading jQuery and your plugin at the same time; it should be pretty obvious that if you were to start downloading both in parallel, your plugin would arrive before jQuery would.

So, because browsers stop all other downloads whilst JavaScript is being fetched, it is usually a good idea to put your JavaScript as late in the document as possible. I’m sure you’ve all seen blank sections of pages where a third party piece of JS is taking ages to load and blocking the fetching and rendering of the rest of the page’s assets; this is JavaScript’s blocking in action.
<hr/>
How react works under the hood?
  
<hr/>
What is client side rendering and how is it different from server side rendering?
Client-side rendering allows developers to make their websites entirely rendered in the browser with JavaScript. Instead of having a different HTML page per route, a client-side rendered website creates each route dynamically directly in the browser. This approach spread once JS frameworks made it easy to take.

Server-side rendering allows developers to pre-populate a web page with custom user data directly on the server. It is generally faster to make all the requests within a server than making extra browser-to-server round-trips for them. This is what developers used to do before client-side rendering.

What is the difference between client-side and server-side rendering?

Client-side rendering manages the routing dynamically without refreshing the page every time a user requests a different route. But server-side rendering is able to display a fully populated page on the first load for any route of the website, whereas client-side rendering displays a blank page first.

Server-side pros:
Search engines can crawl the site for better SEO.
The initial page load is faster.
Great for static sites.

Server-side cons:
Frequent server requests.
An overall slow page rendering.
Full page reloads.
Non-rich site interactions.

Client-side pros:
Rich site interactions
Fast website rendering after the initial load.
Great for web applications.
Robust selection of JavaScript libraries.

Client-side cons:
Low SEO if not implemented correctly.
Initial load might require more time.
In most cases, requires an external library.
<hr/>
  
What is the difference between null and undefined in #javascript?
Lets find out

null:
It means empty or a value which never existed and means nothing.
type: null is an object.
console. log(typeof null) // object
Code:
let a=null
console. log(a) //null

undefined:
It means a variable is defined but its value is never initialized.
type: undefined is of type undefined.
console. log(typeof undefined) // undefined
Code:
let a
console. log(a) // undefined

When to use null object?
When you have declared an object and want it to be empty initialise it with null.

Can we assign undefined to variable?
You can assign undefined to any variable but generally its not recommended. If you want to explicitly make any object not available use null instead . Javascript has provided null keyword for the same purpose. Undefined is assigned by javascript when you forget to initialise.
So the summary is undefined is #javascript way of saying that you forgot to initialize something or it is not existent (assigned by js) and null is user way of saying that I have initialized and want the variable to be non existent (assigned by user).
<hr/>
  
What is useRef hook in react and how is it different from useState?

The ref in useRef is a generic container whose current property is mutable and can change accordingly and hold any value.

What is difference between refs and state while storing data.

The answer is we can store data in both but storing data in refs wont rerender the component when it changes but the case is not the same with states.

When to use Refs?
We can use refs when we dont want the data to rerender when it changes.
eg: When we want to implement a timer which is not needed in the UI but is tracked internally.

When to use states?
When you want the data to rerender on every change.
Eg: A timer which you need to display on UI.
  
<hr/>
How browsers work?
https://developer.mozilla.org/en-US/docs/Web/Performance/How_browsers_work
  
<hr/>
 Positioning in css along with flex box to style components along with hands on coding.
 https://developer.mozilla.org/en-US/docs/Web/CSS/position <br/>
 https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox <br/>
<hr/>
 Javascript ProtoType: https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Object_prototypes
<hr/>  
How to optimise image loading in a website and improve performance?

Images and multimedia files are the most important component of any website. The images have to be of good quality and good quality images are generally heavy which consumes a lot of bandwidth of the client while downloading. Optimising this bandwidth may result in a significant increase in a website load time.
Also having a website which loads items slowly may kill your SEO score and your site may rank down in google search.

But how can we optimise it is a question.
Lets see....
1 :
Choose the correct image format
PNG: Higher quality and high size images, big size, lossless compression (can be lossy as well), can be used for transparent bg.
JPEG: Good quality and can use lossless (can be lossy as well). Use it for images with many colors. Small file size.
GIF: use only 256 colours and uses lossless compression . Best for animated images.

There are other formats as well which are good but some or the other browsers dont support them or are not universally acceptable.
Good comparison for types: https://lnkd.in/ga6TrZTd

Lossy compression:- Filter which eliminates some of the data and may reduce the quality of image. You have to be careful how much compression you do so it does not degrade the quality of images you serve on website.File size is greatly reduced.

Lossless compression:- Removes the metadata of images and compress the image(which can be restored later). Doesn't degrade the quality of images but also size is also not reduced that much.

Source :
https://lnkd.in/gzAAfYjh
https://lnkd.in/g5PvSCQ5

2:
Optimise Dimensions:
Optimising dimensions can be of great help. Lets say an image of 800px * 600px is being displayed in desktop site and the same image is being shown in msite as well. Whats the issue here?
The mobile device is small and doesnt need this much big file to display. The image dimension can be optimised and served as per the need by which device it is being opened upon. High dimension site can show larger dimension image and same for small dimension devices.

3:
Using CDN:
A content delivery network, or CDN, is a geographically diverse network of servers that helps speed up page load time by reducing the distance between the website visitor and the server.

4:
Optimize meta data:
Rename your images to what they are: Good for SEO
Include Alt tag and use responsive images: Good for SEO
Source :https://lnkd.in/gmApthC5

5:
Lazy loading and blur loading
Implement lazy loading within your code for faster loading of images.
<hr/>  
