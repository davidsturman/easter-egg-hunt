# easter-egg-hunt
A simple Javascript file to provide the mechanism for an Easter Egg hunt on your website.
In this case, Easter eggs are clickable images (or other clickable elements) that people can search for and collect.
The code uses a cookie to keep track of what eggs a person has collected and how long it took them to collect all the eggs.

The script has no dependancies.
Released under the MIT license.

## Instructions:
* The only file you need is egghunt.js. The other files are for demonstrating how it works.
*  Include egghunt.js on any page on which you put Easter eggs.\
 ``` <script src="egghunt.js"></script> ``` \
 You can use any clickable element (such as images) for eggs.
* Give easter eggs class="egghunt" and onclick="egghunt.record(1)"
    where the number 1 is replaced with a unique number for
     each egg starting at 0. Make sure you don't skip any numbers.\
     Example:\
       ``` <img src="egg.png" class="egghunt" onclick="egghunt.record(0)"> ```
*  Fill in the total number of eggs into the "neggs" variable
*  Fill in the URL for the "success" page into "success" variable

* If you want to display the time it took to find all the eggs
    on a "success" page, then create a \<div\> or a \<span\> with id="eggscore".
    The script will fill that div or span with text like "10 minutes and 3 seconds"\
    Example:\
      ```<div>It took you <span id=eggscore></span></div>```\
    will become\
       "It took you 10 minutes and 3 seconds"

* Note: Easter Egg scores are kept in an cookie called "eehr".


