# Unique Filenames in Page Bundles


Now that I've switched to the new LoveIt template I noticed something worrisome.
<!--more-->
I *was* organizing my posts by month folders, but it looks like LoveIt uses Hugo's [page bundles](https://gohugo.io/content-management/page-bundles/) which means that each post ends up in its own directory (using the filename of the source file) in the root of the public folder.

Does that mean that every post I ever write will have to have a unique name? Maybe Hugo has a way to solve this, but just in case I've re-written my newpost.fish function to append the current UNIX time in seconds to the filename so it's unique. So the source file for this post, for example, is bundles1590002452.md.

I'm still going to put the source files in the month folder. So, for example:

{{< mermaid >}}
graph LR;
A["content/"] --> B["posts/"] 
B --> C["2020-05/"] 
C --> D[bundles15900002452.md] 
{{< /mermaid >}}

is transformed by Hugo into the static files in the public folder

{{< mermaid >}}
graph LR;
A["public/"] --> B["posts/"] 
B --> C["2020-05/"]
C --> D["bundles15900002452/"]
D --> E[index.html]
{{< /mermaid >}}

here's the new fish function code:

```fish
        ...
	set -l thepost "post/"(date +%Y-%m)"/"$argv(date +%s)".md"
```

**Update:** After further exploration I've realized that hugo can use permalinks of the year-month form (check out the url of this post) and that I can organize the content folders that way, too. I no longer have to use crazy unique filenames. I only need to make sure a post filename is unique in any given month. So here's the new (and I hope final) fish code to create a new post:

```fish
    ...

	# build the file name using the current year and month as dirs, $argv is the argument to the function
    # this generates a string like "posts/2020/05/mypost.md"
	set -l thepost "posts/"(date +%Y)"/"(date +%m)"/"$argv".md"
    ...
    
```


