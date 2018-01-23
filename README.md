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

## Possible Issues ##

### Drop down list items missing: ###
If drop down items updated in db_install.php file are not shown as expected
 you may have to update the database.

To do this log into the database via phpMyAdmin or similar and navigate to
 
\<smf-db-name> -> \<table-prefix>_**themes** -> **geshi_language_selector**

and update the values as required.
The format is a comma separated list of **code-syntax:drop-down-key** pairs 
eg. **cadlisp-7:AutoLisp** where 'AutoLisp' will be displayed in the dropdown.





