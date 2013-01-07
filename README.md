# [jQuery sectionNav][1]

A jQuery plugin to build a sticky navigation of a article’s sections with highlighting while scrolling.

## Usage

### Import

Start by import the script to your page, the best location is in the footer, but no matter what make sure it follows your jquery file.

	<script src=“jquery.sectionNav.min.js”></script>

### Build your page

Include a class or id hook in the element you want to apply the plugin to and include an `<h3>` for each section you want to inlcude in the navigation.

```html
<div class=“main”>
	<article class=“post-article”>
		<h1 class=“post-heading”>This is the main heading for the article</h1>
		<h2 class=“post-sub-headling”>This is a sub-heading for the article</h2>
		<p>Yada yada yada...</p>
		<h3>This is a section heading</h3>
		<p>More yada yada...</p>
		<h3>Another section heading</h3>
		<p>More more yada...</p>
	</article>
</div>
```

### Initialise

Now initialise the plugin with your hook for the article

	$(‘.post-article’).sectionNav();

and the plugin scans the article, grabs all the `<h3>`s, adds them to the navigation list and inserts the list before the article. It’s that easy...well almost.

### Styling

To keep the plugin simple there are no styles added to the navigation, that’s all up to you. The nav structure looks like this and includes class names in [@csswizardry’s][3] [inuit.css][4] framework style:

	<nav class=“section-nav”>
		<span class=“section-nav-heading”>
		<ol class=“section-list”>
			<li class=“section-list-item”>
				<a class=“section-link”>

Check out [this demo][2] to get an idea on what you can do.

## Options

There are a few customizable options in sectionNav besides the element you apply it to using key: value pairs. Here are the defaults.

	$(‘.post-article’).sectionNav({
		sections: ‘h3’, 
		tittleText: ‘Jump To’,
		fixedMargin: 40
	});

### Sections

As mentioned, the script automatically searches for `<h3>`s within the target article. If your page structure differs, feel free to target another element, like a `<h2>` or `<h4>` or even a class, like `.section-headline`.

### Title Text

sectionNav’s default title text is ‘Jump To’, but feel free to change it to whatever works for you, like ‘Article Sections’ or ‘Page Navigation’

### Fixed Margin

This is the `top` dimension you set for the `.section-nav.fixed` class, which is applied as the user scrolls down the page and is removed as they scroll above the article. You definitely want to set this if you don’t use the default 40px, otherwise the nav will jump around as the user scrolls past the top of the article.

## License

sectionNav is released under the [CC Attribution-ShareAlike license][6]. This means you can recreate, edit or share the plugin as long as you maintain the same open licensing.

## Authors

[James Wilson (@jimmynotjim)][7]

With a bit of guidance from [Eric Clemmons (@ericclemmons)][8]

[1]: #
[2]: #
[3]: https://twitter.com/csswizardry
[4]: http://inuitcss.com/
[6]: http://creativecommons.org/licenses/by-sa/3.0/
[7]: http://jimmynotjim.com
[8]: https://github.com/ericclemmons
	
	
	