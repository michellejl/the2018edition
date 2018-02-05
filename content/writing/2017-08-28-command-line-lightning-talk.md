---
title: "Command Line Lightning Talk"
date: 2017-08-28T14:01:55-08:00
Description: "Last Week at Write/Speak/Code I wrote a lightning talk about Command Line Tricks in which I promised a follow up blog article going into more detail about setting up the customizations I talked about. Here it is."
Tags: []
Categories: []
featuredImg: "/imgs/dragon-friend.png"
---

**Note:** *Slides from this lightning talk and other talks I have written can be found on my [github](https://github.com/michellejl/Talk-Slides/).*

## My Setup:

**Computer/Operating System:**
<br />I do most my development on a Macbook pro that is usually running macOS Sierra. (Sometimes it also runs Windows 10,Linux Ubuntu or Linux Mint). All of the tips in this post are set up on the macOS Sierra part.

**Terminal:**<br />
I have used [iTerm2](https://www.iterm2.com/) since I started on the command line and love it.

**Terminal Customization:**<br />
Color Theme: [For the Fishies](https://github.com/michellejl/Some_Configuration_files/blob/master/iterm/colors/ForTheFishies.itermcolors) is a color theme I customized myself to make everything the way I wanted. I named it "For the Fishies" because I was setting my colors while looking at ASCIIQuarium (Bonus tip at bottom of article!)

**Shell**<br />
I have [OhMyZSH](http://ohmyz.sh/) installed to allow me to use ZSH with some fun customizations.

**OhMyZSH Theme**<br />
I use a customized theme that I built inspired by various other themes I liked bits and pieces of. For all the included screenshots, I am using [amichelle2](https://github.com/michellejl/Some_Configuration_files/blob/master/zsh/themes/amichelle2.zsh-theme). Not a very exciting name, but I added the 'a' to the beginning so it shows up at the top of my themes list, and the 2 at the end after I made dramatic changes from my first theme I built.

**Homebrew**<br />
I use [homebrew](https://brew.sh/) for installing all the things it will let me install.

My github repo: [Some Configuration Files](https://github.com/michellejl/Some_Configuration_files) has more of my config files that I use and want to sync up between home and work computer.

## Tip 1: Set a Friendly Creature Greeting

![Dragon ASCII art greeting when I open the terminal]({{site.baseurl}}/assets/images/dragon-friend.png){: .support-image}

This was one of my earlier customizations. The idea was that the command line is kind of a scary place when you are just getting started and I wanted it to say "hi". I looked into ways of running a script or command automatically at startup and found that was super easy. All you need to do is add a quick line with the command into your .zshrc file (or whichever file you use for your shell customization).

Originally I had a simple line that just used the built in "echo" command to simply print out "Hello Michelle!". Kind of boring. I started looking into other ways to print out things to the console. Eventually I found a program called 'cowsay' which is a program that generates ASCII art cows saying things. As I was looking into it, I found that you can actually generate a number of ASCII creatures, not just cows.

#### Cowsay

* **Installation:** (Using Homebrew)
```shell
$ brew install cowsay
```

* List all available creatures you can use besides standard cow
```shell
$ cowsay -l
```

* More helpful commands and information about cowsay can be found on the [wiki page](https://en.wikipedia.org/wiki/Cowsay);

In the process of finding the cowsay program, I also came across a few other nifty little programs. One of those programs was '[fortune](https://en.wikipedia.org/wiki/Fortune_(Unix))' which I don't use but is kind of fun if you want to check it out. The other one I found was magical. It is called 'lolcat' and it makes all your outputs rainbow.

#### Lolcat

* **Installation:** (Ruby Gem)
```shell
$ gem install lolcat
```

* Lolcat is a super easy program to use, basically you can just pipe any text output into it and rainbow magic happens.

* Take a look at lolcat's [github repo](https://github.com/busyloop/lolcat) for more installation instructions and how-tos.

I use cowsay and lolcat together to generate my magical dragon friend that greets me when I open the terminal. I like to imagine that he is with me on all my terminal journeys to help me as needed.

Code I use to make this actually happen:
```shell
cowsay -f dragon "Greetings, Human!" | lolcat
```
This snippet lives in my .zshrc file. It will slightly slow down the time it takes for your terminal to open. Make sure to restart your terminal after installing these programs and adding your greeting to the profile file to make it work!


## Tip 2: Taming the 'rm' Command

When I first learnt about this command it terrified me. Why was there a command that I could use that could potentially erase everything on my computer?? -insert minor panic attack here- I was so worried I would do it on accident somewhere or somehow type it in on accident. One way I found to control this fear was to use an alias to block me from being able to use the command. **This should not be used as a long term solution!** I used it as training wheels basically to help me think about it more before I would use this command, and to help me feel more comfortable as I was learning my way around.

Using an Alias is a powerful tool that you can use on the command line. Like many command line tools, it is extremely simple, but can do awesome things. It is essentially just a keyboard shortcut/ abbreviation. It is used as a means of avoiding typing a long command sequence over and over and over. (OhMyZSH has some really cool [plugins](https://github.com/robbyrussell/oh-my-zsh/tree/master/plugins) you can enable that have a bunch of built-in alias' set up for various commands. I love all the [git alias'](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugin:git) I have now!)

*One important note when setting up an alias: It is generally not a good idea to define an alias that overrides a built-in command. You might get used to a command doing one thing, then jump on someone else's computer or a server and run that command expecting your changed thing to run only to have the command use the default behavior. This can definitely cause problems.*

## Tip 3: Making Mistakes Better / Dealing with Typos
The command line is intimidating and frustrating already. Typos just make things that much more annoying. I have three programs installed that help me deal with typos.


#### sl

![Example of the sl command]({{site.baseurl}}/assets/images/sl.gif){: .support-image}

One of the most common commands I use on the command line is 'ls' which is used to list out all the folders and files at a specific location. Because I use this command so often, I often type it wrong.

* This program generates an ASCII art steam locomotor.
* **Installation:** (With Homebrew)
```shell
brew install sl
```

#### gti

![Example of the gti command]({{site.baseurl}}/assets/images/gti.gif){: .support-image}

Another command I use all the time is all the 'git' commands. Similar to the 'sl' program, 'gti' creates an ASCII vehical (GTI Car) that zooms across the screen.

* **Installation:** (With Homebrew)
```shell
brew install gti
```


#### thefuck

This one is amazing because it works for basically every typo I have ever made on the command line. It is great for when you get really annoyed, your boss isn't looking, and you just need to curse a bit at the computer. This magnificent program is used to correct your previous console command.

* Checkout the [github repo](https://github.com/nvbn/thefuck) for installation and usage information.

I get so annoyed by the default response! It often even asks you if you meant the thing you actually meant. But you then have to either retype the thing, use the up arrow and then arrow through to the place you need to fix the typo. It is annoying and takes time.

![Example of the default typo response]({{site.baseurl}}/assets/images/typo.png){: .support-image}

TheFuck makes this all better because it allows me to type the response I probably want to say anyways. "fuck"!

![Example of thefuck responses]({{site.baseurl}}/assets/images/typo.gif){: .support-image}

## Final Bonus Tip

This is probably the least useful, but I just really enjoy it. It is a nice thing to look at and calm down when the command line world gets too scary.

##### ASCIIQuarium

* You can install it with
```shell
$ brew install asciiquarium
```
* I have mine set up with an alias, so I just get to say 'fishies' and I get fish!
* More Info: [site](http://www.robobunny.com/projects/asciiquarium/html/) **NOTE:** Don't listen to that site on how to install it on mac. You can just homebrew it!

![Example of ASCIIQuarium]({{site.baseurl}}/assets/images/fishies.gif){: .support-image}

Thanks for reading!