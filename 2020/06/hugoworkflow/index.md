# My New Hugo Workflow

This site is a laboratory. In particular, I've been seeking a friction-free way to write. I think I've found it.

<!--more-->
<img src="/images/lab.jpg" align="right" alt="Leo in his lab (from the cover of Leo Laporte's 2003 Technology Almanac)" padding="20px">  I've long wanted to be able to blog as easily as one would tweet. Most content management systems put up a number of roadblocks. If it's a struggle to post, however little, I'm less likely to do it. 

I know I'm an edge case here. As a broadcaster there's zero friction to speaking my mind. I sit in front of a mic, form a thought, make some mouth noises, done. 

<i class="fas fa-brain"></i>    <i class="fas fa-long-arrow-alt-right"></i>    <i class="fas fa-head-side-cough"></i>    <i class="fas fa-long-arrow-alt-right"></i>    <i class="fas fa-microphone"></i>    <i class="fas fa-long-arrow-alt-right"></i>    <i class="fas fa-users"></i>

Writing is a much more painstaking process, and even though I've done a lot of it, it's always felt like labor. I listen to writers do podcasts (I'm listening to [Jon Gruber's Talk Show from WWDC](https://daringfireball.net/thetalkshow/2020/06/24/ep-286) right now, for example) and I can feel how much harder it is for them to talk than write. Sometimes I can even hear them re-writing their words before they speak. I probably should do that more often, but I generally speak quickly and with little to no editing. To each his own but that’s my preferred way to create content. And how I’ve made my living for more than 40 years. 

But I do want to write. There are lots of reasons to put pen to paper. Writing forces a more thoughtful pace, requires more rigorous reasoning, and is the best way to develop complex ideas. It's also more permanent, and, potentially, begs a more thoughtful response from readers. And, once I'm done, writing is more deeply satisfying. That makes sense. The more effort one puts into doing something, the more satisfying the sense of accomplishment will be when done. 

>"I don’t like to write, but like having written."
> -- Frank Norris

Writing is so much work for me that I don't want to add any friction via the mechanics of posting what I've written. Ideally I'd fire up an editor, write something, save it, and it would magically appear as a post. I think that's one reason Twitter is so successful. But... it's also why Twitter is so full of ephemeral crap -- it's *too* easy. Twitter combines the worst of both worlds: thoughtless posting with a permanent record. That combo has bitten most of us over time. So I guess I don't want to make it *that* easy. There should be enough friction to encourage thoughtful writing. That's where the text editor comes in. Once I'm looking at all that blank real-estate on my screen I feel the need to fill it. There's no jotting and posting here. I'm in writing mode. 

For a while I used Manton Reece's [micro.blog](https://micro.blog/), *“the fastest way to blog”*. But it’s too fast. Like Twitter it encourages short off-the-cuff posts - and I wanted to encourage my monkey mind to work on longer pieces (like this). Also, after long experience, I've learned it's best to host my own content. I want my stuff to live on *my* server, and to live in a form that's easy to backup and move around (like, say, plaintext + markdown).

So, my shopping list for a blog includes:
1. Mostly friction-less posting
2. Write anywhere: iPad, Mac, Linux
3. Pick up writing anywhere else
4. Self-hosted
5. Clean, portable content
6. Clean, attractive presentation

I believe I’ve found all of the above here. My workflow at leo.fm varies, but over time it has evolved to the following. 

Hugo is running on my server with -w to watch for changes in the content folder[^1]

[^1]:  For some reason this sometimes results in missing pieces. I believe that’s because hugo in watch mode wants to use the “staging” rules not the “production” rules. This even though I explicitly set hugo_env to production when I run it. Still, some of the plug-ins I use, like mermaid and mapbox don’t always get rendered. Oddly comments do, so it’s a puzzle. The quick fix is to ssh in and do a command-line rebuild and everything reappears.

I mount my web site locally using [sshfs](https://github.com/libfuse/sshfs) on all my machines, so I can create and edit posts on my local machines. When that file is saved or updated, hugo rebuilds the site instantly, and the post is up. You can’t get simpler than Ctrl-S to post.[^2]

[^2]: Saving doesn’t always mean publishing, however. hugo supports YAML compiler directives in the header of every post. One of the directives, draft, let’s me publish a post or keep working on it. Another directive specifies publish date. If that’s in the future, hugo will wait to publish the post. 

This is an wonderfully flexible workflow. That’s another requirement of friction-free posting, it has to work wherever I am. 

There are a number of ways I can create and edit posts. I’ve used emacs on the server for many posts. I like [Panic’s Code Editor](https://panic.com/code-editor/) for the iPad, too. Its support for ssh, sftp, and editing makes the iPad a perfect way to work on the site. I actually started this post on my iPad using Code Editor[^3] but I’m finishing it on my Mac using the absolutely wonderful [Typora](https://typora.io/) (Mac/Windows/Linux). This really is the perfect writing tool for any purpose, but for blogging it’s the best markdown editor I’ve ever used, it even supports the automatic upload of image files. And it’s clean and beautiful - the ideal writing tool. 

[^3]: I’m keeping an eye out for Panic’s new Macintosh editor, Nova. It’s possible it will replace Typora, but I bet it will be more useful for coding than writing. 

I started this post on the iPad using Code Editor while eating breakfast. Now, after lunch, I’m finishing it on my iMac in my office. I’ll probably edit it later on my Linux laptop while in bed. It’s all the same file, which lives on the server at TWiT, but I have many ways to access it. Perfect. Now to change draft to false and post. 

{{< typeit >}}See ma, no friction!{{< /typeit >}}

