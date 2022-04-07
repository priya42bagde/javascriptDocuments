# Learning documents for Javascript
For book download:- https://goalkicker.com/ <br/>
Udemy by colt Steele- JS DSA <br/>
https://learnersbucket.com/ <br/>

# Machine coding round tasks
Tic tac toe implementation <br/>
JSCafe-To Do App <br/>
create a function to clearAllTimeouts <br/>

# Theory questions
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
