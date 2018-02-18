# Michelle's Portfolio: 2018 Edition

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">My #goal for 2018 is going to be to keep the same portfolio site for a  whole year without any major stack changes or complete redesigns. 
#impossible #FrontEndDev #goalsfor2018 #NewYearResolutions</p>&mdash; Michelle Levine 🚀 (@MichelleJLevine) <a href="https://twitter.com/MichelleJLevine/status/946519473942511618?ref_src=twsrc%5Etfw">December 28, 2017</a></blockquote>

## Thoughts
I've created way too many versions of my portfolio since I bought my first url in 2011, and none of them have lived more than maybe 8 months top. I've spent pretty much all of January thinking about what went wrong with all the past attempts. I spent time poking at different options before landing here. I spent a lot of January writing and then throwing out code as I tried out different things and decided they didn't work the way I wanted.

This is still a very early version, but hopefully one that I can expand on.

Once I settled on using a static site generator, [Hugo](http://gohugo.io/) found it's way to the top spot mostly because it doesn't default to a blog setting like many of the other static site generators. Hugo gives more flexibility in how you want to build the site. That same flexibility that drew me to Hugo has been making development slower. 

Using [forestry.io](https://forestry.io) as my CMS was crazy easy to set up, and that ease is more than making up for some of my struggles with Hugo. Forestry is managing my automation for me, by added webhooks to my git repo that allows me to create and publish a new build for my site simply by pushing to master!

# Build / Deployment Notes
Running project locally for localdev:
```
 hugo server --watch --verbose --disableFastRender
```

Build out static files for uploading:
``` 
hugo
```
- or - forestry.io is currently set up as my CMS and has some fancy webhooks set up now. Pushing to master branch will trigger a new build/deployment.
