# Swamp-CodeSyntax #

An SMF package for code syntax highlighting that has been customised for use on
www.theswamp.org

This package is powered by GeSHi -> http://qbnz.com/highlighter/

The original source of this package used (with thanks) is located 
at https://custom.simplemachines.org/mods/index.php?mod=3070
and was created by http://codebirth.com/

## Installation ##
Install this package like any other package in SMF Package Manager.
Download the zip file and upload or provide a url in the specified field and
follow the install prompts.

NOTE: If you are using custom themes please mark the checkboxes at the 
bottom (besides the theme name) to apply the changes where necessary.

## Modifications made for theswamp.org ##
File      |   Modification
----------|------------------------------
db_install.php | added code type keys for drop down list in post editor line 23 -> 'language_selector' values
package-info.xml | small changes to reflect this as a custom package for theswamp.org
Sources/geshi | added cadlisp-7.php file for custom Autolisp syntax
Doc/avlisp/index.html | Added a AutoLisp help refernce file for inline help within the cadlisp-7 code tag.

## Possible Issues ##

### Drop down list items missing: ###
If drop down items updated in db_install.php file are not shown as expected
 you may have to update the database.

To do this log into the database via phpMyAdmin or similar and navigate to
 
\<smf-db-name> -> \<table-prefix>_**themes** -> **geshi_language_selector**

and update the values as required.
The format is a comma separated list of **code-syntax:drop-down-key** pairs 
eg. **cadlisp-7:AutoLisp** where 'AutoLisp' will be displayed in the dropdown.

## Don't like the alternating striped lines? ##
If you don't like the alternating styled lines you can change the styles in the
db_install.php file.
The lines to change are 'geshi_line_style' and 'geshi_line_style_fancy', you
can set the style to:

**padding: 0 5px; background-color: #fff; line-height: 16px; border-left: 1px solid #999; **

If you have already installed the package, use phpMyAdmin per the instructions
above (for editing drop dwon list items) and set the values for the same
variables in that table.
**Note: these changes have been made to the db_install.php file, original lines for
adding the striping are commented out and left for reference.**

## Customizing cb|GeSHi-mod ##

You can customize the appearance of highlighted code for each of your themes by going to Configuration -> Themes and Layout -> Theme Settings and clicking on the theme name. Scroll down and you will see the customizable options.

If you want to customize the active theme just go to _Configuration -> Current_ Theme and scroll down.

### List of customizable options ###

#### GeSHi Code Container ####

For reference please see 3.1 The Code Container.
http://qbnz.com/highlighter/geshi-doc.html#the-code-container


#### Line numbers ####
For reference please see 3.2 Line Numbers.
http://qbnz.com/highlighter/geshi-doc.html#line-numbers


#### Fancy line numbers ####

For reference please see 3.2 Line Numbers.
http://qbnz.com/highlighter/geshi-doc.html#line-numbers


#### Line style ####

For reference please see 3.2.2 Styling Line Numbers.
http://qbnz.com/highlighter/geshi-doc.html#styling-line-numbers


#### Fancy line style ####

For reference please see 3.2.2 Styling Line Numbers.
http://qbnz.com/highlighter/geshi-doc.html#styling-line-numbers


#### Highlighted lines style ####

For reference please see 3.15.2 Styles for the Highlighted Lines.
http://qbnz.com/highlighter/geshi-doc.html#styles-for-highlighted-lines


#### Show header above GeSHi Code Container ####

If enabled, it will show the header specified in the next option.


#### Header above GeSHi Code Container ####

This header is similar to the headers that SMF shows above QUOTE and simple CODE containers when you use those bbc tags in a post. You can do your custom header and there are three keyword available that you can use.

{CODE} is the localized translation of Code for the active language, so if your forum users are using english they will see Code, if they are using spanish they will see Código, and so on...

{TAG} is the bbcode tag for the specified language. If you are highlighting C++ code with the tag code=cpp, it will show CPP

{LANGUAGE} is the full name of the specified programming language. If you are highlighting C++ code with the tag code=cpp, it will show C++


#### Show header inside GeSHi Code Container ####

If enabled, it will show the header specified in the next option.


#### Header inside GeSHi Code Container ####

You can use these keywords. For reference please see 3.12.2 Setting Header Content.
http://qbnz.com/highlighter/geshi-doc.html#setting-header-content


#### Show footer inside GeSHi Code Container ####

If enabled, it will show the footer specified in the next option.


#### Footer inside GeSHi Code Container ####

You can use these keywords. For reference please see 3.12.3 Setting Footer Content.


#### Show language selector ####

If enabled, there will be an additional select box in the text editor you see when posting a message. Since there are +200 programming languages supported and there are only a few that you will use often you can make a list with a set of predefined language that, when selected, will add the corresponding bbcode to the text area of your post.


#### Selectable languages ####

Here you can set the languages that will be available in the language selector. The format to add a new language is code:language_name. Since it would be a tedious task I'm not posting all them here at this moment. You can find a wide list here with their respective code and language name.

So for Visual Basic we'll do vb:Visual Basic and for C++ we'll do cpp:C++ and so on with all the languages you want to be shown in the select box. Separate them by commas and everything will work as expected.

