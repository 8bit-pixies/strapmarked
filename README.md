# Strapmarked

Okay, so [Strapdown](https://github.com/arturadib/strapdown) hasn't been updated in over 5 years, so its effectively dead (right?). In that case what are our options? Can we still generate beautiful documents by writing markdown directly in HTML?

Yes of course! The answer is actually fairly straightforward:

*  Use [marked](https://github.com/markedjs/marked) to handle the markdown parsing
*  Use any drop css framework for styling the page. You can [view a selection here](https://github.com/markedjs/marked). 

What does this look like? The html page could be:

```
<link rel="stylesheet" href="path/to/*.css">

<div id="content"></div>
<xmp id="marked"></xmp>
<script src="https://cdn.jsdelivr.net/npm/marked/marked.min.js"></script>
<script>
document.getElementById('content').innerHTML = marked(document.getElementById('marked').innerHTML);
document.getElementById('marked').style.display = 'none';
</script>
```

And that's it! with 8 lines of boilerplate code, you've essentially got your strapdown alternative!

*  [Example file](https://github.com/chappers/strapmarked/blob/master/index.html)
*  [Live demo](https://chappers.github.io/strapmarked/)

Credit to [Marked](https://github.com/markedjs/marked) for Markdown parser and [dohliam/dropin-minimal-css](https://github.com/dohliam/dropin-minimal-css) for the css picker.

