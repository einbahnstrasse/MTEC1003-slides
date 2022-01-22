---
title: Function Definitions + Calls
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
<!-- <link rel="stylesheet" href="/MTEC1003-slides/public/css/monokai.css" id="highlight-theme"> -->

<!-- <link rel="stylesheet" href="lib/css/monokai.css"> -->
<!-- <script src="plugin/highlight/highlight.js"></script> -->

## In this tutorial, we'll discuss...

<span class="fragment">Function Calls + Definitions</span>

<span class="fragment">Encapsulation</span>

<span class="fragment">Algorithms</span>

<span class="fragment">Built-In Functions</span>

<span class="fragment">Parameters + Arguments <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

...but in _Python_, **NOT** JavaScript!...

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

...okay fine, we'll also talk  
_a little bit about JavaScript too._  
There, _ya happy?!_

So, let's get started:

----

## First of all, what is a Function?  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

<blockquote cite="https://en.wikipedia.org/wiki/Debugging">
  &ldquo;Functions are 'self contained' modules of code that accomplish a specific task. Functions usually 'take in' data, process it, and 'return' a result.&rdquo;
</blockquote>
—[view source](https://www.cs.utah.edu/~germain/PPS/Topics/functions.html){:target="_blank"}  

----

## Why use a Function? #1

<span class="fragment">We can break down a program into **sub-steps**.</span>

<span class="fragment">Each **sub-step** can be _its own function._</span>

<span class="fragment">When any program seems too hard,<br>just break down the program into **sub-steps**!<br>[—view source](https://www.cs.utah.edu/~germain/PPS/Topics/functions.html){:target="_blank"} <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>
</span>

~~

## Why use a Function? #2

<span class="fragment">We can _recycle_ our code instead of constantly<br>needing to **retype it** over and over again!</span>

<span class="fragment">When you think about it,<br>we benefit similarly from writing a _for loop_. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>
</span>

~~

## Why use a Function? #3

<span class="fragment">We can _test_ a portion of our code,<br>by _isolating_ it from the rest.<br>[—view source](https://www.cs.utah.edu/~germain/PPS/Topics/functions.html){:target="_blank"} <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>
</span>

~~

## Why use a Function? #4

<span class="fragment">Finally, remember _way back_ when we learned **variables**?</span>

<span class="fragment">Well, as you'll see in larger programs,<br>**functions** will also let you<br>**organize** _elaborate systems of variables_<br>accessed by different parts of your program.</span>

<span class="fragment">They'll be called **global** and **local** variables.</span>

----

## Encapsulation

<span class="fragment">Functions _reduce our code_</span>

<span class="fragment">by [**encapsulating**](https://en.wikipedia.org/wiki/Encapsulation_(computer_programming)){:target="_blank"} many ordered steps<br>into their own self-contained unit,</span>

<span class="fragment">allowing us to run complicated routines<br>by executing _one line_ of code instead of many!</span>

----

## What is an Algorithm?

<span class="fragment">**Algorithms** are the sets of **instructions**<br>executed by our programs.</span>

<span class="fragment">They can be described _apart_ from any **syntax**<br>or language we're working with... <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>
</span>

~~

Remember our lovely flowcharts?  

<img class="plain" src="{{ site.baseurl }}/io.diagrams/lamp.png" alt="brush" width="350px" style="background:none; border:none; box-shadow:none;">

These came up when we described _conditions._  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

We can use flowcharts to **plan** and **describe**  
### step-by-step procedures  
that we type out in code.  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

Some procedures may require a _conditional,_ as we learned.

<span class="fragment">**Conditions** involve _making a choice,_<br>accounting for _multiple possible scenarios,_ etc.<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

...while other **step-by-step procedures**  
may require things like:  

<span class="fragment">**counting**</span>

<span class="fragment">**iterating**</span>

<span class="fragment">**generating**</span>

<span class="fragment">_What sort of programming have we learned for this?_ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

As you may have guessed,  

<span class="fragment">we can best use a _for loop_</span>

<span class="fragment">to accomplish something like this.</span>

----

But in general,

<span class="fragment">_any step-by-step process_</span>

<span class="fragment">may be captured</span>

<span class="fragment">inside a **function**... <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

That means things like:  

<span class="fragment">_for loops,_</span>

<span class="fragment">_conditionals,_</span>

<span class="fragment">and other programming **statements**</span>

<span class="fragment">can ALL be contained inside your **functions**.<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Because they describe the individual **steps**  
or **tasks** within your **algorithm**.

----

## How Do We Use Functions?  

<span class="fragment">To _use_ a function, that is, to _execute_ it,</span>

<span class="fragment">we simply **call** the function<br>somewhere in our program,</span>

<span class="fragment">like this... <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>
</span>

~~

In JavaScript:

<pre><code class="javascript" data-trim data-noescape>console.log("Hello world!");</code></pre>  

In Python:

<pre><code class="python" data-trim data-noescape>print("Whoa, I can print something... How useless.")</code></pre>

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

This is known as a **function call.**  

----

## Function Calls

<span class="fragment">1. Type the **name** of the function.</span>

<span class="fragment">2. Don't type a space...</span>

<span class="fragment">3. Type **parens**: `()`</span>

<span class="fragment">4. Inside the parens, type comma-separated **arguments**<br>given as **input** to your function. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>
</span>

~~

For example, in Python:

<pre><code class="python" data-trim data-noescape>my_function_name(argument1, argument2, argument3)</code></pre>

Now, compare this to:

<pre><code class="python" data-trim data-noescape>print("Whoa, I can print something... How useless.")</code></pre>

<span class="fragment">The **print** function is **called** by _passing_ it 1 **argument**.<br>Here, the argument is a **string**,<br>which the function prints to the console.</span>

----

But your computer doesn't just "know"  
miraculously how to _interpret_ `print()`...  

<span class="fragment">How does your computer know<br>what a function does? <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>
</span>

~~

## Built-In Functions

<span class="fragment">Like `console.log()` in JavaScript,</span>

<span class="fragment">`print()` in Python is a **built-in function**,</span>

<span class="fragment">meaning it is **defined** somewhere<br>inside the Python code base. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>
</span>

~~

_What are some **built-in functions** you've already used?_  

<span class="fragment">`float()`</span>

<span class="fragment">`int()`</span>

<span class="fragment">`input()`</span>

<span class="fragment">`str()`</span>

<span class="fragment">`type()`</span>

----

That's nice & all...  

<span class="fragment">But I'm a creative do0d...</span>

<span class="fragment">And I write my _own_ functions,</span>

<span class="fragment">thank you very much... <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>
</span>

~~

So,  
what if you need to write  
a function that isn't _built-in?_  
<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

Well, first of all,

## NEWS FLASH OMG!

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

You can write _your very own functions!_  

<iframe src="https://www.youtube.com/embed/F7rLiILFWFo?autoplay=1&loop=1&modestbranding=1&rel=0&fs=0" width="560" height="315" frameborder="0"></iframe>

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

And this is done by first creating a **function definition**.

----

## Function Definitions  

<span class="fragment">When writing your _own_ functions,</span>

<span class="fragment">You first need to **define** its individual steps. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

The syntax is different for various programming languages,  

<span class="fragment">but generally, they all follow a pattern: <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

## 1. Declare Your Function!  
[For example, in JavaScript:](https://www.w3schools.com/JSREF/jsref_function.asp#:~:text=The%20function%20statement%20declares%20a,expression%20(See%20Function%20Definitions)){:target="_blank"}  

<pre><code class="javascript" data-trim data-noescape>function toCelsius(fahrenheit) {
  var tempInCelsius = (5 / 9) * (fahrenheit - 32);
  return tempInCelsius;  
}  
</code></pre>

<span class="fragment">Line 1: Type <span style="color: red">`function`</span> to **declare** a _function statement._</span>

<span class="fragment">Give your function a **NAME**, e.g. <span style="color: red">`toCelsius`</span></span>

<span class="fragment">Inside <span style="color: red">**parens** `()` </span>type your <span style="color: red">parameters,</span> e.g. `fahrenheit`.</span>

<span class="fragment">Type <span style="color: red">curly brackets: `{}`</span> <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

## 2. Algorithmic Steps  

On subsequent lines, code the _individual steps_  
of your **algorithm** _inside your curly brackets:_  

<pre><code class="javascript" data-trim data-noescape>var tempInCelsius = (5 / 9) * (fahrenheit - 32);</code></pre>

<span class="fragment">Here we've defined variable `tempInCelsius`<br>and used the <span style="color: red">parameter</span> `fahrenheit` in our calculation.</span>

<span class="fragment">Write as many steps as you need; here we only need 1. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

## 3. Return Statement

Often we need a function to <span style="color: red">`return`</span> a value to us:  
For example, on the last line of our function definition:  

<pre><code class="javascript" data-trim data-noescape>  return tempInCelsius;
}</code></pre>

<span class="fragment">When this function is **called** within our program,</span>

<span class="fragment">the value of `tempInCelsius` will be <span style="color: red">**returned**</span> to the program, at the place where the **function call** was made.<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

## 4. Function Call  

For example, if we **call** our function  
somewhere in our program, say here:  

<pre><code class="javascript" data-trim data-noescape>var tempInStLouis = toCelsius(104);</code></pre>

<span class="fragment">`toCelsius` will <span style="color: red">`return`</span> the value <span style="color: red">`40`</span> on this line,</span>

<span class="fragment">which means its resulting value of 40<br>will be **assigned** to the **variable** `tempInStLouis` !</span>

----

### Let's See that again... in Python!  

<span class="fragment">Maybe you've already guessed it, but...</span>

<span class="fragment">in Python, the same logic will require<br>some _slight_ syntactical adjustments...<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

## Declare Your Function!
### (Python Style)

<pre><code class="python" data-trim data-noescape>def toCelsius(fahrenheit):
  tempInCelsius = (5 / 9) * (fahrenheit - 32)
  return tempInCelsius
</code></pre>

<span class="fragment">_Notice anything different?_</span>

<span class="fragment"><span style="color: red">`def`</span> instead of <span style="color: red">`function`</span></span>

<span class="fragment"><span style="color: red">colon `:`</span> instead of <span style="color: red">curly brackets `{}`</span></span>

<span class="fragment">and of course, no <span style="color: red">semicolons `;`</span><br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

## Indentation is Everything  

<span class="fragment">_Notice any patterns?_</span>

<span class="fragment">Just like when we write [for loops]({{ site.baseurl }}/slides/python.for.loop.tutorial.v01/#/){:target="_blank"} and [conditionals,]({{ site.baseurl }}/slides/python.conditionals.tutorial.v01/#/){:target="_blank"}</span>

<span class="fragment">in Python, we don't use curly brackets for [code blocks,](https://en.wikipedia.org/wiki/Block_(programming)){:target="_blank"}</span>

<span class="fragment">but instead rely heavily on [_proper indentation_.](https://docs.python.org/2.0/ref/indentation.html){:target="_blank"} <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

So, be sure your **indenting** game is on fleek...

<img class="plain" src="http://www.gamenmeme.com/wp-content/uploads/2016/05/11.png" alt="brush" width="250px" style="background:none; border:none; box-shadow:none;">  

----

## Parameters vs. Arguments

By now, you've noticed both of these terms.  

<pre><code class="python" data-trim data-noescape>def my_function_name(param1, param2, param3):</code></pre>
<pre><code class="python" data-trim data-noescape>my_function_name(argument1, argument2, argument3)</code></pre>

<span class="fragment">You may hear them used interchangeably,<br>but they mean different things... <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

## A Parameter  

<span class="fragment">In a function **definition**,</span>

<span class="fragment">a **parameter** is a _placeholder_ for **input data**</span>

<span class="fragment">**listed** inside (parens),</span>

<span class="fragment">and **referenced** inside of your function. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

For example:

<pre><code class="python" data-trim data-noescape>def my_function_name(param1, param2):
  mult = param1 * param2
  return mult
</code></pre>

<span class="fragment">These **parameters** are simultaneously **arguments**... <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

## Wait, _what?!_  

<iframe src="https://giphy.com/embed/5wWf7H89PisM6An8UAU" width="600px" height="271px" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

## An Argument  

<a href="https://imgflip.com/i/3ziri7"><img src="https://i.imgflip.com/3ziri7.jpg" height="400px" title="Argument"/></a>

<span class="fragment">_Okay, haha, not **that** kind of argument..._ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

## An Argument

<span class="fragment">In a function **call**,</span>

<span class="fragment">an **argument** is a _real value_ for each **input data** point</span>

<span class="fragment">also **listed** inside (parens).</span>

<span class="fragment">Our function **expects** these **arguments**</span>

<span class="fragment">because they're **defined** by the **parameters** we set! <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

## So, what's the difference?  

<span class="fragment">We _create_ a **parameter** for each input data point<br>in our function **definition**.</span>

<span class="fragment">Then we _pass_ input _values_, or **arguments**, when we make<br>our function **call** and thus _use_ or _execute_ our function.</span>

<span class="fragment">_Let's see examples of both..._ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

First, our function **definition** includes 2 **parameters**:  

<pre><code class="python" data-trim data-noescape>def my_stupid_multiplier(param1, param2):
  mult = param1 * param2
  return mult
</code></pre>

Later, we supply our function **call** with 2 **arguments**:  

<pre><code class="python" data-trim data-noescape>my_stupid_multiplier(4, 8)</code></pre>

<span class="fragment">Our function knows to **expect** 2 _values_<br>because they were **defined** by our **parameters**.</span>

<span class="fragment">[More info: _parameters_ vs. _arguments_](https://en.wikipedia.org/wiki/Parameter_(computer_programming)#Parameters_and_arguments){:target="_blank"}</span>

----

### So, to summarize:  

<span class="fragment">"**FUNCTIONS** are 'self contained' modules of code...<br>that 'take in' data, process it, and 'return' a result."</span>

<span class="fragment">A **PARAMETER** is a _placeholder_ for input values<br>designated in our function **definition**.</span>

<span class="fragment">Later, when we **execute** a function,<br>we _pass_ it **ARGUMENTS**<br>for the values our function _expects._</span>

----

## Finé  

Now, time to do [the labs...](https://einbahnstrasse.github.io/Goldford-MTEC1003-OL04/labs/09/dummy.html){:target="_blank"}
