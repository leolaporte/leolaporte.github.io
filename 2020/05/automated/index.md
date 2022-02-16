# Automating Hugo Posting


I've written a small fish function to automate the creation of a new post on this site.

[Fish](https://fishshell.com) is the shell I use pretty much everywhere (instead of the default `bash` shell on Linux, or `zsh` on macOS). It has a great command language and the ability to create functions that become shell commands. The following code is saved as `.config/fish/functions/newpost.fish`

To create this post I ssh'ed into the server (actually I keep a mosh session always open on most of my computers, including the iPad with a tmux pane dedicated to this purpose) and typed `newpost automated`. This fish function creates a new blank markdown file, opens it in my editor, and then will rebuild the site once I finish editing.

Here's the function...

```fish
function newpost -d "creates a new hugo post with the name supplied in $argv and opens emacs to edit it, upon emacs close rebuilds the site"
	# this is my site's location 
	set -l sitedir "/home/leo/www/leofm/"
	
	# save the current directory
	set -l curdir (pwd)
	
	# move to the web dir (hugo needs to be invoked from here)
	cd $sitedir

	# build the file name using the current year and month as dir, $argv is the argument to the function
	set -l thepost "posts/"(date +%Y-%m)"/"$argv".md"	

	# tell hugo to create a new post
        hugo new $thepost
	# then edit it
	emacsclient -c -a="" "content/"$thepost
	
	# after saving the post, update the site
	hugo

	# and return to the original dir
	cd $curdir
end

```

Thanks to this script, and Hugo, all I need to do to post here is log into the server and type `newpost <postname>`. That's exactly what I've been looking for. 

By the way, Hugo has a ton of interesting templates. This is [Binario](https://themes.gohugo.io/binario/). Like it?

