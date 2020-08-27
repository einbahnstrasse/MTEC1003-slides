---
title: For Loops in Python
description: MTEC1003 — Media Computation Skills Lab
theme: black
---

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

<span class="fragment">_Iteration_ + _Collection,_</span>  

<span class="fragment">_Lists_ vs. _Dictionaries_</span>  

<span class="fragment">Python _Methods_</span>

<span class="fragment">_Arithmetic Series_</span>

<span class="fragment">and _For Loops_ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

...but in _Python_, **NOT** JavaScript!...

----

## What is Iteration?  

<span class="fragment">Simply put, **iteration** is the process of _repeating a set of instructions_ until some condition is met. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

## "Why use a Loop?"  

Repetitive tasks take time to code, so it's much more efficient to write a _loop._ With a loop we can:  

<span class="fragment">tell the computer to _repeat_ similar tasks many times,</span>  

<span class="fragment">save valuable time typing endless lines of code, <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

### and also very important...  

<span class="fragment">by forcing ourselves to think carefully about the "rules"<br>we create to govern our loops,</span>  

<span class="fragment">we clarify what we want to accomplish</span>  

<span class="fragment">and avoid making the careless mistakes<br>that occur when we type by hand!</span>  

----

## What is Iteration used for?  

Think of what we can accomplish with _iterative processes..._  

<span class="fragment">rapidly **generate** long lists of numbers</span>  

<span class="fragment">periodically **check** on the value of some variable</span>  

<span class="fragment">**count through** the items in a list</span>  

<span class="fragment">**search** for a string in _each line_ of a text file</span>  

<span class="fragment">_Can you think of some others?_</span>  

----

## Iterate + Collect  

Imagine we have a list of numbers:  

<pre><code class="javascript" data-trim data-noescape>var myList = [1, 3, 7, 5, 4, 2, -3, -9];</code></pre>

Let's say we want to  
_add a value of 2_ to each number in the list...  

<span class="fragment">With a _for loop,_ we can execute an _iterative process_ to _count through_ and perform the _same operation(s)_ on each list item, like adding a constant to each number. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

Our first task would be to be to _iterate over_ the contents of the list, counting through each item while performing the same set of actions.  

<pre><code class="javascript" data-trim data-noescape>1 + 2;
3 + 2;
7 + 2;
5 + 2;
... etc. ...</code></pre>  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

But we still need to **collect** the result into a _new list:_  

<pre><code class="javascript" data-trim data-noescape>var myNewList = [3, 5, 9, 7, 6, 4, -1, -7];</code></pre>  

<span class="fragment">The process by which we create a _new list_<br>**after** we iterate over our data is called **collection.**</span>

<span class="fragment">We'll discuss how _collection_ is done soon.<br>First, let's examine further the _for loop structure._</span>

----

## For Loop Structure  

Let's recall  
[the general structure of a _For Loop_ in JavaScript,](https://einbahnstrasse.github.io/Goldford-MTEC1003-OL04/labs/08/js.for.loops.v02.html#13.0){:target="_blank"}  
which you learned in the 1st set of slides.  

----

What were the **3 main components** of a _For Loop?_  

<span class="fragment">**1. initialization**</span>  

<span class="fragment">**2. termination condition**</span>  

<span class="fragment">**3. increment** <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

And what would each of those pieces look like _in JavaScript?_  

----

## Initialization  

<pre><code class="javascript" data-trim data-noescape>for (var x = 0; ........; ........) {
  [Do things expressed by the statements written here <i>each time.</i>];  
  }</code></pre>

_What does the initialization part do?_  

<span class="fragment">It tells us **how to begin**,</span>   

<span class="fragment">typically starting with an _index variable_ (e.g. var x),</span>  

<span class="fragment">set to a certain value (e.g. var x = 0)</span>

----

## Termination Condition  

<pre><code class="javascript" data-trim data-noescape>for (........; x <= 5; ........) {
  [Do things expressed by the statements written here <i>each time.</i>];  
  }</code></pre>

_What does the termination condition do?_  

<span class="fragment">It tells us **how the loop will end**,</span>  

<span class="fragment">typically when the _index_ reaches a threshold.</span>  

<span class="fragment">This loop will _terminate_ when x reaches 5.</span>  

----

## Increment  

<pre><code class="javascript" data-trim data-noescape>for (........; ........; x = x + 1) {
  [Do things expressed by the statements written here <i>each time.</i>];  
  }</code></pre>

_What does the increment do?_  

<span class="fragment">It shows us how our process _continues,_<br>or how we _step through_ our loop.</span>  

<span class="fragment">It tells us how much we add to **x** _each time._</span>  

<span class="fragment">Here, we add 1 to x _each time_ we cycle through the loop,<br> until it reaches our **termination** goal.</span>  

----

Now, let's see how these  

## Same Three Components  

are written in Python...  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

## In Python  

<pre><code class="python" data-trim data-noescape>for x in range(0, 5):
    [Do things expressed by the statements written here <i>each time.</i>]</code></pre>

<span class="fragment">Before I break this down for you,<br>can you tell what the syntax is doing?</span>

<span class="fragment">Do you see all 3 elements?</span>

<span class="fragment">Is anything missing......?? <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

In Python, the  

### Initialization  

is made by first typing  

**for**    

<span class="fragment">then the **1st argument** to `range()`<br>defines the initial value of our _index variable_ x.</span>

<span class="fragment">This initial value is 0. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

_Let's see that again on the "instant replay"..._

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

<pre><code class="python" data-trim data-noescape>for x in range(0, 5):
    [Do things expressed by the statements written here <i>each time.</i>]</code></pre>

<span class="fragment">`for` initializes the loop structure.</span>  

<span class="fragment">We create variable **x** for indexing.</span>  

<span class="fragment">And yes indeed, the **1st argument** to `range()` is 0,<br>and that's where our indexing _begins._</span>

----

### Termination Condition  

We know the loop will be finished when x reaches 5...  

<span class="fragment">because the value 5 is given as the<br>**2nd argument** to `range()`. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

_Let's see that again on the "instant replay"..._

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

<pre><code class="python" data-trim data-noescape>for x in range(0, 5):
    [Do things expressed by the statements written here <i>each time.</i>]</code></pre>

<span class="fragment">Yes indeed, the **2nd argument** to `range()` is 5,<br>and that's where our indexing _ends._</span>

----

_But how do we know what the_  

### Increment    

_will be??_

<pre><code class="python" data-trim data-noescape>for x in range(0, 5):
    [Do things expressed by the statements written here <i>each time.</i>]</code></pre>

<span class="fragment">Where is our x = x + 1 statement,<br> like in JavaScript? <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

If you guessed that there is currently  
**nothing in our Python code**  
that appears to designate the increment,  

_then you guessed correctly..._

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>  

~~

In this particular format, the _increment_ is given  
with a **3rd argument** to `range()`:  

<pre><code class="python" data-trim data-noescape>for x in range(0, 5, 2):
    [Do things expressed by the statements written here <i>each time.</i>]</code></pre>

<span class="fragment">The arguments to `range()` are 0, 5, and 2.</span>

<span class="fragment">Here, the **3rd argument** is 2.</span>

<span class="fragment">This means "go from 0 to 5, but _increment_ 2 at a time."</span>  

<span class="fragment">Our output will be: 0, 2, and 4. (5 will be omitted.)</span>  

----

## Range()  

In our original code, we did not have  
a **3rd argument** for `range()`  
but we could have...  

There are 3 _possible_ arguments:  

<pre><code class="python" data-trim data-noescape>range(<span style="color: #66FF66;"><b>color: #</b></span>, <span style="color: red"><b>[stop]</b></span>, <span style="color: #66FF66;"><b>[step]</b></span>)</code></pre>

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>  

~~

**Argument #1** or <span style="color: #66FF66;"><b>[start]</b></span> is the _initial_ value. This argument is <span style="color: #66FF66;"><b><i>optional</i></b></span> and if no value is given, the _default_ will be 0.  

<span class="fragment">**Argument #2** or <span style="color: red"><b>[stop]</b></span> is the _terminating_ value. This one is <span style="color: red"><b><i>NOT optional</i></b></span> and, if only 1 argument is given, it will be taken as the [stop] value.</span>

<span class="fragment">**Argument #3** or <span style="color: #66FF66;"><b>[step]</b></span> is the _incremental_ value. It is <span style="color: #66FF66;"><b><i>optional</i></b></span> and, if no 3rd argument is given, the _default_ will be 1. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

And finally, if only 2 arguments are given,  
those are taken to mean:  

<pre><code class="python" data-trim data-noescape>range(<span style="color: #66FF66;"><b>[start]</b></span>, <span style="color: red"><b>[stop]</b></span>)</code></pre>

So unless we provide this "hidden" 3rd argument,  
we can overlook how to specify our _increment_ or _step._

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

This means we could just as easily have written  
a **shorthand** version with only 1 argument!  

<pre><code class="python" data-trim data-noescape>for x in range(5):
    [Do things expressed by the statements written here <i>each time.</i>]</code></pre>

<span class="fragment">In this case, `range()` falls back to its default values:</span>

<span class="fragment">There is only 1 argument, so it's taken as <span style="color: red"><b>[stop]</b></span>.<br>We will _iterate_ up to 5.</span>

<span class="fragment">We will start indexing from 0, i.e. <span style="color: #66FF66;"><b>[start]</b></span>'s default value.</span>

<span class="fragment">The default for <span style="color: #66FF66;"><b>[step]</b></span> is 1, so we will count by 1s.</span>

<span class="fragment">In this case, our output will be: 0, 1, 2, 3, and 4.</span>

----

Now, let's use this _structure_  
to make some really _simple, stupid_ loops...  

----

For example (in Python):  

<pre><code class="python" data-trim data-noescape>for x in range(5):
    print(x)</code></pre>

<span class="fragment">I mean this one is _painfully stupid._</span>  

<span class="fragment">It just prints out the numbers 0 through 4!</span>  

<span class="fragment">I mean come on, who needs this?? <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

But, before we move on to making more _useful_ loops,  
what will our output look like?  

Will it look like this?  

<pre><code class="python" data-trim data-noescape>0, 1, 2, 3, 4</code></pre>

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

If you guessed, "nope!"  
then you guessed correctly...  

_So, why won't it look like this?_

<span class="fragment">Because we've done nothing to **collect**<br>the results into a new list.</span>

<span class="fragment">_What will our output look like then?_ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

<pre><code class="python" data-trim data-noescape>0
1
2
3
4</code></pre>

<span class="fragment">This represents our output at _each loop cycle,_<br>or **each time**. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

We see the output _each time_  
because our `print()` call is **indented**:  

<pre><code class="python" data-trim data-noescape>for x in range(5):
    print(x)</code></pre>

<span class="fragment" style="color: red">**Indentation** in Python works like **brackets** in JavaScript.</span>

<span class="fragment">If it's indented, it's part of a statement _inside_ the loop,</span>

<span class="fragment">and it will repeat _each time,_</span>

<span class="fragment">much like bracketed code in JavaScript.</span>

----

Now let's say we want to  
**collect** our results into a **new list**.  

<span class="fragment">So, instead of seeing the output **each time**,</span>  

<span class="fragment">we want to see only the **final** set of numbers.</span>  

<span class="fragment">For this, we need to create a _list,_ and use a _method_...</span>

----

## Using Lists + Methods

We'll adapt our code ever so slightly...

<pre><code class="python" class="line-numbers" data-trim>y = []
for x in range(5):
    y.append(x)
print(y)</code></pre>

Now if we run this code, our output will be:  

<pre><code class="python" data-trim data-noescape>[0, 1, 2, 3, 4]</code></pre>

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~  

_Okay that's a LOT of change in the code. What's going on here?_

<span class="fragment">Line 1 instantiates an **empty list**, i.e. [ ].</span>

<span class="fragment">Line 3 _collects each element **x** into the list **y**._</span>

<span class="fragment">Also, line 3 uses the `.append()` _method_<br>to **collect** into our list.</span>

<span class="fragment">And line 4 prints the final collection **y**.</span>

----

## What is a Method?

On line 3, the statement  

<pre><code class="python" class="line-numbers" data-trim>y.append(x)</code></pre>  

tells us to **append** new data to the list  
that we've attached to variable **y**  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

The **argument** to `y.append()`  
is our _index variable_ **x**  

<span class="fragment">So we are _appending the list_ **y** with the current value of **x**.</span>

<span class="fragment">We do this _each time_ the loop cycles through. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>
</span>

~~

We call `.append()` a _method_ of **y**.  

<span class="fragment">[A _method_ is a function that _belongs_ to an object.](https://docs.python.org/3/tutorial/classes.html#:~:text=A%20method%20is%20a%20function,%2C%20sort%2C%20and%20so%20on.){:target="_blank"}</span>

<span class="fragment">**y** is a _list,_ and there are functions<br>that "belong" to Python lists...</span>

<span class="fragment">These include `.append()`, `.insert()`, `.remove()`, `.sort()`,<br>and other common list processing operations.</span>

----

How do we know  `print()` will run _at the end?_  

<pre><code class="python" class="line-numbers" data-trim>y = []
for x in range(5):
    y.append(x)
print(y)</code></pre>

<span class="fragment">Line 4 is _**not indented**_ like line 3.</span>

<span class="fragment">This means line 4 is _not inside_ the loop structure<br>and therefore runs _after_ the loop finishes. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Line 4 is executed _after_ the loop is finished.  

<span class="fragment">It therefore prints the _current state_ of the list **y**</span>

<span class="fragment">_after_ the loop stops **collecting** into it.</span>

----

## Iterating Over a List

Say you have this list:

<pre><code class="python" class="line-numbers" data-trim>myShoppingList = ["soap", "video games", "hand sanitizer", "eggs", "masks"]</code></pre>

<span class="fragment">In this case, a list comprised of **strings**...</span>

<span class="fragment">_How would we iterate each item, one at a time?_</span>

----

In JavaScript, we could do this:

<pre><code class="javascript" data-trim data-noescape>var myShoppingList = ["soap", "video games", "hand sanitizer", "eggs", "masks"];
for (var i = 0; i < myShoppingList.length; i = i + 1) {
  console.log(myShoppingList[i]);
  }</code></pre>

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

And our output would be:  

<pre><code class="javascript" data-trim data-noescape>soap
video games
hand sanitizer
eggs
masks</code></pre>

<span class="fragment">exactly what we want:<br>an iterated list of shopping items.</span>

----

This works because we did 2 new things:  

<span class="fragment">1. We used `.length` to give us<br>the number of items in `myShoppingList`, and</span>

<span class="fragment">2. We used `myShoppingList[i]`<br>to process each item in our list. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

`myShoppingList[i]`  

Each time the loop cycles, we use our index **i**  
to reference and print the **i**th place in our list.

----

To do the same thing  
## In Python  

<pre><code class="python" class="line-numbers" data-trim>myShoppingList = ["soap", "video games", "hand sanitizer", "eggs", "masks"]
for elem in myShoppingList:
  print(elem)</code></pre>

<span class="fragment">Output is the same as in JavaScript.</span>

<span class="fragment">`elem` counts each _element_ in the named _list._</span>

<span class="fragment">...a nice shorthand!</span>

----

## Dictionaries

But what if our data looked like this?  

<pre><code class="python" class="line-numbers" data-trim>myShoppingList = {"soap": 0.75, "video games": 23.95, "hand sanitizer": 1.90, "eggs": 2.99, "masks": 15.50}
</code></pre>

<span class="fragment">This isn't a list...</span>

<span class="fragment">It's another data structure called a **dictionary**.<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

<pre><code class="python" class="line-numbers" data-trim>myDict = {"key": value, "key": value}</code></pre>

<span class="fragment">Similar to a _database,_<br>each item in a dictionary is a **key/value pair**.<br></span>

----

We can access 1 or both of our keys/values with a _For Loop:_  

<pre><code class="python" class="line-numbers" data-trim>myShoppingList = {"soap": 0.75, "video games": 23.95, "hand sanitizer": 1.90, "eggs": 2.99, "masks": 15.50}
for k, v in myShoppingList.items():
  print('key:', k, ', value:', v)</code></pre>

<span class="fragment">This works because on line 2<br>we _iterate in parallel_ each **key/value pair**...</span>

<span class="fragment">Notice we iterate 2 things:<br> `for k, v in` ...and not simply... `for k in` <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Our output will be:

<pre><code class="python" class="line-numbers" data-trim>key: soap , value: 0.75
key: video games , value: 23.95
key: hand sanitizer , value: 1.9
key: eggs , value: 2.99
key: masks , value: 15.5</code></pre>

<span class="fragment">Check the fancy `print()` message we made on line 3;</span>

<span class="fragment">Remember: this technique is a _string concatenation!_</span>

----

## Counting Backwards

Remember how we did this [in JavaScript?](https://einbahnstrasse.github.io/Goldford-MTEC1003-OL04/labs/08/js.for.loops.v02.html#16.1){:target="_blank"}  

<span class="fragment">_How can we accomplish this in Python?_ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Well, we can manipulate the **arguments**  
in our `range()` function:

<pre><code class="python" data-trim data-noescape>range(<span style="color: #66FF66;"><b>[start]</b></span>, <span style="color: red"><b>[stop]</b></span>, <span style="color: #66FF66;"><b>[step]</b></span>)</code></pre>

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

What do these **arguments** tell us?    

<pre><code class="python" data-trim data-noescape>range(5, 0, -1)</code></pre>

<span class="fragment"><span style="color: #66FF66;"><b>[start]</b></span> at 5,</span>

<span class="fragment"><span style="color: red"><b>[stop]</b></span> at 0,</span>

<span class="fragment"><span style="color: #66FF66;"><b>[step]</b></span> -1 _each time._</span>

<span class="fragment">_What will our output be?_ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

<pre><code class="python" data-trim data-noescape>5
4
3
2
1</code></pre>

<span class="fragment">_Why doesn't it go from 4 to 0?_ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

To get our numbers in our preferred range,  
make a small adjustment to the **arguments**:  

<pre><code class="python" data-trim data-noescape>range(4, -1, -1)</code></pre>

_How is this one different?_  

<span class="fragment"><span style="color: #66FF66;"><b>[start]</b></span> at 4,</span>

<span class="fragment"><span style="color: red"><b>[stop]</b></span> at -1,</span>

<span class="fragment"><span style="color: #66FF66;"><b>[step]</b></span> -1 _each time._ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Now, the output is:  

<pre><code class="python" data-trim data-noescape>4
3
2
1
0</code></pre>

----

## Arithmetic Series  

How can we use a _For Loop_  
to quickly **generate** an increasing list of numbers?

<span class="fragment">_How about a long list from 1 to 100?_<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

In science papers you might see **Capital-sigma notation**:  

$$ \sum_{i=1}^{100-1} a_{i} = a_{i} + a_{i+1} + a_{i+2} +\dotsb+ a_{i+(100-1)}  $$

which also means _a list ("series") from 1 to 100:_  

<span class="fragment">It means: the **sum** $$ \sum $$ of all **terms** $$ a_{i} $$</span>

<span class="fragment">from a **low limit** of 1, or $$ i=1 $$</span>

<span class="fragment">to a **high limit** of 100, or $$ i+(100-1) $$</span>


~~

Try this:  

<pre><code class="python" data-trim data-noescape>y = []
limit = 100
for x in range(1, limit + 1):
    y.append(x)
print(y)</code></pre>

<span class="fragment">For this, we [1] make an _empty list,_</span>

<span class="fragment">Then, [2] define a _count_ variable (100),</span>

<span class="fragment">[3] set up a _For Loop_ from 1 to our _count,_</span>

<span class="fragment">[4] collect all _indices_ **x** into our _list_ **y**,</span>

<span class="fragment">and [5] print the final list. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

<pre><code class="python" data-trim data-noescape>range(1, limit + 1)</code></pre>

Our **arguments** ensure the output is correct:  

<span class="fragment"><span style="color: #66FF66;"><b>[start]</b></span> at 1,</span>

<span class="fragment">and <span style="color: red"><b>[stop]</b></span> at **limit** + 1.</span>

<span class="fragment">We add 1 to **limit** because the loop will _terminate_ at 101,<br>_after_ 100 has been _appended_ to the list!</span>

<span class="fragment">That's how we get numbers from 1 to 100... <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

The output is correct!    

<pre><code class="python" data-trim data-noescape>[1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 70, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 84, 85, 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100]</code></pre>

<span class="fragment">We've **collected** all numbers into 1 giant list.</span>

<span class="fragment">Sometimes, **collecting** an _increasing_ number<br>of elements is called **accumulation**.</span>

----

## Finé

Now, time to do [the labs...](https://einbahnstrasse.github.io/Goldford-MTEC1003-OL04/labs/08/dummy.html){:target="_blank"}  

----
