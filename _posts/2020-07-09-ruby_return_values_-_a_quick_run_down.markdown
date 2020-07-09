---
layout: post
title:      "Ruby Return Values - A Quick Run Down"
date:       2020-07-09 20:02:36 +0000
permalink:  ruby_return_values_-_a_quick_run_down
---


We'll now do a quick run through of review values on Ruby.

In Ruby, we have both implicit and explicit return values. Let's consider the following example:

1     def multiply(x, y)
2        x * y
3     end
4 
5     multiply (2, 3)

That would as expected, get you the value 6. Simple enough. But what if we made the following change:

1     def multiply (x, y)
2         x * y
3     		"Houston, we have a problem!"
4     end
5
6     multiply(3, 4)

In this case, we would not get lucky #12 ... Rather instead, the insertion of the inauspicious string in line 3 means that string is the last item evaluated within the code block of our multiply method. As such, the code block within the multiply method would *implicitly* return this string rather than our arithmetical operation.


In short, rather than just having *explicit* return values - the result the block following our instertions of **return** - our Ruby code will also pick up values like line 3 as implicit return values.

As you work on your projects like the "CLI Project" keep the above in mind as you define your different instance methods to help ensure your code both works as you expect it to and is both clean and easy to follow. 



