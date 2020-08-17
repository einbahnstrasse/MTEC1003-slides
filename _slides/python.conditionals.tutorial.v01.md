---
title: Booleans + Conditionals
description: MTEC1003 — Media Computation Skills Lab
theme: black
---
<script src='https://kit.fontawesome.com/a076d05399.js'></script>
<!-- https://www.w3schools.com/icons/fontawesome5_icons_arrows.asp -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/9.18.3/styles/night-owl.min.css">
<script src="//cdnjs.cloudflare.com/ajax/libs/highlight.js/9.11.0/highlight.min.js"></script>
<script>hljs.initHighlightingOnLoad();</script>
<!-- http://www.vishalsinha.in/2017/04/23/highlight-code-jekyll.html -->

## In this tutorial, we'll discuss...

<span class="fragment">Boolean _Values_</span>

<span class="fragment">Boolean _Operators_</span>  

<span class="fragment">Boolean _Expressions_</span>  

<span class="fragment">and _Conditionals_ <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

...but in _Python_, **NOT** JavaScript!...

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

...okay fine, we'll also talk  
_a little bit about JavaScript too._  
There, _ya happy?!_

So, let's get started:

----

## Sometimes

Ya gotta make a choice...  

<!-- <img class="plain" src="{{ site.baseurl }}/io.diagrams/brush.png" alt="brush" width="500px"> -->
<img class="plain" src="{{ site.baseurl }}/io.diagrams/brush.png" alt="brush" width="500px" style="background:none; border:none; box-shadow:none;">

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

<pre><code class="python" data-trim data-noescape>True</code></pre>

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

whereas this _boolean expression:_

<pre><code class="python" data-trim data-noescape>  result = 'there' == 'their'
  print(result)</code></pre>

will definitely be

<pre><code class="python" data-trim data-noescape>False</code></pre>  

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
This is done with a _Truth Table._  

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
way back to your [JavaScript Conditionals slides.](https://einbahnstrasse.github.io/Goldford-MTEC1003-OL04/labs/06/js-conditionals.html#10.0){:target="_blank"}  
and you'll remember how a basic condition  
is constructed in JavaScript:  

<pre><code class="javascript" data-trim data-noescape>  if (a > 5) {
    console.log(a);
  }</code></pre>

_What does this program "say"?_

<span class="fragment">"<b>If</b> a is greater than 5, <b>then</b> print a to the console." <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

## In Python  
the same story is told with a different construction:  

<pre><code class="python" data-trim data-noescape>  if a > b:
    print(a)</code></pre>

_So, what's different in Python?_  

<span class="fragment">no semicolon ;</span>

<span class="fragment">no brackets { or }</span>

<span class="fragment">no (parens) around _boolean expression_</span>

<span class="fragment">use of a colon : _following_ boolean expression</span>

----

But what about _multiple conditions?_ In JavaScript:  

<pre><code class="javascript" data-line-numbers="1-2|3-4|5-7">  if (a > 5) {
    console.log(a);
  ) else if (a < 40) {
    console.log(a);
  } else {
    console.log("a is not within range!");
  } </code></pre>

_And what does this program "say"?_

<span class="fragment">"<b>If</b> a is greater than 5, <b>then</b> print a to the console."</span>

<span class="fragment">"<b>Or if</b> a is less than 40, <b>then</b> still print a."</span>

<span class="fragment">"<b>Or if neither condition is true</b>, print an error message." <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>

~~

## In Python  
How would we tell the same story?  

<pre><code class="python" data-line-numbers="1-2|3-4|5-6">  if a > 5:
    print(a)
  elif a < 40:
    print(a)
  else:
    print("a is not within range!")</code></pre>

_So, what's different in Python?_




----

## Values

* <span style="color: #66FF66;">numbers</span>, e.g. 1, -2, 3.14, 35e3
* <span style="color: #66FF66;">strings</span>, e.g. "Hi Fred!"
* <span style="color: #66FF66;">boolean</span>, e.g. True, False

[c.f. Values in JS](https://einbahnstrasse.github.io/Goldford-MTEC1003-Fall2020/labs/05/js-basics.html#9.0)

----

## Numeric Operators

<span class="fragment">+</span>

<span class="fragment">-</span>

<span class="fragment">x</span>

<span class="fragment">÷</span>

<span class="fragment">% <i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i></span>  

[c.f. Operators in JS](https://einbahnstrasse.github.io/Goldford-MTEC1003-Fall2020/labs/05/js-basics.html#13.0)  

~~

## Remember your PEMDAS

<span class="fragment">(<span style="color: red">P</span>arens)</span>

<span class="fragment"><span style="color: red">E</span>xponents (powers, roots)</span>

<span class="fragment"><span style="color: red">M</span>ultiply</span>

<span class="fragment"><span style="color: red">D</span>ivide</span>

<span class="fragment"><span style="color: red">A</span>dd</span>

<span class="fragment"><span style="color: red">S</span>ubtract <br> [more on PEMDAS](https://www.mathsisfun.com/operation-order-pemdas.html)</span>  

----

## Comparison Operators

<span class="fragment">&lt;</span>

<span class="fragment"><=</span>

<span class="fragment">></span>

<span class="fragment">>=</span>

<span class="fragment">==</span>

<span class="fragment">!=</span>

<span class="fragment">is</span>

<span class="fragment">is not <br>[more on Python operators](https://docs.python.org/3/library/stdtypes.html)</span>

----

## Strings

<pre><code class="python" data-trim data-noescape>
  "Hi, I'm a string."
  'also a string'
  "string containing numbers: 4, 5.7"
  "string ending with a new line\n"
  "" # <= empty string
  '' # <= empty string w/single quotes
</code></pre>

[c.f. Strings in JS](https://einbahnstrasse.github.io/Goldford-MTEC1003-Fall2020/labs/05/js-basics.html#15.0)

----

## String Concatenation

<pre><code class="python" data-trim data-noescape>
  "hello" + "there"
  'you have ' + str(450000) + ' unread emails!!'
</code></pre>  
[c.f. String Operators in JS](https://einbahnstrasse.github.io/Goldford-MTEC1003-Fall2020/labs/05/js-basics.html#20.0)

_Wait, what's going on in that last line?_  

<span class="fragment">We used str() to turn 450000 into a string.</span>  
<span class="fragment">Then we concatenated it into a larger string:</span>  
<span class="fragment">'you have 450000 unread emails!!'</span>  
<span class="fragment">I mean, WOW.</span>  

----

## Statements in Python

<pre><code class="python" data-trim data-noescape>
  1 + 3
  4 x 5
</code></pre>

Notice there is <span style="color: red"><b>no semicolon at the end of a line</b></span> in Python!
_And how do we do Statements in JS?..._

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

## Statements in JavaScript

<pre><code class="javascript" data-trim data-noescape>
  1 + 3;
  4 x 5;
</code></pre>

_Notice anything different?_  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

_Friendly reminder:_
<h3><span style="color: red">All statements end in a semicolon in JavaScript!</span></h3>
[Any Questions?](https://einbahnstrasse.github.io/Goldford-MTEC1003-Fall2020/labs/05/js-basics.html#23.0)

----

## Variables

Remember in Javascript how we _declare_ variables?
<pre><code class="javascript" data-trim data-noescape>
  var x = "someValue";
</code></pre>  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

Well, it turns out **variables**,  
in _all_ languages,  
must be **declared** in some way...  

----

## Variables in Python

This couldn't be easier...

<pre><code class="python" data-trim data-noescape>
  x = 'someValue'
</code></pre>

_So, what's different?_  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

We don't need to type **var** to declare a variable.  

<i class='fas fa-arrow-alt-circle-down' style='font-size:48px;color:red'></i>

~~

In Python, a **variable** is _declared_  
as soon as it's assigned a value!

----

## Function

* a sequence of **statements** performing some action  
* **ordered statements:** like checking off a _to-do list_  
* can take inputs & return values, but doesn’t have to  

----

## Calling functions

To _execute_ (i.e. to "call") a function,  
type its name followed by parens...  

----

## A Built-in Python Function

<pre><code class="python" data-trim data-noescape>
  print("you have 450000 unread emails!!")
</code></pre>  

<span class="fragment">print() is the funcion call.</span>  
<span class="fragment">Input to the function goes inside the parens.</span>  
<span class="fragment">So, the string is its input. <br>[c.f. Functions in JS](https://einbahnstrasse.github.io/Goldford-MTEC1003-Fall2020/labs/05/js-basics.html#26.0)</span>  

----

## A Totally Stupid Program

<pre><code class="python" data-trim data-noescape>
  <mark>answer</mark> = input("Say something! ")
  print(<mark>answer</mark>)
</code></pre>  

<span class="fragment">1. Declare variable: <strong>answer</strong></span>  
<span class="fragment">2. Prompt user with <strong>input()</strong></span>  
<span class="fragment">3. Echo it with <strong>print()</strong><br>[c.f. same thing in JS](https://einbahnstrasse.github.io/Goldford-MTEC1003-Fall2020/labs/05/js-basics.html#31.2)</span>  

----

## Finé

Now, time to do [the labs...](https://einbahnstrasse.github.io/Goldford-MTEC1003-OL04/labs/05/lab-05-part2-python-basics.html){:target="_blank"}  
