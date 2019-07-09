---
layout: post
title:  "The Jekyll Patience Test"
---

_WARNING: The following post is long._

I debated whether or not I should make this into a blog post, but how interesting is this blog going to be if I don't post my struggles? 

I had one hell of a time trying to get Jekyll installed and running on my Mac. This blog was very nearly a Wordpress one, if I hadn't taken a step back to breathe and try it again. There were just so many issues that no one had warned me I would have run into. Starting with getting my computer to understand that I had updated Ruby correctly.

As far as I knew I was doing everything right. I went to `https://jekyllrb.com`, pulled up their [Step-by-Step Tutorial](https://jekyllrb.com/docs/step-by-step/01-setup/), and was determined to follow everything to the letter despite my nervousness with the terminal. I opened their [installation guide for Mac](https://jekyllrb.com/docs/installation/macos/), installed Ruby and Ruby Gems without issue, and everything looked like I was ready to start installing Jekyll. Except...

For reasons beyond me my Macbook did not understand I had installed Ruby. I ran the correct command, and then when I typed `ruby -v` out came the outdated Ruby version I had supposedly replaced. I type `brew install ruby` only to be told I already had the latest version installed, a version that `ruby -v` did not display. Immediately I was at a loss. How do you fix this?

Luckily my CTO and friend was more than eager to help. He was the one who recommended I start a blog with Jekyll, after all. After work we sat down, I told him about my issue, and he nodded his head sagely. "Yep, makes complete sense you got stuck. This sort of issue is kind of archaic. What we'll need to do is..."

And in a flurry of new tabs and terminal commands I wasn't wholly familiar with he explained what was going on. He opened an invisible file that needed editing, explained why, and bamn. In minutes everything was working perfectly. Convinced that I would be ready to start working on my blog without issue I promptly closed everything, shut down my laptop, and readied myself to once again tackle the Jekyll tutorial fresh in the morning.

My computer had other plans.

The minute I opened up my terminal again and tried to run `gem install jekyll`, I ran into a **brand new** issue. I didn't have permissions to run the Jekyll installation. My heart sank. 

_What do I do now? Do I ask him for help again? Is this another legit concern? Am I just going to keep relying on him to fix all my issues?_ 

No, damn it. This time...I'll fix the issue _myself_. 

This is where I fell into what I can only call a blackhole of trial and error. I typed my error into Google, pulled up an article I think would help me. Did it work? Nope. Back to Google. Repeat. I'm not really sure what came over me. I just had a feeling that I could not have been the only dummy to have this issue, and some other dummy braver than I out there must have asked for a solution to this publicly on some forum post, and _damn it_ I will find that post of it kills me.

To make a half-hour of furiously searching and typing short, most of all my answers were found on Jekyll's own [troubleshooting documentation](https://jekyllrb.com/docs/troubleshooting/#configuration-problems) I discovered an invisible file, one I remember my CTO friend talking about the evening prior. A file called the `.bashrc` file. In it I just had to put some lines of text the Jekyll installation documentation talks about. I did this using Nano, which gave me its own hiccup when it wouldn't let me save or exit out of the text file (turns out that Nano would only let me save and exit if my cursor was on the last line of the file). I close the terminal window completely and open it back up to refresh it, just as the documentation recommends, and then...

Nope, still not working.

This is where I learned my first lesson about troubleshooting. If the documentation gives you more than one way to do something, and one of those ways doesn't work, **try the other thing**. To me it was kind of illogical. Closing and reopening the terminal window didn't do anything. Why would typing `. .bashrc` work? "Whatever, I'll try it," I say to myself, rolling my eyes.

**Boom**. It works. I laugh outloud to the empty office. How narrowly I just dodged leaping into another Google search blackhole that would have probably lead me nowhere. What a relief.

The rest from there is smooth sailing. Then what happens next leads to the second lesson I learn about troubleshooting. **Never make changes in a panic.**

I decide, for whatever reason, to change the name of the repository the Jekyll site is located. I do this from Github's site, not the terminal window. Suddenly the next commit I push, which just contains a harmless sentence, breaks the entire site. 

I start to freak out a little. 

I look up the issue I'm having, I try to change the location of where I'm pushing my changes to through the terminal window. Okay, good...seems like it works... Except the site still looks broken. Maybe it needs me to push some changes so the location switch takes affect?

I push a new commit that adds in a random sentence. Nothing changes, the site's still broken. 

I push a new commit that undoes what I just wrote. Nothing changes.

I start trying to push more changes. Still nothing.

I Google how to revert changes and I try to revert to the branch before I made the changes. Still. Broken.

At this point, against my better judgment, I let my panic take over and I search and type in a flurry of commands that I think that will revert the changes. Somehow this ends up completely deleting the Jekyll site folder's contents _from my own computer_. I have no idea how I did that. Looking through my past commands gives me no hint at how to change it back. I close everything down in defeat. 

So close to victory, only to have the rug pulled out from under me. _What do I do now? Do I start over?_

I get up, use the restroom, take a sip of water, sit back down at my laptop.

_Fuck it, we're starting over!_

I delete the shell of a folder containing no files, I delete the repository from Github, and start over from the very beginning. 

I am made to face the exact same issues that I started out with. Not having permission to install Jekyll, not having the `.bashrc` file changes stick... I get a little scared, but take a deep breath, re-find the sites that I used before to fix the issues, and get past it again.

I install Jekyll with a repository name I won't want to change later. And before I know it, everything is up and working exactly as I needed it to. I faced my past issues and got it all done faster than before! And yet I don't feel victorious, rather I feel a mix of relief and failure. 

My third lesson of troubleshooting. **If I'm stuck on something serious, don't be afraid to ask for help.** 

While I definitely should have not made any of the changes in a panic, I'm sure that if I had just consulted a more experience dev for help they would have been able to help me actually revert my changes. I probably wouldn't have had to restart the entire process over, as valuable of a learning experience as that was.

I think this last lesson is especially important for me to consider if I plan to work as a dev in a company. When working with other people's code, I'm not going to have the luxury of being able to erase everything I did and start over. All the code I write will be part of a living, breathing codebase composed of other developers constantly adding to it. Panicking and making rash decisions, and restarting from the beginning, won't always be something I can do. So even though I got away with it this time, next time I'll just ask for help again.

I'd rather deal with the embarrassment of asking a dumb question then the dread of putting myself in a spot I can't come back from. 