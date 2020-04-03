# easter-egg-hunt
A simple Javascript file to provide the mechanism for an Easter Egg hunt on your website.
In this case, Easter eggs are clickable images (or other clickable elements) that people can search for and collect.
The code uses a cookie to keep track of what eggs a person has collected and how long it took them to collect all the eggs.

The script has no dependancies.\
Released under the MIT license.

## Instructions:
* The only file you need is egghunt.js. The other files are for demonstrating how it works.
*  Include egghunt.js on any page on which you put Easter eggs.\
 ```<script src="egghunt.js"></script>``` \
 * Set the total number of eggs and the URL for the "success" page
 by calling egghunt.set(number_of_eggs, url).\
 For an example with 10 eggs:\
 ```<script>egghunt.set(10, "success.html")</script>```
 
* You can use any clickable element (such as images) for eggs.\
  Give easter eggs class="egghunt" and onclick="egghunt.record(1)"
    where the number 1 is replaced with a unique number for
    each egg starting at 0. Make sure you don't skip any numbers.\
     Example:\
       ```<img src="egg.png" class="egghunt" onclick="egghunt.record(0)">```\
     Use the class to make eggs invisible before Easter and then visible on Easter.

* The code keeps track of how long it took to someone to find all the eggs.
  This is called the score.\
   There are several ways to find out someone's score.
   1. The success page will be passed a parameter called SQF_BUNNIES
     (compatible with SquareSpace). It is an encoded version of the number
     of milliseconds it took for the person to find all the eggs.\
      Example:\
       Your success page will be called with\
       ```http://www.domain.com/success?SQF_BUNNIES=DMTQ1ODkz```\
    This can be decoded with ```egghunt.decode()```.\
       ```egghunt.decode("DMTQ1ODkz")``` will return 145893 (2 min 26 seconds)\
   2. The javascript will automatically put the score in a page element with id="eggscore".\
      Example:\
         ```<div>It took you <span id=eggscore></span></div>```\
      will become\
       It took you 10 minutes and 3 seconds

* Note: Easter Egg scores are kept in an cookie called "eehr".


