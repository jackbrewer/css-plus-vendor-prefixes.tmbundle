##Introduction

This bundle contains commands to make handling CSS3 vendor prefixes a little bit easier.

Instead of adding prefixes to all standard snippets, this bundle allows you to code using the non prefixed versions of your CSS, then add the prefixes afterwards.

##Installation

In Terminal, navigate to the TextMate bundles folder.

	cd ~/Library/"Application Support"/TextMate/Bundles/

If the directory doesn't exist, create it.

Clone the bundle - once you have it, reload your bundles in TextMate and it will appear in the bundles list.

	git clone git://github.com/jackbb/CSS-JackBB.tmbundle.git "CSS-JackBB.tmbundle"

You can easily update the bundle through the TextMate menus by going to *'Bundles -> CSS Vendor Prefixes - Jack BB -> Update Bundle via Git'*.

##Example usage

To add a text shadow, you can write:

	text-shadow: 1px 1px 3px #000;

Simple! now come the tab triggers to add the prefixes. At the end of your line, add a '**`-`**' followed by *TAB*:

	text-shadow: 1px 1px 3px #000;-

followed by *TAB* gives you

	-moz-text-shadow: 1px 1px 3px #000;
	-o-text-shadow: 1px 1px 3px #000;
	-webkit-text-shadow: 1px 1px 3px #000;
	text-shadow: 1px 1px 3px #000;

Only need one prefix? Add the first letter of your prefix to the trigger. For a webkit only prefix, add '**`-w`**' followed by *TAB* to the end of your line.

	transition: all 0.2s ease;-w

followed by *TAB* gives you

	-webkit-transition: all 0.2s ease;
	transition: all 0.2s ease;

Fancy something different? using just '**`-`**' and *TAB* on an empty line gives you

	-moz-
	-o-
	-webkit-
	|
 
Start typing and watch all four lines fill themselves in at the same time.

I personally find these triggers most useful when editing existing code.

	-moz-border-radius: 3px 3px 0px 0px;
	-o-border-radius: 3px 3px 0px 0px;
	-webkit-border-radius: 3px 3px 0px 0px;
	border-radius: 3px 3px 0px 0px;
	
If I need to change a border-radius, it is much quicker to delete the first three lines, make my changes, then use the '**`-`**' trigger:

	border-radius: 5px 5px 2px 2px;-

which returns:
		
	-moz-border-radius: 5px 5px 2px 2px;
	-o-border-radius: 5px 5px 2px 2px;
	-webkit-border-radius: 5px 5px 2px 2px;
	border-radius: 5px 5px 2px 2px;

---

For the moment, I am only using the -moz-, -o-, and -webkit- prefixes. If you need more, it should be fairly easy to duplicate and edit the commands in the bundle editor (or you can ask me to do it!).

I have also intentionally left these triggers out of my main CSS bundle. My reason being that if and when (hopefully) browser prefixes become obsolete, this bundle can be easily deleted.

Enjoy!