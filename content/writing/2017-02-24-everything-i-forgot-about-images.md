---
title: "Everything I Forgot About Images"
date: 2017-02-24T11:45:30-08:00
Description: "I went to a great talk this week where the speaker, Jessica Tate, reminded me about a lot of best practices for using image on the web that I seem to have forgotten about as of late."
Tags: []
Categories: []
featuredImg: "/imgs/images-for-web.jpg"
---

I went to a great talk this week where the speaker, [Jessica Tate](https://twitter.com/missjessicatate), reminded me about a lot of best practices for using image on the web that I seem to have forgotten about as of late. She took a subject I have always found boring and a little annoying and made it interesting and relevant. She was an engaging speaker.

I know I studied all the things about images for both print and web when I attended art school, and for a while I was pretty good about always optimizing my images for web. But at some point, I seem to have just gotten bored of it and figured 'oh well” and ignored the whole subject. Side effect: I have a photography site that takes forever and a half to load because I am squishing images more than 5000px wide into little itty bitty 250px wide thumbnails. So I wanted to gather some of the things she went over in a blog post here to remind myself of the importance of optimizing images for web. Something to remind me the next time I decide to ignore it.

### Image File Formats

There are four main types of image file formats that are used today: jpg, png, gif, svg. Svg is definitely the new and exciting one, but it can not replace everything. Knowing what all the different options and file types exist for images isn’t enough, but it is a good start.

1. **jpg** <br />
Stands for Joint Photographic Experts Group. This type of file should be used for high quality, full color photography. Keep in mind, jpgs do use lossy compression, so don’t go crazy with the editing and saving. Every time you save it as a jpg it will lose some quality. It is better to save a RAW or Photoshop document version of the image for edits and use that to update and create a new jpg every time you need to change it.

1. **png** <br />
Stands for Portable Network Graphics. There are two main types of png that are used: png-8 and png-24. Both types support transparency, but png-24 handles it better. A png-8 will only include 256 colors, and is good for clipart and simple graphics with low amounts of color. On the other hand, png-24 can support any number of colors and is the best option if you need a full color photo or graphic with transparency. It does tend to make for a large file.

1. **gif** <br />
Stands for Graphic Interchange Format. Gifs support transparency like pngs, but only supports 256 colors like the png-8. Gif isn’t generally recommended anymore, but it still has its place. Mostly for when you want (silly) animations.

1. **svg** <br />
The newest member of the image file types, svg stands for Scalable Vector Graphics. This file type allows you to create images that are infinitely scalable. The image is created using vectors and can be edited on the fly with code in some pretty cool ways. Animation is also possible with this image type and can be manipulated in a variety of ways through the code. Often this is a good choice for icons and graphics like social media icons. Font Awesome and other symbols as font services can be useful for this, but svg gives you more freedom and will scale better than these fonts.

### Rules for Saving Images for Web

These are directly taken from Jessica’s talk. I’ve known the different file types and generally what they were each used for, but that doesn’t mean I have always made good choices when saving out images. These seem so basic, but at the same time they are so important, I just have to share her rules.

1. **Save the correct file type** <br />
Know the different types and what they do best. Make smart choices.

1. **Save at the correct size** <br />
This isn’t talking about file size, but rather about dimensions. Think about what the largest size you would display the image as and make that the largest you would save the file. Monitors are only so big, and at a certain point, continuing to scale the image with the larger monitors only makes so much sense. Often times 2000px is larger than you will ever display an image (even a hero) so don’t over do things. You don’t need that giant 5000px wide image. Save that for the print world and scale down for the web! You can also save different sizes of the image to use for different breakpoints if you want to get fancy with it.

1. **Use Pixels!** <br />
I came to web from a print graphics world, so I am definitely guilty of trying to size everything with the wrong measuring tool. We use pixels on the web (not inches!) so size your image with pixels.

Following these rules and using a tool like Photoshop’s Save for Web, will help keep your file sizes small and your image quality good. When you are done, your images should each be about 150k or smaller.

### Wrap up
Although she covered additional topics, these rules were my main take away. And now I know what I am going to be doing this weekend: going back over projects and getting all the images optimized correctly.

Thank you to [Jessica Tate](https://twitter.com/missjessicatate) for giving this talk, and to the meet up group [Front End PDX](https://www.meetup.com/Front-End-PDX/) for putting on the talk. Jessica’s slides from the talk can be found [here](https://drive.google.com/file/d/0B7VNh2WG2rWKRHp3TXJTZkZFeG8/view). For additional reading, I recommend the same link she has in her slides: [The Myth of DPI](https://www.webdesignerdepot.com/2010/02/the-myth-of-dpi/).
