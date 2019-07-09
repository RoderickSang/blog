---
layout: post
title: Adding My Site's Header Image
---

I completed my site's navigation bar and admittedly that took much longer to make than I thought it would. Writing your own code without a tutorial to follow really will humble you. But since I made it with Flexbox, at least it looks nicely spaced and is responsive! 

![Here's a link to a gif to show what that looks like.](https://i.imgur.com/XehdTQM.gif) 

There isn't much to see, but I'd be lying if I said I wasn't proud of it. 

After getting this to work, I knew the next thing I wanted was some sort of header image. I've seen sites call it a "hero" image, but I'm not sure why. Is the size of the image heroic in some way? _Maybe one day I'll have my answer..._

Regardless, I spent a large amount of time trying to decide if I wanted this image to be a normal `<img>` HTML tag or a background image added in through CSS. They both seemed the same, aesthetically. 

I tried making it work with the background CSS property, but the image didn't want to appear at all. I assumed it was because the container I was trying to place the image into wasn't filled with content, so there was nothing for the background image to show up under. I struggled with this for a few more minutes before deciding just to test if the image would show up fine as an HTML `<img>` tag. It did!

![A screenshot of the image appearing under the navigation bar.](https://i.imgur.com/4khDvWo.png)

I never really expected adding a header image to be a great learning experience, since it seems so simple. Follow any tutorial you want on creating a landing page or some sort of profile page and it'll look very intuitive. In fact it'll take the teacher no more than a few minutes, usually. But writing the thing yourself is definitely a humbling experience. Especially when you decide you want to place text over the image.

I decided that over the image I wanted the words "Web Developer" to show up in white. I also wanted the words to look nice and big. Centering it over the image wasn't too much of a problem. The issue was placing it over the image while having it be responsive.

This was probably the largest sticking point I had when putting this together. I couldn't manage to figure out how to get the text to show up directly centered ontop of the image while also being responsive to any screen size. I must have been using the wrong Google search terms because nothing was showing up that made any sense. Somehow the easiest way to get this working looked like it would be by using LESS. I was apprehensive to use LESS since this seemed like a very small usecase to justify throwing in an entire CSS extension which I probably wouldn't use for the rest of the website.

This is where the fact that I was trying to create this in the morning before work came in handy. For in my time of need walks into the office a front end developer. And one that I'm already friendly with, no less! I told him of my struggle, and right away he goes, "Have you tried using VW?"

"What?" I say. "VW?"

Turns out there's a whole type of CSS unit that I wasn't even aware of! I toyed around with VW units for just a few minutes and boom.

![A short gif of the text appearing perfectly over the image and showing its responsiveness.](https://i.imgur.com/QqGpHGv.gif)

I may have celebrated a tad early, however, since now I have a new issue.

![A screenshot showing there's a whole column of whitespace on the side of my site.](https://i.imgur.com/F4EBljB.png)

Hopefully this won't be _too_ much of an ordeal to fix. But even if it is, I'm kind of confident now that I'll be able to find a solution. Eventually. Maybe with a little help from my friends.