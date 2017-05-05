![decorators make people think they're smart, but nobody uses them regularly](https://cdn.rawgit.com/Dobiasd/articles/3370dffd/programming_language_learning_curves/python.png)

Python Decorators
=================

On a whim, I decided I was brave enough to give a presentation at [EdmontonPy](http://edmontonpy.com/) before I went back home to Ottawa. I also decided to give the presentation via Emacs. Granted, I spent several hours learning about Emacs Lisp and org-mode, but it was *a ton of fun* once I got everything working.

The full org-mode source of the presentation can be [viewed online via GitHub](Presentation.org), which works reasonably well. If you download that file, you can open it in Emacs and execute all the code examples and stuff.

After several hours of fiddling, I managed to export the presentation to [S5](http://meyerweb.com/eric/tools/s5/), using the exporter in Org 8's contrib files. I had to manually edit the output a bit - I'm going to write a blog post about the steps involved and I'll link to it here when I'm done.

Anyway, you should soon be able to view the presentation on the [project page for this repository](http://matthewdarling.github.io/PythonDecorators).

Technical notes
===============

I used a script made in [AutoHotKey](autohotkey.com) to turn my PowerPoint-focused presenter remote into something actually useful. You can see that [here](presenting.ahk).

If you're curious, my [Emacs setup](https://github.com/MatthewDarling/.emacs) is available. I used [org-present](https://github.com/rlister/org-present/) to do the heavy lifting. Before running the examples, you'll want to eval the code blocks under the "Setup" heading.

You'll want to add some hooks to org-present-mode so that it's more presentation-ish - [something like this](https://github.com/MatthewDarling/.emacs/blob/8a91020c0646eb6a7fd95f173121002234e556d2/matthewdarling/changes.el#L63-L93). This is a bit updated from what I used for the decorators talk.

For the decorators talk, I recorded a keyboard macro that would execute a code block and then jump over to its results. It worked surpringly well! But I've since replaced it with [a bit of elisp](https://github.com/MatthewDarling/.emacs/blob/8a91020c0646eb6a7fd95f173121002234e556d2/matthewdarling/changes.el#L63-L74). ```exec-next-plus-jump-to-result``` looks for a Clojure code block that is putting its results into an Org block, executes that code, then jumps down to the block.
