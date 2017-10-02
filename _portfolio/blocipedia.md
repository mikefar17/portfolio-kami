---
layout: post
title: BlocJams-Angular
thumbnail-path: "img/angular-icon-vector.png"
short-description: BlocJams is able to play music from a libray using AngularJS. 
---
---

{:.center}
![]({{ site.baseurl }}/img/AngularLogo.png)

{% highlight javascript %}
<table class="album-view-song-list">
        <tr class="album-view-song-item" ng-mouseover="hovered = true" ng-mouseleave="hovered = false" ng-repeat="song in album.albumData.songs">
            <td class="song-item-number">
                <span ng-show="!hovered && !song.playing">{{ $index + 1 }}</span>
                <a class="album-song-button" ng-show="hovered && !song.playing" ng-click="album.songPlayer.play(song)"><span class="ion-play"></span></a>
                <a class="album-song-button" ng-show="song.playing" ng-click="album.songPlayer.pause(song)"><span class="ion-pause"></span></a>
            </td>
            <td class="song-item-title">{{ song.title }}</td>
            <td class="song-item-duration">{{ song.duration | timecode }}</td>
        </tr>
</table>
{% endhighlight %}

## Explanation

Translating the project BlocJams into AngularJS was definetely a journey. I had to learn the different concepts behind AngularJS and how they differed from pure vanilla JavaScript. Using modules, directives, controllers and services was an interesting experience. All the information thrown at you from different directions and even more interesting how all this information worked together to form a single page application. 

## Problem

Figuring out how the dynamic works between directives, services, and controllers was chanllenging. Since every type js file has a certain functionality. My challenge was deciphering the difference between the functionality of each part of the app. For example, in my project app fixture.js serves as container for an object which holds the information that is passed used for in this specific for information of an album. This 

## Solution

The solution to this problem wasn't a really a simple answer. It was more like experimenting and learning what each js file did. For example, directives such as ng-show and ng-mouseover which had to be defined by on the view in HTML like in the example above. This is only one of the many lessons I had to learn. 

## Results


> Bacon ipsum dolor amet filet mignon meatball spare ribs fatback bacon shankle. Kielbasa andouille fatback salami, boudin bresaola pig alcatra turkey spare ribs jerky. Corned beef bresaola leberkas salami alcatra beef landjaeger venison shank bacon meatloaf beef ribs picanha. Leberkas sausage brisket porchetta shankle prosciutto chicken picanha kielbasa pig kevin t-bone turducken filet mignon jowl.

## Conclusion

I definately learned a powerful lesson. Being able to undestand and manipulate different technologies will definitely be a useful skill out in the field. And, will allow me to create a range of different variaty type of projects. 

