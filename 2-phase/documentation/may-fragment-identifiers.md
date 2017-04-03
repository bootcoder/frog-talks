# Fragment identifiers

A **fragment identifier** is a short string of characters in a URL that refers to a resource that is a subordinate of another resource. It is often named to indicate what the subresource is.

URLs can end with an optional hash symbol; the fragment identifier goes after the hash symbol. In a URL where there is no fragment identifier after the hash symbol, the browser points to the top of the page.

Example:

```https://en.wikipedia.org/wiki/Bobblehead#Promotional_merchandise_by_American_corporations```

In this case ```Promotional_merchandise_by_American_corporations``` is the fragment identifier and directs the user to the promotional merchandise section of the Wikipedia page on bobbleheads.

Fragment identifiers work on the client side only. When an agent requests a resource from the server it only sends the URI, not the fragment. Because of this a fragment doesn't reload a page but does update the browser's history.

## Common uses:
- Used with AJAX to emulate the back button
- Used on pages where there are sections written in JS to create linkable URLs
- Can pass information to scripts, for example telling a YouTube video to begin playing at a specific time
