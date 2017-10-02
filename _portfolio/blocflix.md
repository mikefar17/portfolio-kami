---
layout: post
title: BlocJams-JavaScript
thumbnail-path: "img/bloc_jams.png"
short-description: BlocJams is able to play music from a libray using pure vanilla JavaScript. 
---

{:.center}
![]({{ site.baseurl }}/img/bloc_jams.png)

{% highlight javascript %}
var setSong = function(songNumber){
   if(currentSoundFile) {
       currentSoundFile.stop();
   }
    
   currentlyPlayingSongNumber = parseInt(songNumber);
   currentSongFromAlbum = currentAlbum.songs[songNumber - 1];
    //#1
    currentSoundFile = new buzz.sound(currentSongFromAlbum.audioUrl, {
    //#2
        formats: ['mp3'],
        preload: true
    });
    
    setVolume(currentVolume);
};
{% endhighlight %}

## Explanation

I'm new to Web Development, so for me, to be able to use a tool such as Buzz(a Javascript HTML5 Audio library) is really exiciting. Being able to integrate libraries into my projects and to see a project come one step closer to life, well, it just warms my heart. BlocJams was my first project using vanilla JavaScript.

## Problem

I think my problem with this section of code was understanding the concept behind setting a value of a variable from one value and then switching that same variable to a different value in order to get the result desired. I had this preconceived notion that once a variable was given a value, that value was set in stone and was unable to change. Straying away from this notion was hard for me to do. In this example, "currentSoundFile" was previously declared with a value of null(var currentSoundFile = null) in the glbal scope. However, in the declared function "setSong", currentSoundFile is "redeclared", in a sense, in order to use the buzz library.  

## Solution

Understanding the versatility of declared variables is very important. Variables can hold many values and the value executed depends on the value given to it by the developer at a specific scope. Understanding the concept behind the code and erradication preconceived notions is essential.

## Results

As a result, I was able to set a song by using the Buzz Library as a new object. I would be over simplifying if I said that that this was the only step which made the project interactive, however, it was facinating to be able to use a tool such as the buzz library.  

## Conclusion

In conclusion, I understood a very important lesson for coding that I will transcend into my other projects. I'm sure that using tools like this will become a very useful skill. 
