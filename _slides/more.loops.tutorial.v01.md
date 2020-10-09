---
title: More ("MOAR!") Kinds of Loops
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

<span class="fragment">While Loops</span>

<span class="fragment">Self-Similarity</span>

<span class="fragment">Recursion <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

...and we'll be doing so in both  
_Python_ **AND** _JavaScript._  

So, let's get started:  

----

## For Loop: Reconsidered    

<span class="fragment">So far we’ve learned about the **for loop.**</span>

<span class="fragment">Its basic structure fulfills many of our programming tasks: <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

...For example, **step-by-step, repetitive tasks**  
that may require things like:  

<span class="fragment">**counting**</span>

<span class="fragment">**iterating**</span>

<span class="fragment">**generating**</span>

----

But it’s important to remember...  

<span class="fragment">There are other structures available to us,</span>

<span class="fragment">for tasks _other than_ iterating, counting, etc.</span>

----

Imagine:  
You have a repetitive task...

<span class="fragment">But you don't know in advance how many times to repeat it. <br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

_Can we use a **for loop** to accomplish this?_  

----

Recall the basic structure of a **for loop**, in JavaScript:  

<pre><code class="javascript" data-trim data-noescape>for (i = 1; i <= 10; i = i + 1) {
    first statement;
    second statement;
}</code></pre>

<span class="fragment">What are its 3 components? <br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

#### The 3 Components of a For Loop:  

<span class="fragment">**1. initialization**</span>  

<span class="fragment">**2. termination condition**</span>  

<span class="fragment">**3. increment** <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

And how do we code each of these (i.e. in JavaScript)?

<span class="fragment">1. initialization: <br>`i = 1;` </span>  

<span class="fragment">2. termination condition: <br>`i <= 10;` </span>  

<span class="fragment">3. increment: <br>`i = i + 1` </span>

----  

In this case, the termination condition is **definite**:  

<span class="fragment">`i <= 10;` </span>  

<span class="fragment">It tells us: after a _**known** number of iterations,_</span>

<span class="fragment">the loop will stop. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

But what if the number of iterations  
is _not fixed in advance of the loop?_  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

For example,  

<span class="fragment">what if the number of iterations</span>  

<span class="fragment">depends on _what the user does_ each time?<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

Well, in that case...  

<span class="fragment">We need another kind of loop structure.</span>  

----

Allow me to introduce the...

<h2><span class="fragment">While Loop</span></h2>  

----

The **while loop** is also _iterative_.  

<span class="fragment">So, _like_ the **for loop**,<br>we can use both to count and repeat stuff.<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

But, _unlike_ **for loops**...  

<span class="fragment">the **while loop** only repeats itself<br><span style="color: #66FF66;"><b><i>while</i> a certain condition is <i>true</i>.<br></b></span> <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

Here's a flowchart describing how, logically,  
a **while loop** functions:  

<img class="plain" src="https://cdn.programiz.com/sites/tutorial2program/files/whileLoopFlowchart.jpg" alt="while-loop-flowchart" width="250px" style="background:none; border:none; box-shadow:none;">  
[view source](https://www.programiz.com/python-programming/while-loop){:target="_blank"}

~~

Think of it this way:  

<span class="fragment">A **while loop** acts like the **combination**<br>of a _for loop_ and a _conditional statement._</span>

<span class="fragment">As long as some condition continues to be true,<br>the loop keeps repeating... <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

But as soon as that condition is no longer true,

<span class="fragment">that is, when the condition becomes <span style="color: red">**false**,</span></span>

<span class="fragment">the loop immediately <span style="color: red">**stops repeating;**</span></span>

<span class="fragment">and our program <span style="color: red">_"exits the loop."_</span> <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

## Wait, _what?!_  

<iframe src="https://giphy.com/embed/5wWf7H89PisM6An8UAU" width="600px" height="271px" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>

<span class="fragment">Yeah, yeah, I know, you're only five, got it...</span>

<span class="fragment">How about a fancy, shmancy example then?</span>

----

For example, consider this simple,  
amazingly stupid **while loop** in Python:  

<pre><code class="python" data-trim data-noescape>i = 1
limit = 10

while i <= limit:
    print(i)
    i = i + 1

# After the loop terminates, print this:  
print("i is now greater than ", limit)</code></pre>

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

As you can imagine,  
this **while loop** produces the following output:  

<pre><code class="console" data-trim data-noescape>$ python3 /path/to/my/while-loop-script.py
1
2
3
4
5
6
7
8
9
10
i is now greater than 10
$</code></pre>

~~

<pre><code class="python" data-trim data-noescape>i = 1
limit = 10

while i <= limit:
    print(i)
    i = i + 1

# After the loop terminates, print this:  
print("i is now greater than ", limit)</code></pre>

<span class="fragment">_Can you identify the **3 components** of this loop?_ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

## While Loop: Initialization

<pre><code class="python" data-trim data-noescape># Intitialization:
i = 1
limit = 10</code></pre>

<span class="fragment">At the top, we _declare_ + _initialize_ 2 variables:</span>

<span class="fragment">the <span style="color: #66FF66;">`i`</span> variable _indexes_ our loop, as normal,</span>

<span class="fragment">but we also make a <span style="color: red;">`limit`</span> variable...</span>

<span class="fragment">Once this **counter value** has been reached (i.e. 10),<br><span style="color: red;">_the loop will stop._</span> <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

## While Loop: Increment  

Inside the **while loop** itself:  

<pre><code class="python" data-trim data-noescape>while i <= limit:
    print(i)
    i = i + 1</code></pre>

We find our usual _incremental expression_:  

<pre><code class="python" data-trim data-noescape>i = i + 1</code></pre>

<span class="fragment">Notice that it's _inside_ the loop (i.e. _indented_ in Python),</span>

<span class="fragment">meaning it increments _each time_ the loop runs. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Anything missing?

<span class="fragment">We found the <span style="color: #66FF66;">**initial**</span> and <span style="color: #66FF66;">**incremental**</span> parts...<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

But where is our <span style="color: red;">**termination condition??**</span>

<iframe src="{{ site.baseurl }}/public/confused.travolta.transparent.gif" width="600px" height="600px" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>

~~

## While Loop: Termination  

Check out the **while loop** once again:  

<pre><code class="python" data-trim data-noescape>while i <= limit:
    print(i)
    i = i + 1</code></pre>

Its first line  

<pre><code class="python" data-trim data-noescape>while i <= limit:</code></pre>

includes its own **termination condition**...  

<span class="fragment">This says to us: _Once_ <span style="color: #66FF66;">`i`</span> _is greater than_ <span style="color: red;">`limit`</span>_, stop._</span>

----

In other words,  

<span class="fragment">like <span style="color: tomato;">`if`</span> and <span style="color: tomato;">`then`</span> clauses,</span>

<span class="fragment">the <span style="color: tomato;">`while`</span> clause includes a **condition**. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

As long as that **condition** continues to be _true_,  

<span class="fragment">the loop will continue repeating itself.</span>

----

What would this simple **while loop** look like  

<span class="fragment">in JavaScript? <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

### Simple While Loop: JavaScript Version  

<pre><code class="javascript" data-trim data-noescape>var i = 1;
var limit = 10;

while (i <= limit) {
  console.log(i);
  i = i + 1;
}

// After the loop terminates, print this:  
console.log("i is now greater than " + limit);</code></pre>

<span class="fragment">_And what are the differences between this syntax<br>and the earlier Python version?_ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

#### Key Differences Compared to Python  

<span class="fragment">Declare all variables with <span style="color: tomato;">`var`</span></span>

<span class="fragment">Lines end with a semicolon <span style="color: tomato;">`;`</span></span>

<span class="fragment">While clause is in parens <span style="color: tomato;">`(i <= limit)`</span></span>

<span class="fragment">Entire **while loop** is enclosed in braces <span style="color: tomato;">`{}`</span></span>

----

Now, maybe you noticed...

<span class="fragment">that this simple **while loop**<br>had a fixed number of iterations (10).<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

What about that situation I mentioned earlier?  

<span class="fragment">_Imagine:<br>You have a repetitive task..._</span>

<span class="fragment">_But you don't know in advance how many times to repeat it._ <br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Well, we can use a **while loop** for this too...  

----

Consider this **while loop** (in Python):  

<pre><code class="python" data-trim data-noescape>userstring = input("Is MTEC1003 the best class? (y/n) ")

while userstring != "y":
    userstring = input("Sorry, I don't understand... Is MTEC1003 the best class? (y/n) ")

print("That's exactly what I was thinking...")
print("I agree! MTEC1003 really IS the best class!")</code></pre>
<small>_(Scroll to the RIGHT to see the complete line...)_</small>

<span class="fragment">_What is going on here?!_ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

First of all...

<span class="fragment">What does the <span style="color: tomato;"><b>!=</b></span> operator do?</span>

<span class="fragment">_...Remember?_</span>

<span class="fragment">It means _"not equal."_ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

So the first line of this **while loop**:  

<pre><code class="python" data-trim data-noescape>while userstring != "y":</code></pre>

<span class="fragment">which designates a **condition**,</span>

<span class="fragment">tells us that the loop will keep repeating<br>for as long as <span style="color: tomato;">`userstring`</span> is not "y".<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Now, look at the whole thing once again:  

<pre><code class="python" data-trim data-noescape>userstring = input("Is MTEC1003 the best class? (y/n) ")

while userstring != "y":
    userstring = input("Sorry, I don't understand... Is MTEC1003 the best class? (y/n) ")

print("That's exactly what I was thinking...")
print("I agree! MTEC1003 really IS the best class!")</code></pre>
<small>_(Scroll to the RIGHT to see the complete line...)_</small>

<span class="fragment">On line 1, we prompt the user for input.</span>

<span class="fragment">Inside the **while loop** we <span style="color: tomato;">_keep prompting the user_</span><br>if their answer isn't "correct,"</span>

<span class="fragment">And once it's "correct," the loop _terminates_,<br>and we print some final messages. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

So, as you can imagine, this **while loop**  
_can produce_ the following output:  

<pre><code class="console" data-trim data-noescape>$ <span style="color: tomato;">python3 /path/to/my/while-loop-script.py</span>
Is MTEC1003 the best class? (y/n) <span style="color: tomato;">n</span>
Sorry, I don't understand... Is MTEC1003 the best class? (y/n) <span style="color: tomato;">n</span>
Sorry, I don't understand... Is MTEC1003 the best class? (y/n) <span style="color: tomato;">but i like my other classes...</span>
Sorry, I don't understand... Is MTEC1003 the best class? (y/n) <span style="color: tomato;">OK I RLY HATE THIS CLASS</span>
Sorry, I don't understand... Is MTEC1003 the best class? (y/n) <span style="color: tomato;">fine, ok you win</span>
Sorry, I don't understand... Is MTEC1003 the best class? (y/n) <span style="color: tomato;">y</span>
That's exactly what I was thinking...
I agree! MTEC1003 really IS the best class!
$</code></pre>
<small>_(Scroll to the RIGHT to see the complete line, <span style="color: tomato;">including user input</span>...)_</small>

<span class="fragment">Why _"can produce"_ and not _"definitely will produce?"_ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Because the precise output of this **while loop**  
_entirely depends on what the user does._  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

The loop will keep cycling _whenever_  
the user answers something other than "y".

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

In other words,  

<span class="fragment">the exact number of iterations</span>

<span class="fragment">_is not fixed in advance._</span>

----

So, what would this **intermediate while loop** look like  

<span class="fragment">in JavaScript? <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

### Intermediate While Loop:<br>JavaScript Version  

<pre><code class="javascript" data-trim data-noescape>var userstring = prompt("Is MTEC1003 the best class? (y/n) ");

while (userstring != "y") {
  userstring = prompt("Sorry, I don't understand... Is MTEC1003 the best class? (y/n) ");
}

console.log("That's exactly what I was thinking...");
console.log("I agree! MTEC1003 really IS the best class!");</code></pre>
<small>_(Scroll to the RIGHT to see the complete line...)_</small>

<span class="fragment">_Again, what are the differences between this syntax<br>and the earlier Python version?_ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

#### Key Differences Compared to Python  

<span class="fragment">Declare all variables with <span style="color: tomato;">`var`</span></span>

<span class="fragment">Lines end with a semicolon <span style="color: tomato;">`;`</span></span>

<span class="fragment">While clause is in parens <span style="color: tomato;">`(userstring != "y")`</span></span>

<span class="fragment">Entire **while loop** is enclosed in braces <span style="color: tomato;">`{}`</span></span>

----

_But, when should I use a **for loop**?_  

<span class="fragment">_And when should I use a **while loop**?_  </span>

----

### For Loop vs. While Loop  

<span class="fragment">**For loops** repeat a _certain number of times._</span>

<span class="fragment">Use a **for loop** for simple counting, indexing, generating, reading through the items in a list, etc.</span>

----

### For Loop vs. While Loop  

<span class="fragment">**While loops** can easily repeat an _UNcertain number of times;_</span>

<span class="fragment">that is, _until_ a certain condition is no longer true.</span>

<span class="fragment">Use a **while loop** for _more complex_ iterations;<br>for example, when the number of repetitions depends<br>on a user's interaction with your program.</span>

----

So far we've discussed:

<span class="fragment"><span style="color: tomato;">for loops</span></span>

<span class="fragment">and <span style="color: tomato;">while loops</span></span>

----

Both of these types of loops  
have been used to accomplish  
what we've called <span style="color: tomato;">iteration.</span>

<span class="fragment">_Which is?_</span>

<span class="fragment">_Remember?..._</span>


----

### Iteration

<span class="fragment">To _iterate_ is to execute a sequence of instructions<br>that is <span style="color: tomato;">_continually repeated._</span> [\[view source\]](https://computersciencewiki.org/index.php/Iteration){:target="_blank"}<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

We might use an _iterative approach_  
to a problem requiring us to _iterate_:  

<span class="fragment">a precise <span style="color: tomato;">number of times,</span> or</span>

<span class="fragment">_until_ some <span style="color: tomato;">condition is _no longer_ true</span>, or</span>

<span class="fragment">through the <span style="color: tomato;">elements in a list,</span><br>_until_ the entire list has been traversed.</span>

----

But there's a special kind of "loop" we can use  

<span class="fragment">for processes that are <span style="color: tomato;">_not quite the same_</span> on each repetition,</span>

<span class="fragment">but when each repeated step is <span style="color: tomato;">_similar_</span>...</span>

<span class="fragment">that is, when each repetition is <span style="color: tomato;">_related_</span><br>in some way to the <span style="color: tomato;">_whole._</span></span>

----

## Wait, _what?!_  

<iframe src="https://giphy.com/embed/5wWf7H89PisM6An8UAU" width="600px" height="271px" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>

<h3><span class="fragment">What are you even talking about?!</span></h3>

<span class="fragment">Ugh, I know, okay, let me break this down...</span>

<span class="fragment">How about another fancy, shmancy example?!</span>

----

For example, this _entire structure_ consists  
of continual <span style="color: tomato;">variations of the same shape:</span>    

<iframe src="https://www.youtube.com/embed/-U52N6gq2Zc" width="560" height="315" frameborder="0"></iframe>

<span class="fragment">It's called a [_Sierpiński Triangle..._](https://tinyurl.com/y2z47yw8){:target="_blank"} <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

And is constructed by taking a single triangle...  

<img style="-webkit-user-select: none;margin: auto;cursor: zoom-in;" src="https://upload.wikimedia.org/wikipedia/commons/7/74/Animated_construction_of_Sierpinski_Triangle.gif" width="380" height="392">

<span class="fragment">and continually _subdividing it_ into a<br>potentially _infinite_ number of smaller triangles.</span>

----

Imagine a loop... Each time that loop repeats itself,  

<iframe src="{{ site.baseurl }}/public/sierpinski.v02.png" width="720px" height="118px" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>

<span class="fragment">big triangles are <span style="color: tomato;">_subdivided_</span> into smaller triangles.</span>

<span class="fragment">Each cycle through the loop generates results that are<br><span style="color: tomato;">_not identical_</span>, but curiously <span style="color: tomato;">_similar_</span>: <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Each time produces <span style="color: #66FF66;">_multiples of smaller triangles._</span>

----

This is a _property_ known as  

<h3><span class="fragment">Self-Similarity</span></h3>

<span class="fragment">meaning...</span>

<span class="fragment">[_the WHOLE has approximately the same shape<br>as its internal, component PARTS._](https://en.wikipedia.org/wiki/Self-similarity#:~:text=In%20mathematics%2C%20a%20self%2Dsimilar,statistical%20properties%20at%20many%20scales.){:target="_blank"} <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

In the case of the [_Sierpiński Triangle,_](https://tinyurl.com/y2z47yw8){:target="_blank"}  

<iframe src="{{ site.baseurl }}/public/sierpinski.v02.png" width="720px" height="118px" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>

<span class="fragment">all _smaller_ triangles, and their spatial arrangements,</span>

<span class="fragment">bear resemblance to all the _larger_ levels of triangles,</span>

<span class="fragment">and vise versa!</span>

----

#### So, why is self-similarity important?

<span class="fragment">It turns out that nature is full of things<br>that display this characteristic property...<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Like trees...

<iframe src="{{ site.baseurl }}/public/trees.v01.gif" width="400px" height="292px" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>

[view source](https://www.reddit.com/r/woahdude/comments/1230hb/animated_fractal_tree_gif/){:target="_blank"}  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

Or coastlines...

<iframe src="{{ site.baseurl }}/public/egypt3.jpg" width="540px" height="333px" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>

[Location: Egypt. Source: _Google Earth_](http://paulbourke.net/fractals/googleearth/egypt2.jpg){:target="_blank"}  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

Or models of _population growth..._  

<img class="animated-gif" src="https://upload.wikimedia.org/wikipedia/commons/6/63/Logistic_Map_Animation.gif" width="600px" height="auto">

<!-- <iframe src="{{ site.baseurl }}/public/Logistic_Map_Animation.gif" width="540px" height="333px" frameBorder="0" class="giphy-embed" allowFullScreen></iframe> -->

[view source](https://en.wikipedia.org/wiki/Logistic_map){:target="_blank"}  

----

So, it's worth understanding  

<span class="fragment">_how self-similar structures work,_</span>

<span class="fragment">_and how to "simulate" them in our programs._<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Now, back to programming stuff...

----

Remember: I mentioned a _special kind of loop_...

<span class="fragment">that is, for programming <span style="color: tomato;">_repeating sequences_</span></span>

<span class="fragment">where each step generates results that are <span style="color: tomato;">_similar_</span>,</span>

<span class="fragment">but <span style="color: tomato;">_not identical_</span>...</span>

<span class="fragment">each step <span style="color: tomato;">_relating to the whole..._</span></span>

----

We call this process...

<h2><span class="fragment">Recursion</span></h2>   

<span class="fragment">and we invoke _Recursion_ by creating</span>

<h2><span class="fragment">Recursive Functions</span></h2>  

----

Notice we aren't calling them _"Recursive Loops"..._  

<span class="fragment">Although **recursive functions** definitely<br>_repeat_ sequences in a very _"loop-like"_ way...<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Instead, we define _"Recursive Functions"_  

<span class="fragment">as functions with a very _"loop-like"_ behavior...<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Now, one way to <span style="color: tomato;">**incorrectly**</span> do this  
would be to _embed_ a **for loop** _within_ a function:

<pre><code class="python" data-trim data-noescape>def foo():
  for x in range(0, 5):
    print(x)</code></pre>

<span class="fragment">This is _close_ to what we mean by<br>_a function with "loop-like" behavior,_</span>

<span class="fragment">but this <span style="color: tomato;">_still isn't recursion..._</span></span>

----

## Recursive Functions

<span class="fragment"><span style="color: #66FF66;">_are functions that **call themselves**._</span></span>

<span class="fragment">That means, within a function **definition**,<br>we also **call** the function being defined.</span>

<span class="fragment">By **calling** the function within its own definition,<br>we also create a _"loop-like"_ structure...</span>

<span class="fragment">To understand better,<br>let's revisit function **definitions** and **calls**...</span>

----

### Function Definition  

<pre><code class="python" data-trim data-noescape>def foo():
  [statement 1]
  [statement 2]
  return someResult</code></pre>

<span class="fragment">In Python, we _**define**_ a function like this, remember?</span>

----

### Function Call  

<pre><code class="python" data-trim data-noescape>foo()</code></pre>

<span class="fragment">Then we _**call**_ that function somewhere else in our program.</span>

<span class="fragment">You know... to _execute_ or to _"use"_ that function.</span>

----

## But, A Recursive Function

<pre><code class="python" data-trim data-noescape>def foo():
  foo()</code></pre>

<span class="fragment"><span style="color: #66FF66;">_is a function that **calls itself**._</span></span>

<span class="fragment">Notice this function **definition** _contains_ its very own **call**.</span>

<span class="fragment"><span style="color: #66FF66;">_Here, the function is defined in terms of itself._</span></span>

----

## THIS Recursive Function

<pre><code class="python" data-trim data-noescape>def foo():
  foo()</code></pre>

<span class="fragment">...Well, it's pretty stupid, actually...</span>

<span class="fragment">_Can you imagine what would happen if we run it?_</span>

<span class="fragment">It would produce an <span style="color: tomato;">**infinite loop**</span> calling itself</span>

<span class="fragment">over and over again...</span>

<span class="fragment">And eventually it would <span style="color: tomato;">**crash**</span> our program!</span>

----

_Why would it **crash**?_  

<span class="fragment">Basically, if a **loop** keeps cycling forever,</span>

<span class="fragment">eventually we'll run out of **memory**.</span>

<span class="fragment">So, we need something to _**stop**_ this loop...<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

_Why would it **crash**?_  

<span class="fragment">Because this recursive function is missing<br>something very important...</span>

<span class="fragment">something fundamental to all<br>recursive functions, which we call a...</span>

<h3><span class="fragment">Base Case <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>
</span></h3>

~~

## Base Case

<span class="fragment">Without a **base case**, a recursive function<br>would go on _recursing forever..._</span>

<span class="fragment">A **base case** is used to **STOP** a recursive function.</span>

<span class="fragment">_Do you remember how we STOP a for loop?_<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

We use a **base case** to STOP a _recursive function_  

<span class="fragment">similarly to how a **termination condition**<br>is used to **STOP** a _for loop._</span>

----

In Python, here's a _recursive function_ with a **base case**:  

<pre><code class="python" data-trim data-noescape>def factorial(n):
    if n == 1:
        return 1
    else:
        return n * factorial(n-1)</code></pre>

<span class="fragment">This one calculates the _factorial_ of a number.</span>

<span class="fragment">For example, <span style="color: tomato;">_3 factorial_</span> would be defined as <span style="color: tomato;">`3!`</span></span>

<span class="fragment">where <span style="color: tomato;">`n=3`</span> evaluates to <span style="color: tomato;">`3 x 2 x 1 = 6`</span>.<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

_So, how does this crazy thing work?_  
First, notice that <span style="color: #66FF66;">_the function **calls itself**._</span>  

<pre><code class="python" data-trim data-noescape>def factorial(n):
    if n == 1:
        return 1
    else:
        return n * factorial(n-1)</code></pre>

<span class="fragment">On line 1, we define the function <span style="color: tomato;">`factorial(n)`</span>,</span>  

<span class="fragment">But _inside_ our definition; _inside_ our <span style="color: tomato;">`else`</span> statement,</span>  

<span class="fragment">on line 5, the <span style="color: tomato;">`factorial`</span> function is **called**;</span>  

<span class="fragment">with an <span style="color: tomato;">**argument**</span> of <span style="color: tomato;">`n-1`</span>, or: <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

_1 less than the argument <span style="color: tomato;">`n`</span> given in the **previous** function call._  

<span class="fragment">This means the function <span style="color: tomato;">`factorial`</span> will keep _**calling** itself!_</span>  

<span class="fragment">Each time, reducing <span style="color: tomato;">`n`</span> by a value of 1... <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

For example, if we were to run <span style="color: tomato;">`factorial(3)`</span>  

<span class="fragment">Our function would _**call itself**_ in this order:</span>  

<span class="fragment"><span style="color: tomato;">`factorial(3)`</span></span>  

<span class="fragment"><span style="color: tomato;">`factorial(2)`</span></span>  

<span class="fragment"><span style="color: tomato;">`factorial(1)`</span></span>

<span class="fragment">And we obtain our solution: <span style="color: tomato;">`3 x 2 x 1 = 6`</span></span>

----

But, how does this function know _when_ to <span style="color: tomato;">**STOP**</span>?  

<span class="fragment">How does it _know_ when to stop _reducing by 1?_</span>  

<span class="fragment">The answer is:</span>

<h3><span class="fragment">The Base Case <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>
</span></h3>

~~

_But where is this **BASE CASE** thing already??_

<iframe src="{{ site.baseurl }}/public/confused.travolta.transparent.gif" width="600px" height="600px" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>

~~

Inside our function definition,  
the <span style="color: tomato;">`if`</span> clause gives us our base case:  

<pre><code class="python" data-trim data-noescape>def factorial(n):
    if n == 1:
        return 1</code></pre>

<span class="fragment">This says: _if <span style="color: tomato;">`n`</span> is 1, return the value 1, and STOP repeating._</span>

<span class="fragment">We know it will **STOP** because inside the `else` clause,</span>

<span class="fragment">there is **no function call** to keep our function looping.</span>

----

_How can we see what's going on **inside** the function?_

<iframe src="{{ site.baseurl }}/public/confused.travolta.transparent.gif" width="600px" height="600px" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>

~~

_And why is Confused John Travolta_  
_asking all the questions??_

<iframe src="{{ site.baseurl }}/public/confused.travolta.transparent.gif" width="600px" height="600px" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>

~~

To see what happens  
each time the function is **called** internally,  

<span class="fragment">we can add <span style="color: tomato;">`print()`</span> statements at each step. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Here, I'll add 2  <span style="color: tomato;">`print()`</span> statements,  
one inside the <span style="color: tomato;">`if`</span> clause, and another  
inside the <span style="color: tomato;">`else`</span> clause:  

<pre><code class="python" data-trim data-noescape>def factorial(n):
    if n == 1:
        print("n is 1, so return 1 and STOP!")
        return 1
    else:
        print("n is " + str(n) + ", so reduce n and CALL n-1=" + str(n-1))
        return n * factorial(n-1)</code></pre>

<span class="fragment">_Now, we can monitor what happens at each step..._ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Now, when we _execute_ this function,  
by **calling it once** inside our Python code:  

<pre><code class="python" data-trim data-noescape>factorial(3)</code></pre>

the output (in the Terminal) will be:  

<pre><code class="console" data-trim data-noescape>$ <span style="color: tomato;">python /path/to/my/python/script.py</span>
n is 3, so reduce n and CALL n-1=2
n is 2, so reduce n and CALL n-1=1
n is 1, so return 1 and STOP!
6
$ </code></pre>

<span class="fragment">And we obtain our result: <span style="color: tomato;">`3 x 2 x 1 = 6`</span>.</span>

<span class="fragment">_Each time, <span style="color: tomato;">`n`</span> is multiplied by <span style="color: tomato;">`n-1`</span>... **UNTIL** <span style="color: tomato;">`n=1`</span>._ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

**Each repeated step** is _similar_ to the previous one:  

<pre><code class="console" data-trim data-noescape>factorial(3) : n=3 : <span style="color: tomato;">3</span>
factorial(2) : n-1=2 : 3 x (3-1) = <span style="color: tomato;">6</span>
factorial(1) : n-1=1 : 6 x (2-1) = <span style="color: tomato;">6</span>
<i>final result returned by our function:</i> <span style="color: tomato;">6</span></code></pre>

<span class="fragment">Each **operation** is the same, but the **input** changes...</span>

<span class="fragment">so, the result we evaluate **each time**<br>_is not identical... but related_.</span>

----

What would this simple **recursive function** look like  

<span class="fragment">in JavaScript? <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Inside of an HTML file, and between `<script>` tags,  
we could write a JS version of our `factorial()` function,  
which would look like this:  

<pre><code class="javascript" data-trim data-noescape>function factorial(n) {
  if (n == 1) {
    return 1;
  } else {
    return n * factorial(n-1);
  }
}</code></pre>

<span class="fragment">On your own:<br>_How could you add_ `print` _statements to this?_</span>

----

And, as always,  
<span style="color: tomato;">**carefully note the differences in syntax**</span>  
between _Python_ and _JavaScript_!  

----

_Okay fine, but can you give us more (MOAR!) examples_  

<span class="fragment">_of **recursions** and how they work?_</span>

----

For a <span style="color: tomato;">**visual**</span> example, watch  
this video by Daniel Shiffman:  

<iframe src="https://www.youtube.com/embed/0jjeOYMjmDU" width="560" height="315" frameborder="0"></iframe>

in which he explains [tree branching structures](https://io9.gizmodo.com/scientists-still-puzzled-by-a-fractal-discovered-500-ye-5864577){:target="_blank"} and  
writes a **recursion** in his own JavaScript library: [**p5.js**](https://p5js.org/){:target="_blank"}  

<span class="fragment"><span style="color: tomato;">_You **don't** need to know **p5.js** to understand this video!_</span></span>

----

For a more <span style="color: tomato;">**intermediate**</span> example,  
watch this video by Professor Thorsten Altenkirch:  

<iframe src="https://www.youtube.com/embed/8lhxIOAfDss" width="560" height="315" frameborder="0"></iframe>

in which he explains the famous [Tower of Hanoi](https://en.wikipedia.org/wiki/Tower_of_Hanoi){:target="_blank"} problem,  
and writes a **recursion** in Python to solve it!  

----

_So... did you watch those videos?_  

<span class="fragment">_If not, go back and watch them all the way through!_</span>  

<span class="fragment"><span style="color: tomato;">_You **might very well** be quizzed or tested on them..._</span></span>

----

### So, to summarize:  

<span class="fragment">**For loops** and **while loops** are both _**iterative**._</span>

<span class="fragment">A **while loop** is like a **for loop** with a **conditional statement**.</span>

<span class="fragment">**Self-similarity** is when _parts_ bear resemblance to the _whole._</span>

<span class="fragment">**Recursion** is something that's defined _in terms of itself._</span>

<span class="fragment">A **Recursive function** includes a **call** _to itself,_<br>producing repetitions that are _similar_ but _not identical._</span>

----

Finally, here are some possible  

### Discussion Questions  

on the remaining slides  

<span class="fragment">_Prepare your responses to these questions,_</span>  

<span class="fragment">_And bring them to class:_</span>

----

## Discussion Question #1  

<span class="fragment">What are some situations<br>when you should you use a **for loop**?</span>

<span class="fragment">And how about some situations<br>when should you'd best use a **while loop**?</span>

----

## Discussion Question #2  

<span class="fragment">What are some _self-similar_ objects<br>you've encountered in nature?</span>

<span class="fragment">(...Something not mentioned already in these slides?)</span>

----

## Discussion Question #3  

<span class="fragment">What are some _differences_ between **iteration** and **recursion**?</span>

----

## Finé  

Now, time to do [the labs...](https://einbahnstrasse.github.io/Goldford-MTEC1003-OL04/labs/09/dummy.html){:target="_blank"}
