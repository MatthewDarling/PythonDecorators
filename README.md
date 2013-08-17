Python Decorators
=================

On a whim, I decided I was brave enough to give a presentation at [EdmontonPy](http://edmontonpy.com/) before I went back home to Ottawa. I also decided to give the presentation via Emacs. Granted, I spent several hours learning about Emacs Lisp and org-mode, but it was *a ton of fun* once I got everything working.

The full org-mode source of the presentation can be [viewed online via GitHub](Presentation.org), which works reasonably well. If you download that file, you can open it in Emacs and execute all the code examples and stuff.

After several hours of fiddling, I managed to export the presentation to [S5](http://meyerweb.com/eric/tools/s5/), using the exporter in Org 8's contrib files. I had to manually edit the output a bit - I'm going to write a blog post about the steps involved and I'll link to it here when I'm done.

Anyway, you should soon be able to view the presentation on the [project page for this repository](http://matthewdarling.github.io/PythonDecorators).

Technical notes
===============

If you're curious, my [Emacs setup](https://github.com/MatthewDarling/.emacs) is available. I used [org-present](https://github.com/rlister/org-present/) to do the heavy lifting. You'll want to add some hooks to org-present-mode so that it behaves properly - you can see my org-specific configuration from when I presented [here](https://github.com/MatthewDarling/.emacs/blob/93f9374417b9ea049bb44843d79dd3e4927777aa/init-org.el). The stuff for org-present is at the bottom, should be pretty clear. Also, before running the various examples, you'll want to eval the code blocks under the "Setup" heading (it may work without doing that, I'm not sure).

Also, I recorded a really awesome/really fragile macro to execute the first code block in a "slide" with one button, and open up the \*output\* buffer. This worked out surprisingly well! You can see that [here](https://github.com/MatthewDarling/.emacs/blob/93f9374417b9ea049bb44843d79dd3e4927777aa/init-org.el#L68). It requires ido-mode to be turned on. (What it's supposed to do: `C-s` to search, `(` to place the cursor inside the code block (what are the odds of a code block not including an opening paren?), `C-c C-c` to evaluate the code block. The output is sent to a buffer called *output* by the my-post block. So then I hit `C-x 4 b`, bound to `ido-switch-buffer-other-window`, and type *out* to select the *output* buffer, and enter to select it. Then I can hit the down arrow key to close the window and kill the buffer.

I also used a script made in [AutoHotKey](autohotkey.com) to turn my PowerPoint-focused presenter remote into something actually useful. You can see that [here](presenting.ahk).
