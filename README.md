Python Decorators
=================

On a whim, I decided I was brave enough to give a presentation at [EdmontonPy](http://edmontonpy.com/) before I went back home to Ottawa. I also decided to give the presentation via Emacs. I may have spent several hours learning about Emacs Lisp and org-mode, but it was *a ton of fun* once I got everything working.

The full org-mode source of the presentation can be [viewed online via GitHub](https://github.com/MatthewDarling/PythonDecorators/blob/master/EdmontonPyPresentation.org), which works reasonably well. If you download that file, you can open it in Emacs and execute all the code examples and stuff.

I'm working on exporting the presentation to [S5](http://orgmode.org/worg/org-tutorials/non-beamer-presentations.html#sec-3), so it can be viewed online in a nice way. Hopefully with syntax highlighting.

Technical notes
===============

If you're curious, my [Emacs setup](https://github.com/MatthewDarling/.emacs) is available. I used [org-present](https://github.com/rlister/org-present/) to do the heavy lifting. My org-specific configuration at the time is in [this file](https://github.com/MatthewDarling/.emacs/blob/c5c3e54a12aef371f0a66fda0bdcd6ad6329fa8c/init-org.el).

Also, I recorded a really awesome/really fragile macro to execute the code in a "slide" with one button, and open up the \*output\* buffer. This worked out surprisingly well! You can see that [here](https://github.com/MatthewDarling/.emacs/blob/c5c3e54a12aef371f0a66fda0bdcd6ad6329fa8c/init-org.el#L66).

I also used a script made in [AutoHotKey](autohotkey.com) to turn my PowerPoint-focused presenter remote into something actually useful. You can see that [here](https://github.com/MatthewDarling/PythonDecorators/blob/master/presenting.ahk).
