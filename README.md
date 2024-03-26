# [GindaChen Blog](https://gindachen.github.io)


## How to install



Useful script when in trouble of git submodule:
```bash
# Delete the submodule entry from .gitmodules file:
# [submodule "path/to/submodule"]
#     path = path/to/submodule
#     url = https://github.com/user/repo.git

# Stage the .gitmodules changes:
git add .gitmodules

# Delete the submodule entry from `.git/config`

# Remove submodule files from working tree and index. 
# Note: this has not removed your local version.
git rm --cached path/to/submodule

# Optionally, remove your local submodule files:
rm -rf path/to/submodule

# Commit the changes:
git commit -m "Removed submodule <name>"


# Add submodule
git submodule add --depth=1 https://github.com/GindaChen/hugo-PaperModX.git themes/PaperModX
git submodule update --init --recursive # needed when you reclone your repo (submodules may not get cloned automatically)
```



Disque comment service:
```html
<div id="disqus_thread"></div>
<script>
    /**
    *  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR PLATFORM OR CMS.
    *  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: https://disqus.com/admin/universalcode/#configuration-variables    */
    /*
    var disqus_config = function () {
    this.page.url = PAGE_URL;  // Replace PAGE_URL with your page's canonical URL variable
    this.page.identifier = PAGE_IDENTIFIER; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
    };
    */
    (function() { // DON'T EDIT BELOW THIS LINE
    var d = document, s = d.createElement('script');
    s.src = 'https://gindachen.disqus.com/embed.js';
    s.setAttribute('data-timestamp', +new Date());
    (d.head || d.body).appendChild(s);
    })();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
```

```html
<script id="dsq-count-scr" src="//gindachen.disqus.com/count.js" async></script>
```