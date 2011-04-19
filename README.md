##Introduction

This bundle contains commands to make handling CSS3 vendor prefixes a little bit easier.

Instead of adding prefixes to all standard snippets, this bundle allows you to code using the non prefixed versions of your CSS, then add the prefixes afterwards.

##Installation

In Terminal, navigate to the TextMate bundles folder.

	cd ~/Library/"Application Support"/TextMate/Bundles/

If the directory doesn't exist, create it.

Clone the bundle - once you have it, reload your bundles in TextMate and it will appear in the bundles list.

	git clone git://github.com/jackbb/CSSVendorPrefixes-JackBB.tmbundle.git "CSSVendorPrefixes-JackBB.tmbundle"

You can easily update the bundle through the TextMate menus by going to *'Bundles -> CSS Vendor Prefixes - Jack BB -> Update Bundle via Git'*.

##Example usage

To add a text shadow, you can write:

	text-shadow: 1px 1px 3px #000;

Simple! now come the tab triggers to add the prefixes. At the end of your line, add a '**`-`**' followed by *TAB*:

	text-shadow: 1px 1px 3px #000;-

followed by *TAB* gives you

	-webkit-text-shadow: 1px 1px 3px #000;
	   -moz-text-shadow: 1px 1px 3px #000;
	     -o-text-shadow: 1px 1px 3px #000;
	        text-shadow: 1px 1px 3px #000;

Only need one prefix? Add the first letter of your prefix to the trigger. For a webkit only prefix, add '**`-w`**' followed by *TAB* to the end of your line.

	transition: all 0.2s ease;-w

followed by *TAB* gives you

	-webkit-transition: all 0.2s ease;
	        transition: all 0.2s ease;

Fancy something different? using just '**`-`**' and *TAB* on an empty line gives you

	-webkit-
	   -moz-
	     -o-
	        |
 
Start typing and watch all four lines fill themselves in at the same time.

If you aren't a fan of the indented syntax, use '**`--`**' instead of '**`-`**' (e.g. '**`--w`**') to format the prefixes without indentation.

	text-shadow: 1px 1px 3px #000;--

followed by *TAB* gives you

	-webkit-text-shadow: 1px 1px 3px #000;
	-moz-text-shadow: 1px 1px 3px #000;
	-o-text-shadow: 1px 1px 3px #000;
	text-shadow: 1px 1px 3px #000;

---

For the moment, I am only using the -moz-, -o-, and -webkit- prefixes. If you need more, it should be fairly easy to duplicate and edit the commands in the bundle editor (or you can ask me to do it!).

I have also intentionally left these triggers out of my main CSS bundle. My reason being that if and when (hopefully) browser prefixes become obsolete, this bundle can be easily deleted.

Enjoy!