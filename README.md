pcpctest
========

using Zurb Foundation 3 - [documentation](http://foundation.zurb.com/old-docs/f3/)


### PROBLEM:

Using the Orbit jQuery slider that comes with Zurb Foundation 3. Unfortunately, it's buggy and deals with the "Flash of Unstyled Content". Orbit is fixed in Foundation 4. Unfortunately, a rewrite to Foundation 4 is not an option at this time. 

### POSSIBLE SOLUTION

Look at implement bxslider jquery slider, [http://bxslider.com](http://bxslider.com)


# UPDATE: August 24, 2013

Ryan Mitts updated markup for bxslider js and it works much better. Much more fluid than that of Orbit. But problem still remained with "Flash of Unstyled Content" on page load. See [http://bzerangue.github.io/pcpctest/index2.html](http://bzerangue.github.io/pcpctest/index2.html)

**But, found the solution of the "Flash of Unstyled Content" issue...**

- First copied Ryan's adjusted files to index2.html and workspace/js/app-previous.js
- Added `style="display:none;"` to `<ul id="bxslider">` \- [https://github.com/bzerangue/pcpctest/blob/master/index.html#L212](https://github.com/bzerangue/pcpctest/blob/master/index.html#L212)
- And then added jQuery method `.show()` to `$('.bxslider')` \- [https://github.com/bzerangue/pcpctest/blob/master/workspace/js/app.js#L50](https://github.com/bzerangue/pcpctest/blob/master/workspace/js/app.js#L50)
- also, added the option of auto... to auto slide the slides.

Here's the result...

[http://bzerangue.github.io/pcpctest/index.html](http://bzerangue.github.io/pcpctest/index.html)

Now it hides the ul#bxslider until the window loads... and it keeps from the having the "flash of unstyled content" issue from happening. 
---

## MUCH MUCH MUCH thanks to the great Ryan Mitts from [d6interactive.com](http://www.d6interactive.com) who helped me figure this out. 
