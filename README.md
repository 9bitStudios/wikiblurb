Wikiblurb.js
=========

A jQuery Plugin for Wikipedia and Other Wikis. All you have to do is call it on an element and Wikiblurb will populate that element with data from a wiki...

```javascript
<script type="text/javascript">
$(document).ready(function(){
    
    $('#article').wikiblurb();
    
    $('#otherWikiArticle').wikiblurb({
	      wikiURL: "http://fallout.wikia.com/",
	      apiPath: '',
	      section: 0,
	      page: 'Fallout',
	      removeLinks: false,	    
	      type: 'text',
	      customSelector: ''
    });
    
});
</script>
```

### Options

Below is a listing of options your can set....

| Option | Value | Default Value | Description | Example |
| --- | --- | --- | --- | --- |
| wikiURL | String | "http://en.wikipedia.org/" | The base URL of the wiki you want to get data from with trailing slash included | wikiURL: "http://fallout.wikia.com/" |
| apiPath | String | "w" | Any additional path needed to be added to properly get data from the API (no slashes). Wikipedia uses "w" but often this will be an empty string for other wikis. | wikiURL: "" |
| page | String | "Jimi_Hendrix" | The name of the wiki page. | page: "Brazil" |
| section | Integer | 0 | The section of the wiki you want to get data from. | section: 4 |
| removeLinks | Boolean | false | Setting this option to true will return just text data and will not have any links present. | removeLinks: true |
| type | String | "all" | Possible values are "text", "blurb", "infobox", and "custom" | type: "infobox" |
| customSelector | String | "" | If the type setting is set to "custom", then this is the selector that Wikiblurb will look for | customSelector: ".mw-class" |
