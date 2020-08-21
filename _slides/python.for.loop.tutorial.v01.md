---
title: For Loops in Python
description: MTEC1003 — Media Computation Skills Lab
theme: black
---
<script src='https://kit.fontawesome.com/a076d05399.js'></script>
<!-- https://www.w3schools.com/icons/fontawesome5_icons_arrows.asp -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/9.18.3/styles/night-owl.min.css">
<script src="//cdnjs.cloudflare.com/ajax/libs/highlight.js/9.11.0/highlight.min.js"></script>
<script>hljs.initHighlightingOnLoad();</script>
<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
<!-- http://www.iangoodfellow.com/blog/jekyll/markdown/tex/2016/11/07/latex-in-markdown.html -->
<!-- http://www.vishalsinha.in/2017/04/23/highlight-code-jekyll.html -->

## In this tutorial, we'll discuss...

<span class="fragment">_Iteration_</span>  

<span class="fragment">_Collection_</span>  

<span class="fragment">and _For Loops_ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

...but in _Python_, **NOT** JavaScript!...

----

## For Loop structure  

First, let's recall  
[the general structure of a _For Loop_ in JavaScript,](https://einbahnstrasse.github.io/Goldford-MTEC1003-OL04/labs/08/js.for.loops.v02.html#13.0){:target="_blank"}  
which you learned in the 1st set of slides.  

<!-- <img class="plain" src="{{ site.baseurl }}/io.diagrams/brush.png" alt="brush" width="500px"> -->
<!-- <img class="plain" src="{{ site.baseurl }}/io.diagrams/brush.png" alt="brush" width="500px" style="background:none; border:none; box-shadow:none;"> -->
<!-- <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i> -->

----

What were the **3 main components** of a _For Loop?_  

<span class="fragment">**initialization**</span>  

<span class="fragment">**termination condition**</span>  

<span class="fragment">**increment** <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

And what would each of those pieces look like _in JavaScript?_  

----

## Initialization  

<pre><code class="javascript" data-trim data-noescape>for (var x = 0; ........; ........) {
  [Do things expressed by the statements written here <i>each time.</i>];  
  }</code></pre>

_What does the initialization part do?_  

<span class="fragment">_Initialization_ tells us how to begin an iteration,</span>   

<span class="fragment">typically starting with an _index variable_ (e.g. var x),</span>  

<span class="fragment">set to a certain value (e.g. var x = 0)</span>

----

## Termination Condition  

<pre><code class="javascript" data-trim data-noescape>for (........; x <= 5; ........) {
  [Do things expressed by the statements written here <i>each time.</i>];  
  }</code></pre>

_What does the termination condition do?_  

<span class="fragment">The _termination condition_ tells us how the loop will end,</span>  

<span class="fragment">typically when the _index variable_ reaches a certain limit or threshold, e.g. when x reaches 5.</span>  

<span class="fragment">Our loop will therefore _iterate_ 5 times.</span>  

----

## Increment  

<pre><code class="javascript" data-trim data-noescape>for (........; ........; x = x + 1) {
  [Do things expressed by the statements written here <i>each time.</i>];  
  }</code></pre>

_What does the increment do?_  

<span class="fragment">The _increment_ shows us how our process _continues,_<br>or how we _increment_ through our loop.</span>  

<span class="fragment">This tells us how much we add to the value x _each time._</span>  

<span class="fragment">In this case, we add 1 to the variable x _each time_ we cycle through the loop.</span>  

----

Now, let's see how these  

## Same Three Components  

are written in Python...  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

<pre><code class="python" data-trim data-noescape>for x in range(0, 5):
    [Do things expressed by the statements written here <i>each time.</i>]</code></pre>

<span class="fragment">Before I break this down for you,<br>try to understand the Python syntax.</span>

<span class="fragment">Do you see all 3 elements?</span>

<span class="fragment">Is anything missing?? <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Notice that the 3 elements are written differently in Python than in JavaScript:

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

In Python, the  

### Initialization  

is made by first writing  
**for**    

<span class="fragment">then the **1st argument** to `range()`<br>defines the initial value of our _index variable_ x.</span>

<span class="fragment">This initial value is 0. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

### Termination Condition  

We know the loop will be finished when x reaches 5...  

<span class="fragment">because the value 5 is given as the<br>**2nd argument** to `range()`. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

_But how do we know what the_  

### Increment    

_will be??_

Look again...  

<pre><code class="python" data-trim data-noescape>for x in range(0, 5):
    [Do things expressed by the statements written here <i>each time.</i>]</code></pre>

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>  

~~

If you guessed that there is nothing in our Python code to indicate the increment,  
_then you guessed correctly..._

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>  

~~

In this particular format in Python, the _increment_ is given with a **3rd argument** to `range()`:  

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
But we could have...  
These 3 _possible_ arguments are as follows:  

<pre><code class="python" data-trim data-noescape>range([start], [stop], [step])</code></pre>

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>  

~~

**Argument #1** or [start] is the _initial_ value. This argument is _optional_ and if no value is given, the _default_ will be 0.  

<span class="fragment">**Argument #2** or [stop] is the _terminating_ value. This argument is _NOT optional_ and, if only 1 argument is given to `range()`, it will be taken as the <stop> value.</span>

<span class="fragment">**Argument #3** or [step] is the _incremental_ value. This argument is _optional_ and, if no 3rd argument is given, the _default_ will be 1. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

This means that we could just have easily have written  
the following **shorthand** version of our _For Loop_ in Python:  

<pre><code class="python" data-trim data-noescape>for x in range(5):
    [Do things expressed by the statements written here <i>each time.</i>]</code></pre>

<span class="fragment">In this case, `range()` falls back to its default values:</span>

<span class="fragment">Since there is only 1 value, that is taken as the [stop] value.<br>We will _iterate_ up to 5.</span>

<span class="fragment">The default value for [start] is 0, so we will start indexing from 0.</span>

<span class="fragment">The default value for [step] is 1, so we will count by 1.</span>

<span class="fragment">In this case, our output will be 0, 1, 2, 3, and 4.</span>

----








----

## In programming languages

These "choices" are called <span style="color: #66FF66;"><b><i>conditions</i></b></span>  
and they determine the course of actions our programs take.  

<img class="plain" src="{{ site.baseurl }}/io.diagrams/lamp.png" alt="brush" width="350px" style="background:none; border:none; box-shadow:none;">

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

### But they're not _just_ choices...

_Conditions_ can indeed mean _instructions_  
given to software programs by _users:_  

<img class="plain" src="{{ site.baseurl }}/io.diagrams/deletefiles.png" alt="brush" width="500px" style="background:none; border:none; box-shadow:none;">

----

### Evaluation

Or they can also also be used to _evaluate_ our data.

<img class="plain" src="{{ site.baseurl }}/io.diagrams/team.png" alt="brush" width="500px" style="background:none; border:none; box-shadow:none;">

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

Notice the use of <span style="color: #66FF66;"><b><i>True</i></b></span> and <span style="color: red"><b><i>False</i></b></span> in the last slide.

In programs like JavaScript and Python,  
<span style="color: #66FF66;"><b><i>True</i></b></span> and <span style="color: red"><b><i>False</i></b></span> are called:

## Boolean Values

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

## Booleans are values

just like other _values types_ we've encountered:  

<span class="fragment">integers</span>  

<span class="fragment">floating-point numbers</span>  

<span class="fragment">strings <br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

And like these other _value types_, we can do lots with them...  

For example, we can assign booleans to <span style="color: #66FF66;"><b><i>variables.</i></b></span>  
In JavaScript:  

<pre><code class="javascript" data-trim data-noescape> var x = true;</code></pre>    

<span style="color: red"><i>(Notice in JS that the letter "t" is <b>NOT</b> capitalized.)</i></span>

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

We can even create a _new_ variable  
based on a changing _threshold:_  

<pre><code class="javascript" data-trim data-noescape> var belowFreezing = temperature < 32;</code></pre>

<span class="fragment">If the <span style="color: #66FF66;">temperature</span> variable is less than 32,</span>  

<span class="fragment">the <span style="color: #66FF66;">belowFreezing</span> variable will evaluate to: <span style="color: #66FF66;">true</span>.</span>  

<span class="fragment">Or if not, it will be: <span style="color: #66FF66;">false</span>.<br>[view source](https://www.khanacademy.org/computing/ap-computer-science-principles/programming-101/boolean-logic/a/conditionals-with-if-else-and-booleans){:target="_blank"}</span>  

----

## in Python

Boolean values are essentially the same...  

But, we _CAPITALIZE_ <span style="color: #66FF66;"><b><i>True</i></b></span> and <span style="color: red"><b><i>False</i></b></span>

----

In programming languages,  
_boolean values_ only give us words for  

"true" or "false."  

----

At some point, we want to **identify**  

<span style="color: #66FF66;">the _quality of being "true" or "false"_</span>  

in the stuff we're talking about;  
in the data we're processing.  

----

For this, we need to _assign_ a boolean value  
to a larger piece of language...  
One that binds a _boolean value_ to an object...  

----

Behold! To _assign_ a boolean value, we need a  

## Statement  

the same way that we _assign_ a variable.  
Here's a statement that does just that:     

<pre><code class="javascript" data-trim data-noescape> var x = "I'm a string and now I equal variable x!";</code></pre>

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

But to assign a boolean _value_, we must use one of the    

## Boolean Operators  

which can either be:

<span class="fragment"><span style="color: #66FF66;">a _logical_ operator</span>  
<span class="fragment"><span style="color: #66FF66;">a _comparison_ operator</span>  
<span class="fragment"><span style="color: #66FF66;">or a _conditional_ operator </span><br><br>_Yikes! Srsly?!_<br>_This seems way too complicated._<br>_What the hell are those things?_</span>  

----

## Comparison Operators  

In JavaScript, we use these:  

<span class="fragment"><span style="color: #66FF66;">==</span> (equal to)</span>  

<span class="fragment"><span style="color: #66FF66;">===</span> (equal value AND equal type)</span>  

<span class="fragment"><span style="color: #66FF66;">!=</span> (not equal)</span>  

<span class="fragment"><span style="color: #66FF66;">!==</span> (not equal value OR not equal type)</span>  

<span class="fragment"><span style="color: #66FF66;">&gt; [or] &lt;</span> (greater than [or] less than)</span>  

<span class="fragment"><span style="color: #66FF66;">&lt;=</span> (less than OR equal to)</span>  

<span class="fragment"><span style="color: #66FF66;">&gt;=</span> (greater than OR equal to) <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

~~

## = vs. ==

_Remember!_  
<span style="color: red"><b>= is an <i>assignment operator</i></b></span>

and is only used to _assign_ a value to something.  
For determining _equality,_ we instead  
use the equality operators:  

**==**  
**===**  
or  
**!=**

----

## Logical Operators  

In JavaScript:  

<span class="fragment"><span style="color: #66FF66;">&&</span> (logical "AND")</span>  

<span class="fragment"><span style="color: #66FF66;">||</span> (logical "OR")</span>  

<span class="fragment"><span style="color: #66FF66;">!</span> (logical "NOT")</span>   

----

Additionally, we can use a  

## Conditional Operator

to test for a boolean (true/false),  
and then assign one of two values to our variable.  
In JavaScript, we use the <span style="color: #66FF66;">?</span> operator for this.  

----

For example, in JavaScript:  

<pre><code class="javascript" data-trim data-noescape> var voteable = (age < 18) ? "Too young":"Old enough";</code></pre>

<span class="fragment">If the <span style="color: #66FF66;">age</span> variable is less than 18,</span>

<span class="fragment"><span style="color: #66FF66;">voteable</span> will be "Too young".</span>

<span class="fragment">Or if not, <span style="color: #66FF66;">voteable</span> will be "Old enough".<br>[view source](https://www.w3schools.com/js/js_comparisons.asp){:target="_blank"}</span>   

----

## Plain English in Python

In Python, _some operators_ look more like spoken language:   

<span class="fragment"><span style="color: #66FF66;">and</span> (logical "AND")</span>  

<span class="fragment"><span style="color: #66FF66;">or</span> (logical "OR")</span>  

<span class="fragment"><span style="color: #66FF66;">not</span> (logical "NOT")<br>[_How do these Python operators compare to JavaScript?_](#/11){:target="_blank"}<br><i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Special cases of this in Python include the operators:

<span style="color: #66FF66;"><b>is<br>is not</b></span>  

These aren't the same as operators == or !=,  
as you might have guessed...  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'>

~~

## is (or is not) vs. == (or !=)

Whereas <span style="color: #66FF66;"><b>==</b></span> tests for the _values_  
on both sides of the operator,  
<span style="color: #66FF66;"><b>is</b></span> tests for the same _object._  

Let's demonstrate this with a quick example...  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'>

~~

Here are 2 empty _lists_ in Python:

<pre><code class="python" data-trim data-noescape>  list1 = []
  list2 = []</code></pre>

[_(Remember! = does not mean "equal"!)_](#/10/1){:target="_blank"}

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'>

~~

Now, if I evaluate this statement:

<pre><code class="python" data-trim data-noescape>  result = list1 == list2
  print(result)</code></pre>

what do you think will happen?

<span class="fragment">Well, it will return <span style="color: #66FF66;"><b><i>True</i></b></span> because the _values_ contained inside the _objects_ (the lists) are identical, i.e. they're both empty!</span>

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'>

~~

But what if I evaluate this one?  

<pre><code class="python" data-trim data-noescape>  result = list1 is list2
  print(result)</code></pre>

Will it still be <span style="color: #66FF66;"><b><i>True</i></b></span>?

<span class="fragment">It turns out to be <span style="color: red"><b><i>False</i></b></span> because, even though their _values_ are the same, the _objects_ are different. Both lists are stored in different locations in computer memory; one for list1 and another for list2. They're the same _type,_ and indeed contain the same _values,_ but they are _not at all_ the same _object._ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

This means that the operators:  

<span style="color: #66FF66;"><b>is</b></span>   
and  
<span style="color: #66FF66;"><b>is not</b></span>  

tell us about the _objects_  
and not just the _values_ contained in them.  

[view source](https://www.geeksforgeeks.org/difference-operator-python/){:target="_blank"}  

____

With boolean _operators_ and _values_, we can now form  

## Boolean Expressions

Boolean **expressions** _evaluate_ to boolean **values**,  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

meaning a **statement** is evaluated  
and its result is either <span style="color: #66FF66;"><b><i>True</i></b></span> or <span style="color: red"><b><i>False</i></b></span>.

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

For example, this _boolean expression_ in Python:  

<pre><code class="python" data-trim data-noescape>  result = 60 == (30 * 2)
  print(result)</code></pre>

will return the _boolean value:_  

<pre><code class="python" data-trim data-noescape>  True</code></pre>

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

whereas this _boolean expression:_

<pre><code class="python" data-trim data-noescape>  result = 'there' == 'their'
  print(result)</code></pre>

will definitely be

<pre><code class="python" data-trim data-noescape>  False</code></pre>  

since the strings are not the same.  

----

We can also form _compound boolean expressions_  
by testing _multiple_ statements at the same time.  

For example:

<pre><code class="python" data-trim data-noescape>  result = 4 > 0 and 2 < 1
  print(result)</code></pre>

What do you think the value of <span style="color: #66FF66;"><b>result</b></span> will be?

<span class="fragment">In our console, we'll see <span style="color: red"><b><i>False</i></b></span> because _both_ of the expressions _are not_ true. In this case, only one of them is true, and by using the operator <span style="color: #66FF66;"><b>and</b></span> we're requiring that _both_ expressions be true. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Okay, I just can't stop myself.  
How about this one?  

<pre><code class="python" data-trim data-noescape>  result = 4 > 0 or 2 < 1
  print(result)</code></pre>

<span class="fragment">This time we'll def get a <span style="color: #66FF66;"><b><i>True</i></b></span> because _at least one_ of the expressions is true. By invoking the operator <span style="color: #66FF66;"><b>or</b></span> we're dropping our requirement that _both_ expressions be true. <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

Obviously, when evaluating multiple boolean expressions  
things get complicated really fast!  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

Often we need to visualize all possible outcomes at once.
This is done with a _Truth Table._ For example:  

<img class="plain" src="{{ site.baseurl }}/io.diagrams/truth.table.png" alt="brush" width="500px" style="background:none; border:none; box-shadow:none;">  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

To sort out the confusion, you can  
[read all about Truth Tables here.](https://openbookproject.net/thinkcs/python/english3e/conditionals.html){:target="_blank"}  

____

So far we've examined:  

<span class="fragment">boolean _values_<br></span>
<span class="fragment">boolean _operators_<br></span>
<span class="fragment">boolean _expressions_<br><br></span>

<span class="fragment">We've now got all the building blocks we need<br>to make some fancy, shmancy _conditions..._</span>

----

In addition to _states_ of true- or false-ness,  
we still need language to express  
_what will happen_ or _what to do_  
in one scenario or another.  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

Each of these _scenarios_ is a

## Condition  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

----

## If, then, else, else if

Think back, waaaayy back, many slides ago...  
way back to your [JavaScript Conditionals slides](https://einbahnstrasse.github.io/Goldford-MTEC1003-OL04/labs/06/js-conditionals.html#10.0){:target="_blank"}  
and you'll remember how a basic condition  
is constructed in JavaScript:  

<pre><code class="javascript" data-trim data-noescape>  var a = parseInt(prompt("Give me a number, any number..."), 10);
  if (a > 5) {
    console.log(a);
  }</code></pre>

_What does this conditional statement "say"?_

<span class="fragment">"<b>If</b> a is greater than 5, <b>then</b> print a to the console." <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

## In Python  
the same story is told with a different construction:  

<pre><code class="python" data-trim data-noescape>  a = float(input("Give me a number, any number... "))
  if a > b:
    print(a)</code></pre>

_So, what's different in Python?_  

<span class="fragment">no semicolon ;</span>

<span class="fragment">no brackets { or }</span>

<span class="fragment">no (parens) around the _boolean expression_</span>

<span class="fragment">use of a colon : _following_ the boolean expression</span>

----

But what about _multiple conditions?_  

For this, we need another kind of statement:  

## Else if  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

To make an **"else if"** statement in JavaScript:  

<pre><code class="javascript" data-line-numbers="1-2|3-4|5-7">  var a = parseInt(prompt("Give me a number, any number..."), 10);
  if (a <= 40) {
    console.log("Your number is less than or equal to 40");
  } else if (a <= 60) {
    console.log("Your number is less than or equal to 60");
  } else {
    console.log("Your number is greater than 60");
  }</code></pre>

_And what do the conditional statements "say"?_

<span class="fragment">"<b>If</b> a is less than or equal to 40, <b>then</b> print to the console."</span>

<span class="fragment">"<b>Or if</b> a is less than or equal to 60, <b>then</b> print a 2nd message."</span>

<span class="fragment">"<b><i>Or if neither condition is true</i></b>, print a 3rd message." <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

## Python Syntax  
<pre><code class="python" data-line-numbers="1-2|3-4|5-6">  a = float(input("Give me a number, any number... "))
  if a <= 40:
      print("Your number is less than or equal to 40")
  elif a <= 60:
      print("Your number is less than or equal to 60")
  else:
      print("Your number is greater than 60")</code></pre>

<span class="fragment">no semicolon ; <i>as before</i></span>

<span class="fragment">no brackets { or } <i>as before</i></span>

<span class="fragment">no (parens) <i>as before</i></span>

<span class="fragment">use of a colon : <i>as before</i></span>

<span class="fragment"><b>NEW: elif</b> instead of <b>else if</b> <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

_And what's SIMILAR in both JavaScript and Python?_

<span class="fragment">if</span>

<span class="fragment">else</span>

<span class="fragment">statements begin _**without** indentation_</span>

<span class="fragment">statements always end _**with** indentation_<br>(i.e. the _**"then"**_ clause)</span>

<span class="fragment">can _chain_ together multiple "elif"s (in JS: "else if")...</span>

----

## Chaining 'Elif's  

Let's augment our Python to include multiple "scenarios":

<pre><code class="python" data-line-numbers="1-2|3-4|5-6">  a = float(input("Give me a number, any number... "))
  if a <= 40:
      print("Your number is less than or equal to 40")
  elif a <= 60:
      print("Your number is less than or equal to 60")
  elif a <= 100:
      print("Your number is less than or equal to 100")
  else:
      print("Your number is greater than 100")</code></pre>

<span class="fragment">You're not limited to just 3: if / else if / else.<br>It's easy to **add** as many conditions as you need!</span>

<span class="fragment">_How would you do this in JavaScript? Try it!_</span>

----

## Compound Boolean Expressions in Conditions

We can also make a _conditional statement_  
that includes _compound boolean expressions._  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

For example, in Python:   

<pre><code class="python">  a = float(input("Give me a number, any number... "))
  if a >= 5 and a <= 40:
      print("Your number is in between; it's a sandwich!")
  elif a < 5 or a > 40:
      print("Your number is out-of-range!")
  else:
      print("Umm, you didn't type a number...")</code></pre>

<span class="fragment">Here, we've created an _interval_ spanning the range 5-40:<br>$$ a = \{ 5 \leqslant x \leqslant 40 \}, \forall x \in \mathbb{R} $$</span>

<span class="fragment">Meaning: _**a**_ is a set of all numbers _**x**_ between (and including) 5 and 40, for all _**x**_ contained in the set of _Real whole numbers._</span>

<span class="fragment">_How would you do this in JavaScript? Try it!_</span>

----

## Finé

Now, time to do [the labs...](https://einbahnstrasse.github.io/Goldford-MTEC1003-OL04/labs/07/lab-07-part2-python-conditionals.html){:target="_blank"}  

----