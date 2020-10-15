# jQuery Tags Input Plugin

Do you use tags to organize content on your site?
This plugin will turn your boring tag list into a
magical input that turns each tag into a style-able
object with its own delete link. The plugin handles
all the data - your form just sees a comma-delimited
list of tags!

[View Demo](http://xoxco.com/projects/code/tagsinput/)

Created by [XOXCO](http://xoxco.com)

Updated by [maito](https://twitter.com/maito)

## Instructions

First, add the Javascript and CSS files to your <head> tag:

```html
<link rel="stylesheet" type="text/css" href="jquery.tagsinput.css" />
<script src="jquery.tagsinput.js"></script>
```

Create a real input in your form that will contain a comma-separated list of
tags. You can put any default or existing tags in the value attribute, and
they'll be handled properly.

```html
<input name="tags" id="tags" value="foo,bar,baz" />
```

Then, simply call the tagsInput function on any field that should be treated as a list of tags.

```javascript
$('#tags').tagsInput();
```

## Properties


| Parameter | Type | Default | Description |
----|----|----|----
| autocomplete_url | string | undefined | If you want to use jQuery.autocomplete, you can pass in a parameter with the autocomplete url. |
| autocomplete | object | {selectFirst: false } | If you're using the bassistance jQuery.autocomplete, which takes extra parameters, you can also send in options to the autocomplete plugin, as described here. `autocomplete:{selectFirst:true,width:'100px',autoFill:true}` |
| height | string | '100px' | tag height |
| width | string | '300px' | tag width |
| interactive | bool | true | active or disactive interactive |
| defaultText | string | 'add a tag' | default tag text |
| removeWithBackspace | bool | true | active or disactive remove tag with backspace |
| delimiter | array or string | ',' | delimiter |
| minChars | number | 0 | min charcters |
| maxChars | number | undefined | max charcters |
| placeholderColor | string | '#666666' | placeholder color |
| onBeforeAddTag | function | undefined | Before add tag, called this function with tag name. Need to return true or false. If return false, not add tag. |
| onAfterAddTag | function | undefined | After add tag, called this function with tag name. |
| onBeforeRemoveTag | function | undefined | Before remove tag, called this function with tag name. Need to return true or false. If return false, not remove tag. |
| onAfterRemoveTag | function | undefined | After remove tag, called this function with tag name. |
| onChange | function | undefined | After add or remove tag, called this function with tag name. |


## Methods


| Method | arg | Description |
----|----|----
| $('#tags').addTag(tagName) | tagName:string | add tag |
| $('#tags').removeTag(tagName) | tagName:string | remove tag |
| $('#tags').importTags(tagNames) | tagNames:string | Add tags ex) 'foo,bar,baz'. If reset tags , set `$('#tags').importTags('')` |
| $('#tags').tagExist(tagName) | tagName:string | check if a tag exists |
