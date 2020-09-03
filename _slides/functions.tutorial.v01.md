---
title: Functions: Definitions + Calls
description: MTEC1003 — Media Computation Skills Lab
theme: black

---
<!-- spotifytrack: spotify/episode/55gHhsasbJp2r6QZiYRjIA?si=Eke95zp2QKKcJqfY_beEZw  
spotifysername: einb0hnstrasse  -->
<!-- https://open.spotify.com/episode/55gHhsasbJp2r6QZiYRjIA?si=Eke95zp2QKKcJqfY_beEZw -->
<!-- 6rqhFgbbKwnb9MLmUQDhG6 -->

<script src='https://kit.fontawesome.com/a076d05399.js'></script>
<!-- https://www.w3schools.com/icons/fontawesome5_icons_arrows.asp -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/9.18.3/styles/night-owl.min.css" id="highlight-theme">
<script src="//cdnjs.cloudflare.com/ajax/libs/highlight.js/9.11.0/highlight.min.js"></script>
<script>hljs.initHighlightingOnLoad();</script>
<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
<!-- http://www.iangoodfellow.com/blog/jekyll/markdown/tex/2016/11/07/latex-in-markdown.html -->
<!-- http://www.vishalsinha.in/2017/04/23/highlight -code-jekyll.html -->

<!-- Theme used for syntax highlighting of code -->
<!-- <link rel="stylesheet" href="/MTEC1003-OL04-slides/public/css/monokai.css" id="highlight-theme"> -->

<!-- <link rel="stylesheet" href="lib/css/monokai.css"> -->
<!-- <script src="plugin/highlight/highlight.js"></script> -->

## In this tutorial, we'll discuss...

<span class="fragment">Function Definitions</span>

<span class="fragment">Function Calls <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

...but in _Python_, **NOT** JavaScript!...

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

...okay fine, we'll also talk  
_a little bit about JavaScript too._  
There, _ya happy?!_

So, let's get started:

----

## What is a Function?  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

<blockquote cite="https://en.wikipedia.org/wiki/Debugging">
  &ldquo;Functions are "self contained" modules of code that accomplish a specific task. Functions usually "take in" data, process it, and "return" a result.&rdquo;
</blockquote>
—[Wikipedia](https://en.wikipedia.org/wiki/Debugging){:target="_blank"}  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

It's can also be thought of as  
_a process of identifying:_  

<span class="fragment">what **variables**</span>  

<span class="fragment">hold what **values**</span>  

<span class="fragment">at what **point in time**.</span>  

<span class="fragment">—Rebecca Hill, _WeTransfer.com_<br>Debugging Specialist + JavaScript Developer</span>  

----

By now, you've had _plenty_ of opportunity  
to create **bugs** in your code...  

<span class="fragment">I mean, think of all those lovely JavaScript + Python exercises we've done! <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

But, have you _fixed_ these errors on your own?  

<img class="plain" src="https://i.pinimg.com/564x/6d/d9/e9/6dd9e95858f11330f58429aea900abfd.jpg" alt="debug-meme" width="400px" style="background:none; border:none; box-shadow:none;">

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

If so,  

### CONGRATULATIONS!!  

After all, our goal is for you to  
<span style="color: #66FF66;"><b><i>learn HOW to keep learning,</i></b></span>  
that is, to squash your own bugs...  

<span class="fragment"><img class="plain" src="{{ site.baseurl }}/io.diagrams/bug.png" alt="bug" width="100px" style="background:none; border:none; box-shadow:none;"><br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

Much of the time, however,  
**catching + solving** our own coding mistakes...  

<span class="fragment">well, it can be difficult...</span>  

<span class="fragment">and maybe we don't always figure it out...</span>  

----

### The truth about debugging is  

<span class="fragment">1. It takes time,</span>

<span class="fragment">2. resourcefulness,</span>

<span class="fragment">3. and problem-solving skills.</span>

----

### Yet Surprisingly,  
## we _rarely_ teach debugging!  

<span class="fragment"><img class="plain" src="{{ site.baseurl }}/io.diagrams/bug.png" alt="bug" width="100px" style="background:none; border:none; box-shadow:none;"><br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

There are still  
### computer science programs  

<span class="fragment">where you can spend your _entire_ degree<br>_never_ learning how to debug!</span>  

----

_How could that be, you ask??_  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

Maybe it's because   
we've always relied on the  

<span class="fragment"><b>NATURAL PROBLEM SOLVING SKILLS</b><br>of so-called "good students?"</span>  

<span class="fragment">Maybe we've even taken this for granted...? <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

Or, maybe it's because now there are
#### _a lot more_ computer languages  
to learn...  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

Or maybe it's because   

<span class="fragment">software projects today</span>  

<span class="fragment">typically use pieces of code</span>  

<span class="fragment">from these **different languages, packages, libraries, frameworks, etc.**.</span>  

<span class="fragment">all having their own documentation!<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

Developers need to be **well-prepared**  
to **interact** with these languages.  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

Imagine being asked to speak to a room full of  
_English, Spanish, French,_ and _Chinese_ speakers without  

<img class="plain" src="https://imgs.xkcd.com/comics/formal_languages.png" alt="brush" width="600px" style="background:none; border:none; box-shadow:none;">  

<span class="fragment"><b>FULLY UNDERSTANDING THE RULES</b><br>that govern those languages?! <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

You'll _probably_ make some **mistakes**, right?  

<span class="fragment">We need **tools** to **navigate** situations like that. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Plus, software _today_ serves a
**wide variety of purposes**:  

<span class="fragment">**web** development / front-end</span>  

<span class="fragment">**game** design</span>  

<span class="fragment">**app** development</span>  

<span class="fragment">endless **machine learning** initiatives</span>  

<span class="fragment">...just to name a few <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

Which means:  

<span class="fragment"><span style="color: #66FF66;"><b>efficiently debugging</b></span>  

<span class="fragment"><span style="color: #66FF66;"><b>many languages</b></span>  

<span class="fragment"><span style="color: #66FF66;"><b>at the same time</b></span>  

<span class="fragment">becomes an ever-greater challenge.</span>  

----

## How To Debug

<span class="fragment">_So, "How do I fix my broken code," you ask?_</span>  

----

Actually, you've already _debugged_ something!  

<span class="fragment">If you've been doing your labs, of course...<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

## Do you remember?  

<img class="plain" src="https://i.imgflip.com/2ifhp3.jpg" alt="brush" width="300px" style="background:none; border:none; box-shadow:none;">  

<span class="fragment">[Lab 6 / Part 2 ?](https://einbahnstrasse.github.io/Goldford-MTEC1003-OL04/labs/06/lab-06-part2-python-basics.html){:target="_blank"}</span>  

<span class="fragment">That was all about **debugging** _temperature.py_</span>  

<span class="fragment">Those were fun times, weren't they? <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

Some of the most  

### Essential Debugging Tools  

were discussed in that exercise...  

----

## Essential Debugging Tools  

<span class="fragment">1. a **print** function</span>  

<span class="fragment">2. a **type** function</span>  

<span class="fragment">3. **using comments** effectively</span>  

<span class="fragment">_Let's see these in action..._</span>

----

### 1. Our Print Functions  

_Which are?_  

<span class="fragment"><span style="color: red">`print()`</span> in Python<br>_(Duh, that's easy to remember...)_</span>  

<span class="fragment"><span style="color: red">`console.log()`</span> in JavaScript<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

### You may think  

these functions are only good  
for Day \#1 of your programming class:  

<pre><code class="javascript" data-trim data-noescape>console.log("Hello world!");</code></pre>  
<pre><code class="python" data-trim data-noescape>print("Whoa, I can print something... How useless.")</code></pre>

<span class="fragment">But, we teach them for a _good_ reason...</span>  

----

Let's say you need to quickly make a **list**  
of numbers from 1 to 20 in Python, like this:  

<pre><code class="python" data-trim data-noescape>[1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20]</code></pre>

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>  

~~

To do this, you've written a lovely _for loop:_  

<pre><code class="python" data-trim data-noescape>count = 0
myList = []

for i in range(20):
    count = count + i
    myList.append(count)
print(myList)</code></pre>

<span class="fragment">Looks good...</span>  

<span class="fragment">This should work......</span>  

<span class="fragment">_We're finished here, right?........._ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

So you run your Python script in Terminal,  
and to your surprise,  
you get:  

<pre><code class="python" data-trim data-noescape>[0, 1, 3, 6, 10, 15, 21, 28, 36, 45, 55, 66, 78, 91, 105, 120, 136, 153, 171, 190]</code></pre>

<span class="fragment">This... uh... doesn't go from 1 to 20... <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

<div style='position:relative; padding-bottom:calc(70.67% + 44px)'><iframe src='https://gfycat.com/ifr/TastyPlainIrukandjijellyfish' frameborder='0' scrolling='no' width='100%' height='90%' style='position:absolute;top:0;left:0;' allowfullscreen></iframe></div><p> <a href="https://gfycat.com/tastyplainirukandjijellyfish-happened-what-hey"></a>HEY WHA' HAPPENED?!</p>

~~

So, you go back to your _beautiful_ Python code:  

<pre><code class="python" data-trim data-noescape>count = 0
myList = []

for i in range(20):
    count = count + i
    myList.append(count)
print(myList)</code></pre>

<span class="fragment">and realize you need to see what's going on<br>_inside the loop,_ that is, _at every step..._ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

## How do you know this?  

<pre><code class="python" data-trim data-noescape>[0, 1, 3, 6, 10, 15, 21, 28, 36, 45, 55, 66, 78, 91, 105, 120, 136, 153, 171, 190]</code></pre>

<span class="fragment">Because it's not incrementing in 1s.</span>  

<span class="fragment">Also not incrementing in regular intervals, which is weird...</span>

<span class="fragment">Plus, the increment gets wider _each time_... Bizarre!<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

To see what's happening _each time,_  
### Add a Print Statement  

<pre><code class="python" data-trim data-noescape>count = 0
myList = []

for i in range(20):
    count = count + i
    myList.append(count)
    print("current i is: " + str(i) + " and count is: " + str(count))
print(myList)</code></pre>

<span class="fragment">This converts **i** and **count** into strings using `str()`</span>  

<span class="fragment">It also **concatenates** them into 1 string,<br>and passes the string to `print()`</span>  

<span class="fragment">It's **indented**, so it's _inside_ the for loop. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

Our <span style="color: red">`print()`</span> statements give us a new point of view:  

<pre><code class="bash" data-trim data-noescape>current i is: 0 and count is: 0
current i is: 1 and count is: 1
current i is: 2 and count is: 3
current i is: 3 and count is: 6
current i is: 4 and count is: 10
current i is: 5 and count is: 15
...
current i is: 19 and count is: 190
$ </code></pre>

<span class="fragment">Now it's clear that **i** indexes by 1s, but **count** is irregular.</span>  

<span class="fragment">We also see **count** increasing by the current **i** _each time._<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Once we've _"seen it this way,"_  
it occurs to us that what we need is to  

### add a constant  

at a value of 1 to the value of **count**  

<span class="fragment">and not an _expanding interval_ like **i**<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

So, we make one small change to our code:  
<pre><code class="python" data-trim data-noescape>count = count + 1</code></pre>

<span class="fragment">to ensure that **count** increments by 1s, as we intend.<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

And our Terminal output confirms it works!  

<pre><code class="bash" data-trim data-noescape>current i is: 0 and count is: 1
current i is: 1 and count is: 2
current i is: 2 and count is: 3
current i is: 3 and count is: 4
current i is: 4 and count is: 5
current i is: 5 and count is: 6
...
current i is: 19 and count is: 20
$ </code></pre>

<span class="fragment">Now **count** properly increments by 1s, from 1 to 20.</span>  

<span class="fragment">And maybe you noticed we don't need **count**<br>to do what we want _at all..._ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

The final version of our code is much cleaner:  

<pre><code class="python" data-trim data-noescape>myList = []
for i in range(1, 20):
    myList.append(1)
print(myList)</code></pre>

and our Terminal output is correct:  

<pre><code class="python" data-trim data-noescape>[1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20]</code></pre>

<span class="fragment">Turns out we only needed to _append_ our _index variable_ **i**.</span>  

----

To fix our mistake, all we needed was this  

### change in perspective  

made possible using a  

## print statement  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

Once we could _see_ the results of the loop  
at **each step**, the rest just fell into place.  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

So, next time you can't figure out  
why something isn't working...

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

## Add some print statements!  

<span class="fragment">like <span style="color: red">`print()`</span> in Python</span>  

<span class="fragment">or <span style="color: red">`console.log()`</span> in JavaScript</span>

<span class="fragment">to monitor changing variables,<br>and to reveal where things went wrong<br>at _internal levels_ of your programming.</span>  

----

### 2. Our Type Functions  

_Which are?_  

<span class="fragment"><span style="color: red">`type()`</span> in Python<br>_(Duh, that's easy to remember...)_</span>  

<span class="fragment"><span style="color: red">`typeof()`</span> in JavaScript<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

----

### What does a _Type_ Function do?

<span class="fragment">Sometimes, an error results because<br>it's unclear what _type_ of data you're working with.</span>  

<span class="fragment">Often, this happens when a **variable** holds<br>a different kind of _value_ (or _type_) that should be<br>processed by a **function** you pass your **variable** on to.<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

## Wait, _what?!_  

<iframe src="https://giphy.com/embed/5wWf7H89PisM6An8UAU" width="600px" height="271px" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

Okay. Say, for example, you have Python **variable** x  
and you want to _concatenate_ **x** inside a **print statement**:  

<pre><code class="python" data-trim data-noescape>x = 600
print("I can lift: " + x + " pounds!")</code></pre>  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

And you're expecting this output:  

<pre><code class="bash" data-trim data-noescape>I can lift: 600 pounds!</code></pre>

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

So, you run your code...  

<span class="fragment">Looks good...</span>  

<span class="fragment">This should work......</span>  

<span class="fragment">_We're finished here, right?........._ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

## Surprise!  
## ERROR IN THE CONSOLE:  

<pre><code class="bash" data-trim data-noescape>Traceback (most recent call last):
  File "/path/to/my/file.py", line 2, in &lt;module&gt;
    print("I can lift: " + x + " pounds!")
TypeError: can only concatenate str (not "int") to str</code></pre>  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~  

<div style='position:relative; padding-bottom:calc(70.67% + 44px)'><iframe src='https://gfycat.com/ifr/TastyPlainIrukandjijellyfish' frameborder='0' scrolling='no' width='100%' height='90%' style='position:absolute;top:0;left:0;' allowfullscreen></iframe></div><p> <a href="https://gfycat.com/tastyplainirukandjijellyfish-happened-what-hey"></a>HEY WHA' HAPPENED?!</p>

----

## Understanding Errors  

First rule about errors:

<span class="fragment"><b>DON'T PANIC!</b></span>  

<span class="fragment">Second rule about errors:<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

## READ YOUR ERROR MESSAGES!  

<pre><code class="bash" data-trim data-noescape>Traceback (most recent call last):
  File "/path/to/my/file.py", line 2, in &lt;module&gt;
    print("I can lift: " + x + " pounds!")
TypeError: can only concatenate str (not "int") to str</code></pre>  

<span class="fragment">Look again:<br>It tells us the problem is on line 2...<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

## Go back to your Python code  

Line 2 looks like this:  

<pre><code class="python" data-trim data-noescape>print("I can lift: " + x + " pounds!")</code></pre>  

<span class="fragment">_So, what's the problem with line 2?_<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~  

## READ YOUR ERROR MESSAGES!  

<pre><code class="bash" data-trim data-noescape>Traceback (most recent call last):
  File "/path/to/my/file.py", line 2, in &lt;module&gt;
    print("I can lift: " + x + " pounds!")
TypeError: can only concatenate str (not "int") to str</code></pre>  

<span class="fragment">Look again:<br>It also tells us line 2 has a <b>TypeError</b>...</span>  

<span class="fragment">It can't **concatenate**<br>an _integer_ ("int") to a _string_ ("str")<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

That just means we forgot  
to _convert_ variable **x** into a **string**,  
before we passed **x** to the `print()` function.  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>  

~~

But maybe, for whatever reason, it's **not obvious**  
what _type_ of data is contained in variable **x**.  

<span class="fragment">Well, we can **test x** to find out what _type_ it is...</span>  

<span class="fragment">...using <span style="color: red">`type()`</span><br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

----

## Determining the _type_  

Go back to your Python code, and **comment out** line 2:  

<pre><code class="python" data-trim data-noescape>x = 600
&num; print("I can lift: " + x + " pounds!")</code></pre>  

<span class="fragment">This way, we can make changes **without losing line 2**.</span>   

<span class="fragment">Now our program won't run line 2 since it's _commented out,_ and so it won't **throw an error**.</span>  

<span class="fragment">We can always _comment in_ line 2 again if we need it...<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

Then, **insert** a new line 2 that reads:  

<pre><code class="python" data-trim data-noescape>x = 600
print(type(x))
&num; print("I can lift: " + x + " pounds!")</code></pre>  

<span class="fragment">We use <span style="color: red">`type()`</span> to **test** the _type of value_<br>contained in variable **x**.</span>   

<span class="fragment">Then we <span style="color: red">`print()`</span> the result.</span>   

<span class="fragment">Run the code in Terminal to see the result...<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~  

<pre><code class="bash" data-trim data-noescape>&lt;class 'int'&gt;</code></pre>

<span class="fragment">This is the output of the the <span style="color: red">`type()`</span> function.</span>

<span class="fragment">It tells us that the variable **x** is an **'int'** or _integer,_<br>and not a _string_ like we need. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Now it's clear: we gave `print()` the wrong _type_  

<span class="fragment">So we got a <b>TypeError</b>...</span>  

<span class="fragment">Let's change **x**'s _type_ and see what happens...</span>  

----

## Fixing a TypeError  

Go back to your Python code.  
_Comment out_ <span style="color: red">`print(type())`</span>, then _comment in_  
your _original_ line 2 (now line 3). Make 1 small change:  

<pre><code class="python" data-trim data-noescape>print("I can lift: " + str(x) + " pounds!")</code></pre>  

<span class="fragment">We use <span style="color: red">`str()`</span> to convert **x** into a _string._<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

Now, our complete code looks like this:  

<pre><code class="python" data-trim data-noescape>x = 600
&num; print(type(x))
print("I can lift: " + str(x) + " pounds!")</code></pre>  

<span class="fragment">_Let's see what the output will be._ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

<pre><code class="bash" data-trim data-noescape>I can lift: 600 pounds!
$</code></pre>

<span class="fragment">Just as we expected! It works!</span>  

<span class="fragment">There you have it:</span>  

<span class="fragment">Fixing a **TypeError** is a piece of cake!</span>  

----

## 3. Using Comments Effectively  

<span class="fragment">Normally, we think of **comments** as a great way to **document** our work.<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

For example:  

<pre><code class="python" data-trim data-noescape>x = 600
&num; set variable x to value 600
print("I can lift: " + str(x) + " pounds!")
&num; concatenate string, then print!</code></pre>  

<span class="fragment">The comments above are **ignored by the compiler**<br>when you run your code.</span>

<span class="fragment">They're used to **remind** us what our code is doing,</span>

<span class="fragment">They can also **annotate** + **explain** complicated algorithms in "human-readable language,"</span>

<span class="fragment">so we should use them frequently for these purposes!<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

But we can also use **comments** in other ways...  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

For example, recall when we were about  
midway through our last example:  

<pre><code class="python" data-trim data-noescape>x = 600
print(typeof(x))
&num; print("I can lift: " + x + " pounds!")</code></pre>  

<span class="fragment">Here, we _commented out_ the original print statement</span>

<span class="fragment">so it wouldn't **throw an error**.</span>

<span class="fragment">We could always _comment in_ our print statement later.<br>That way, we don't lose our work.<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

But how about this version?  

<pre><code class="python" data-trim data-noescape>x = 600
&num; print("I can lift: " + x + " pounds!")
&num; print("I can lift: " + str(x) + " pounds!")</code></pre>  

<span class="fragment">Now, there are 2 lines _commented out:_</span>

<span class="fragment">2 different _versions_ of **the same** print statement.</span>

<span class="fragment">This lets us **try different solutions**<br>and **keep track** of our progress **without loosing our work**, like this...<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

### Possible solution \#1:  

<pre><code class="python" data-trim data-noescape>x = 600
print("I can lift: " + x + " pounds!")
&num; print("I can lift: " + str(x) + " pounds!")</code></pre>  
<small>_(Line 3 is ignored.)_</small>  

### Possible solution \#2:  

<pre><code class="python" data-trim data-noescape>x = 600
&num; print("I can lift: " + x + " pounds!")
print("I can lift: " + str(x) + " pounds!")</code></pre>  
<small>_(Line 2 is ignored.)_</small>  

<span class="fragment">We can freely _comment in_ and _out_ these lines<br>**without deleting** any of our work!<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

----

### So, you can use comments to:  

<span class="fragment">1. **remind yourself what your code is doing**, esp. _long after_ you wrote it (e.g. when you need it in a future class...)</span>

<span class="fragment">2. **document**, **annotate** + **explain** complicated algorithms.</span>

<span class="fragment">3. **save** + **organize** problematic lines, and</span>

<span class="fragment">4. **try multiple solutions** to the same problem,<br>without **losing your work**.</span>

----

## Single-Line Comments  

If you just need to _comment out_ 1 line at a time:  

<span class="fragment">In Python, use <span style="color: red"><b>#</b></span><br>_(pound sign, number sign, "hashtag")_</span>

<span class="fragment">In JavaScript, use <span style="color: red"><b>//</b></span><br>_(2 forward slashes)_<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

For example:  

<pre><code class="python" data-trim data-noescape>&num; I'm a single-line comment in Python!</code></pre>  
<pre><code class="javascript" data-trim data-noescape>// I'm a single-line comment in JavaScript!</code></pre>  

----

## Multi-Line Comments  

If you have _more than 1 line_ to _comment out:_  

<span class="fragment">In Python, use 3 quotes: <span style="color: red"><b>"""</b></span><br>_on lines before + after your comment._</span>

<span class="fragment">In JavaScript, use <span style="color: red"><b>/\*</b></span> _before,_<br>and <span style="color: red"><b>\*/</b></span> _after_ your comment. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

For example:  

<pre><code class="python" data-trim data-noescape>"""
I'm a multi-line
c O m M e N t
in Python!
Compilers always ignore me.
"""</code></pre>  
<pre><code class="javascript" data-trim data-noescape>/* I'm a multi-line
C o M m E n T
in JavaScript!
Compilers always ignore me.
*/</code></pre>  

----

## HTML + CSS  

We haven't learned much about these yet,  
but we will later this semester...  

<span class="fragment">These 2 languages have _one comment format_<br>for both single-line _and_ multi-line comments:<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

### In HTML:  

Use <span style="color: red"><b>\<\!\-\-</b></span> _before,_  
and <span style="color: red"><b>\-\-\></b></span> _after_ your comment.

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

For example:  

<pre><code class="html" data-trim data-noescape>&lt;&excl;-- I'm a single-line comment in HTML! --&gt;</code></pre>  

<pre><code class="html" data-trim data-noescape>&lt;&excl;--
I'm a multi-line
c O m M e N t
in HTML!
Compilers always ignore me.
--&gt;</code></pre>  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

### In CSS:  

Use <span style="color: red"><b>/\*</b></span> _before,_  
and <span style="color: red"><b>\*/</b></span> _after_ your comment.

<span class="fragment">...Just like in JavaScript! <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

For example:  

<pre><code class="css" data-trim data-noescape>/* I'm a single-line comment in CSS! */</code></pre>  

<pre><code class="css" data-trim data-noescape>/*
I'm a multi-line
c O m M e N t
in CSS!
Compilers always ignore me.
*/</code></pre>  

----

_Wow that's a lot of **differing syntax!**_  
_How do I keep track of all these comment formats?_  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

Well, the good news is...

### You don't have to remember them!!   

_In any good text editor there is usually_

### 1 keystroke to rule them all...  

----

## Toggle Single-Line Comments On-And-Off  

In your text editor, position your cursor  
anywhere on a line of code, then:  

<span class="fragment">On macOS, type <span style="color: red"><b>Command ⌘ + /</b></span></span>

<span class="fragment">On Windows, type <span style="color: red"><b>Control + /</b></span><br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Do it once to _comment out_,  

<pre><code class="javascript" data-trim data-noescape>// console.log("I'm a single-line C o M m E n T in JavaScript!"); </code></pre>  

<span class="fragment">Your text editor _adds_ the<br>proper comment characters for you!<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

do it again to _comment in._  

<pre><code class="javascript" data-trim data-noescape>console.log("I'm a single-line C o M m E n T in JavaScript!");</code></pre>  

<span class="fragment">Your text editor _removes_ the<br>proper comment characters for you!<br></span>

----

## Multi-line Comment Blocks  

Easy! Just _highlight the lines_ you need to comment,  
and use the **same keystroke** you did before!  

<span class="fragment">On macOS, type <span style="color: red"><b>Command ⌘ + /</b></span></span>

<span class="fragment">On Windows, type <span style="color: red"><b>Control + /</b></span><br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

With your multiple-lines highlighted,  

<span class="fragment">Do it once to _comment out,_</span>

<span class="fragment">do it again to _comment in._<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

## Amazing!  

You don't need to memorize anything but the keystrokes!  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

So far we've seen some of the _essentials..._  

<span class="fragment">But, there must be an **order** to all this madness, right?<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

What **steps** should I take to **debug _effectively?_**  

----

## Debugging Step \#1  

<span class="fragment">Try to <span style="color: red"><b>REPRODUCE</b></span> the bug.<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

### Ask yourself:  

<span class="fragment">Can I make this error **reappear** in some **predictable** way?</span>

<span class="fragment">Does it only happen **sometimes** or **always**?</span>

<span class="fragment">**Observe** + try to **make** the error appear _again..._<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

_By the way, this is gonna feel_  
_a little bit like detective work..._

<iframe src="https://giphy.com/embed/v1gWOJFYLapnG" width="700px" height="271px" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>  

----

## Debugging Step \#2  

<span class="fragment"><span style="color: red"><b>ISOLATE</b></span> the bug.<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Can you **narrow down** _all_ of your code  
to just **1 part** that's causing the error?  

<span class="fragment">What are some **tools** you can use to do this?<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

### How about starting with  

<span class="fragment"><span style="color: #66FF66;"><b>print statements</b></span></span>

<span class="fragment"><span style="color: #66FF66;"><b>type functions</b></span></span>

<span class="fragment"><span style="color: #66FF66;"><b>commenting in/out</b></span> different lines<br>that might be the _source_ of the problem...</span>

<span class="fragment">Also, never forget to...<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

## READ YOUR ERROR MESSAGES!  

<span class="fragment">Most of the time, your error messages already tell you:</span>

<span class="fragment"><span style="color: #66FF66;"><b>what line</b></span> the bug is on, and</span>

<span class="fragment"><span style="color: #66FF66;"><b>what kind of error</b></span> is causing it!</span>

----

## Debugging Step \#3  

<span class="fragment"><span style="color: red"><b>DON'T CHANGE TOO MUCH AT ONCE!</b></span><br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Be <span style="color: #66FF66;"><i>methodical</i></span> and <span style="color: #66FF66;"><i>systematic</i></span>  
about the changes you make  
in pursuit of a solution...  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

<span style="color: #66FF66;"><i>Break down</i></span> your plan of action  
into a series of <span style="color: #66FF66;"><i>logical steps.</i></span>  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

<span style="color: #66FF66;"><i>Document</i></span> each solution you try.

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

### Hey! Here's an idea:  

<span class="fragment">You can even think of this process like<br>one **giant** _conditional statement..._</span>

<span class="fragment"><span style="color: #66FF66;"><b>IF</b></span> my 1st idea doesn't squash the bug,</span>

<span class="fragment"><span style="color: #66FF66;"><b>THEN</b></span> try something else...</span>

<span class="fragment"><span style="color: #66FF66;"><b>ELSE IF</b></span> that doesn't work,</span>

<span class="fragment"><span style="color: #66FF66;"><b>THEN</b></span> try the next idea...</span>

<span class="fragment">_and so on..._ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

But, if you _introduce_  
<span style="color: red">too many <b>new elements</b> into your code</span>  
all at the same time...  

<iframe src="https://i.kym-cdn.com/entries/icons/original/000/012/248/wheresoda.gif" width="300px" height="200px" frameBorder="0" allowFullScreen></iframe>  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

You'll have made changes  

<span class="fragment">that _impact_ your program</span>

<span class="fragment">in _too many ways_ to keep track of,</span>

<span class="fragment">changing _multiple behaviors_<br>within your code. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Then, you'll probably get **confused**,  

<span class="fragment">and **forget** what you've already tried.</span>

<span class="fragment">And if you fix it,</span>

<span class="fragment">it will not be clear what worked!</span>

----

## Debugging Step \#4  

<span class="fragment">_If you can't figure it out at first..._</span>

<span class="fragment">Spend about <span style="color: red"><b>1 hour working on the problem,</b></span> and</span>

<span class="fragment"><span style="color: red"><b>take frequent breaks</b></span> to refresh your brain.<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

## An hour can make a difference  

Not much more,  
but not much less.

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

## Or try the [Pomodoro Method](https://medium.com/manager-mint/the-pomodoro-technique-a-productivity-guide-908c73619e9){:target="_blank"}  

<iframe src="https://miro.medium.com/max/552/1*iRmZDugBpvyLVlzC1DXSiA.png" width="500" height="300" frameBorder="0" allowFullScreen></iframe>
_If you want to be more systematic..._ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~  

Taking a break means you'll return  
_with a fresh perspective..._  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

And maybe the solution will be **instantly clear**!

----

## Debugging Step \#5  

<span class="fragment">_If you still can't figure it out..._</span>

<span class="fragment"><span style="color: red"><b>Search forums</b></span>, e.g. Stackoverflow,<br>for others who had the same problem...<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

<img class="plain" src="https://imgs.xkcd.com/comics/wisdom_of_the_ancients.png" alt="googleit" width="600px" style="background:none; border:none; box-shadow:none;">

<span class="fragment"><span style="color: red"><b>_BUT WAIT!!..._</b></span></span>

----

## <span style="color: red"><b>Don't just copy/paste!</b></span>

<span class="fragment">_Why not?! It's so easy!_</span>

<span class="fragment">Because you won't **learn anything** that way...<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

If you copy/paste code from a forum,  

<span class="fragment">You won't understand why your own code **didn't work**,</span>  

<span class="fragment">and you _also_ won't know<br>why the solution you found **does work**.<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

If you copy/paste code from a forum,  

<span class="fragment">without **fully understanding** what that code does,</span>

<span class="fragment">you're going to keep <span style="color: red"><b>repeating the same mistake!</b></span><br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

So if you find something online that helps...  

<span class="fragment">you must **study and understand** it<br>in order to **use it**.</span>

<span class="fragment">And to avoid possible disciplinary action,<br>you must also _cite someone else's code._<br>See our [syllabus blurb on plagiarism](https://einbahnstrasse.github.io/Goldford-MTEC1003-OL04/#integrity){:target="_blank"} for more info.</span>

----

## Debugging Step \#6  

<span class="fragment">_If nothing else works..._</span>

<span class="fragment"><span style="color: red"><b>Ask someone for help.</b></span></span>

<span class="fragment">But, be prepared to<br><span style="color: red"><b>show them what you've already tried.</b></span><br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Be _mindful_ of your colleague's time:  

<span class="fragment">Don't ask for too much of it.</span>

<span class="fragment">Don't expect them to _start from scratch_ for you.</span>

<span class="fragment">_Guide_ them to the source of the problem, and</span>

<span class="fragment">_show what you do understand_ about the bug!<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Treat this person as if they were a  
**senior developer** at your new job...  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

You need them to  
_believe in your ability_  
to work independently!  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

## Protips on asking for help  

<span class="fragment">Prepare _specific_ questions about the bug.<br>(not _"OMG HAAALP! I don't know what to do!"_)</span>

<span class="fragment">Share what you've _done_ + what you _understand so far._<br>Don't worry: it's a process... You're learning!</span>

<span class="fragment">Gather your questions _in advance_ so you don't keep asking.<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

But most importantly...  
Before asking _anyone_ for help,  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

Follow the previously-mentioned  

## Debugging Steps  

<span class="fragment">and <span style="color: #66FF66;"><b>challenge yourself</b></span><br>to find a solution on your own.<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

You will <span style="color: #66FF66;"><b>grow</b></span> as a coder because of it!  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

You'll <span style="color: #66FF66;"><b>remember how to<br>solve similar problems</b></span> more frequently!

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

Think of it this way:  

<span class="fragment"><span style="color: red"><i>We actually don't learn enough<br>from "pretty" examples of perfectly-working code...</i></span></span>  

<span class="fragment"><span style="color: #66FF66;"><b>We learn WAY MORE from fixing<br>our _very own_ broken code!</b></span></span>  

----

So, debugging is basically its own study,  

<span class="fragment">and these were just a few ideas to get you started.</span>

<span class="fragment">There are some powerful _debugging tools_ out there... <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

For example, our web browser _Google Chrome_  
has excellent support for debugging JavaScript...  

<iframe width="560" height="315" src="https://www.youtube.com/embed/H0XScE08hy8" frameborder="0" allowfullscreen></iframe>

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

We might explore more _advanced debugging_  
_strategies,_ such as this, on another day.  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

Meanwhile,  

<span class="fragment">the concepts discussed above<br>are _really_ the _essentials_ we need. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

So for now...  

<span class="fragment">_Happy debugging!_</span>

<span class="fragment"><img class="plain" src="{{ site.baseurl }}/io.diagrams/bug.png" alt="bug" width="100px" style="background:none; border:none; box-shadow:none;"></span>

----

## Resources

Some of the ideas in this presentation were borrowed from the following episode of the _Ladybug Podcast:_  

<!-- {% raw %} -->
<iframe src="https://open.spotify.com/embed-podcast/episode/55gHhsasbJp2r6QZiYRjIA" width="80%" height="232" frameborder="0" allowtransparency="true" allow="encrypted-media"></iframe>  
<!-- {% endraw %} -->

Listening to the whole conversation is _highly recommended!_    

----

Also, check out how this guy  
locates + solves a nasty Python bug:  

<iframe width="560" height="315" src="https://www.youtube.com/embed/K6WGRBhacq8" frameborder="0" allowfullscreen></iframe>

You don't need to understand all the code he uses.  
The concepts are more important!

----

## Finé  

<span class="fragment"><img class="plain" src="{{ site.baseurl }}/io.diagrams/bug.png" alt="bug" width="100px" style="background:none; border:none; box-shadow:none;"></span>
