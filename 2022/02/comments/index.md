# A New Commenting System

I've been using a third-party commenting system here, [Commento](https://commento.io). But I think it's time to make a change.
<!--more-->
Commento is well supported by my blog engine, Hugo. It's relatively inexpensive with a good set of features, but.... this is such a low volume blog that I don't think it's worth the $5/month for Commento. That's no reflection on it - it's a nice system. But I like the idea of the Fediverse and I'd like to support the Mastodon instance I run, [twit.social](https://twit.social). 

It turns out it's pretty easy to use Mastodon comments with Hugo. I found a great [post by Carl Schwan](https://carlschwan.eu/2020/12/29/adding-comments-to-your-static-blog-with-mastodon/) that included the code to insert in my theme. A simple copy and paste and - wow!- it worked! I modified the default header to include a link to twit.social. The only trick is to quickly edit the post metadata to point to the toot announcing the post. So it's not automatic, but it's not hard either. I'm hoping that this will facilitate conversation on posts here, and, not incidentally, drive some traffic on Mastodon. 

Thanks, Carl. To try it out - press "Reply" below and it will open a Mastodon form in your browser. Your comment will appear here and on your Mastodon account. If you don't have a Mastodon account, join us at [twit.social](https://twit.social). We'd love to have you!

UPDAYE: Well for some reason that's not working at all. Sigh. I'll keep banging on it. I love the idea of creating a conversation about posts on Mastodon, especially since I'm already running my own instance. Ironically one of the replies to this post was a complaint about my facetious cookie banner. Without Commento.io there are no cookies, so I'm turning that off too.

Finally, I had it half working using Carl's code, but I did need to get some Javascript, purify.min.js, accesible. Carl uses it to sanitize HTML in comments. I stuck that dang code everywhere, but finally put it in /static/assets/js/ and lo and behold, it works! I still have a lot to learn about Hugo. Per Carl, I am using his "Load Comments" button to keep from hammering the Mastodon server. So have at it! 

