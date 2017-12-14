# A crash course on Wordpres

So, you want to get that side-hustle on and learn how to make small client websites. If you 
don't have previous skill programming, and learning would honestly take up too much time that
you do not have, then Wordpress is for you.

## What is Wordpress?

Wordpress is a blogging engine. It sits on top of a web server like apache and provides all of
the looks and brains of a website. Coding something in HTML or CSS can give you a website to,
but Wordpress makes this a lot easier for you, and provides a cms.

A cms is a _content management system_ and is super important. Wordpress's version of this is 
Wordpress Admin, which makes up 99% of what you will be working with. Wordpress Admin allows
you to create web pages within the website, and change how the content looks. For example: if
you had `www.mywebsite.com` and wanted to add an about page at `www.mywebsite.com/about`, you
would add it through the wordpress admin. This isn't even the most important part of wordpress
admin, though. The most important part is _saving you time with clients_. Your time is valuable,
so when you get paid to build a website, you are using that time wisely (hopefully). What wastes
your time is clients coming back to you every time they want to update their blog, because there
is no way they would pay you every time for this. Wordpress admin allows you to give clients
access to a website in a way they understand, so that they can _manage their own content_.

## How do I build a website with Wordpress?

Let us start from the beginning and work our way up

### Tools

You don't need many unless you are working in theme development (more on that later). There are
some common tools that you may need though. 

The first tool is an __FTP Client__. You may be doing most of your work from WP Admin, but sometimes
you just want to push an image file or something to the webserver fast. An FTP Client allows you
to connect to the wordpress server manually for when you really need it, although if your theme is 
good enough then you shouldn't have to do this. Always make sure to configure your connection to use
sftp instead of ftp, so you can be secure.

Recommended clients:
* [filezilla](https://filezilla-project.org/): The classic. It can do anything and run anywhere. Watch out for annoying freeware though, I have been burned in the past when I didn't read the installation screens and accidentally installed annoying crap.
* [winscp](https://winscp.net/eng/download.php): It's ugly, but it is crazy fast. It is incredibly reliable but it is windows-only. I recommend it over filezilla
* [cyberduck](https://cyberduck.io): very reliable and multiplatform. I recommend it over filezilla for OSX.

The second tool that will be extremely helpful is a __Text Editor__. The literal swiss army knife of 
programming tools, you may need to use one to fix something that is randomly broken, or modify something
for whatever cooky website you are building. Please note that a Document Editor like Microsoft Word or 
Notepad is _not_ a text editor. Do not use it to edit code! Stuff like word will not only display code 
almost unreadably poorly, but saving code from it may add formatting that breaks everything.

I, like most dwellers of programming communities, am incredibly opinionated over what editor is the absolute 
best (so take my advice with a grain of salt). I live and breath vim, but the learning curve is a tad
high for that and you likely want a GUI. My current favorite is [Github Atom](https://atom.io/). The plugin
system is spectacular so any tool you could need is in there (even ftp clients if you are an all-in-one
kind of person), and it is so darn comfy that typing in it is a dream. Download it and open this readme
in it, you will see just how nice it feels.

Note: other clients include [sublime text](https://www.sublimetext.com/), [vscode](https://code.visualstudio.com/), [brackets](http://brackets.io/), and [lightroom](http://lighttable.com/).

### Hosting

You need to have your website reachable by the world, and your hosting provider is what allows you to do that.
There seems to be an infinite amount of hosting sites to choose from, but in reality there are very few.
Actually, there is just one: [godaddy](https://www.godaddy.com/). Most programmers will be quick to argue
against godaddy, but _programmers are not your customers, normal f*kin people are_. Godaddy is the easiest
website to use to __transition ownership__. You are _not_ trying to maintain a website forever for next to 
no pay, you are trying to crank out the website in a couple days and offload it onto the client for _them_ 
to manage. For a typical client, you are gonna buy a month of wordpress webhosting (which you can even convince
the client to pay for), build the website, and then transfer ownership of the godaddy account to the client.
That's your flow, and you can just point them to godaddy support if they ever have questions about website 
performance. Speaking of which, Godaddy's online support is spectacular too, I could honestly just bullshit 
with the support agents online on their website chat box for hours. They are that nice. It's unreal.

There is a problem though, godaddy is not free. Despite that, I still encourage you to spend the $7 and 
get [a month of webhosting](https://www.godaddy.com/hosting/wordpress-hosting), because you are gonna be 
using them a lot and it helps to get a head start on understanding how godaddy webhosting works. You can
even [buy a domain for it too](https://www.godaddy.com/domains) and godaddy will connect everything for 
you pretty easily. Its good to learn that flow as well because likely clients will want a snazzy domain
for their new website. 

If you are really stingy, you can make a free account at [pantheon](https://pantheon.io/) and mess around
there. They are more difficult to explain, but if you check out their [spectacular documentation](https://pantheon.io/docs/),
you can probably make your way around the account when learning wordpress. They are more for theme developers
and established agencies though. I use pantheon every day, but I still would have a hard time explaining
the site and transferring ownership to average mom-and-pop shops trying to buy a website.

### Themes

The literal most important thing about being a wordpress dev is the theme. When you buy wordpress hosting
from godaddy, it has a base install of a generic wordpress website. Taking that base install and applying
unique styles and features is what the theme does. It provides website-building tools to build nearly 
any shape or look of a website. You can get a theme in one of two ways:

#### Build one

You do not want to do this. This requires actually learning how to code PHP, which is a bit too much for
the client contract size you are gunning for. The learning curve is way higher, and if you are just starting
out then this can be a skill to shoot for that you learn further down on the job.

#### Buy one

You want to do this. There are a variety of themes out there and they range in price. Your theme is your
bread and butter, and I recommend you try out a bunch before settling on one that feels comfortable. Most
themes come with drag-and-drop editors for building websites. Look at videos of the theme to get an idea of what it feels like.
What you are mainly looking for is speed of development and capabilities. A great test for this when 
trying out a theme is to take [a](https://modpizza.com/) [generic](https://www.greatharvest.com/) 
[website](http://www.vapology101.com/) and see how fast and accurately you can replicate it with your 
theme. Most themes come with default example websites built in and these are great for starting off.

If you are looking for a theme ready to use, [Avada](https://avada.theme-fusion.com/). It is the top-selling
theme of all time. Yes it is paid, but most good ones are, and even then the free trial will be enough for you
to try it out and see if you can work with it. I think avada is like $40 but you get a license that you can use
with an unlimited amount of sites. If you want to see what else is out there, check out [themeforest](https://themeforest.net/),
it has a rediculous amount of themes in it. You will most definitely find a tool that fits your needs there.

### Learn it

When you have a running, hosted wordpress instance try this exercise:
1. find a website that is similar to ones you want to build
2. install your theme onto the wordpress server and find a default preset that looks closest to what you are rebuilding
3. explore wordpress admin and look at how every page is configured through the theme
4. perform modifications to the pages to match the ones on the website you are copying
5. add or remove pages, build new ones, anything that gives that spit and polish to your website.

For help with #2, the theme should come with documentation that helps you through this. If it doesn't, 
then check the online documentation for the theme. If both of these do not work, you need to swap themes 
to one that doesn't suck. If #4 is giving you problems, look more in depth at the docs, and drop the theme
if it is still giving you problems. If you have difficulty with #5, then you did not spend enough time on #4.
When you want to try again, or try building a different website, wipe out the theme to a clean slate and try
again from #1.

If you can do this easily and quickly, it is about time to build a portfolio. Use the skills in the exercise,
and build a website that represents you: a guy that builds websites. Buy a domain on godaddy that is catchy,
start writing a blog on your wordpress site, make sure it pops up nicely in google ([all in one seo can help](https://wordpress.org/plugins/all-in-one-seo-pack/)),
and start handing out your business card to locals.

[and](https://www.elegantthemes.com/blog/tips-tricks/how-to-effectively-market-your-freelance-wordpress-business) 
[market](https://mattreport.com/marketing-wordpress-developer-tonya-mork/) 
[yourself](http://wern-ancheta.com/blog/2015/01/31/how-to-market-yourself-as-a-developer/)
