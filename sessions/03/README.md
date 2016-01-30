<!--

- [ ] Embed videos
- [ ] QUIZ?
- [ ] Lato / Lekton?
- [ ] make sure we're using Chrome.
- [ ] Animated gif

-->

# Web stories day 3

You can find this tutorial is online at **bit.ly/web-stories-day-3**.

### Today, Saturday 30th of January

1. [Recap](#recap) of what we have learned so far
* [Crash course](#html--css-crash-course) in **HTML & CSS** to build an one-page **portfolio**
* **Publish** your portfolio online


# Recap 

<!--

Tell them what you've told them

-->

### What have we learned so far?

* **Ingredients** of stories: time/place markers, events, surprise, feelings
* **Structure** of stories: Freytag's pyramid, linear vs non-linear
* Played with an interactive storytelling tool: **Twine**
* Began using **HTML** 

### What are we doing today?

We think we have a better idea of where you are right now. You are putting together your portfolios and in the next few days / weeks many of you have interviews.

So the aims of today are:

* Organise your work to **tell the story** of your projects
* Start building an **online one-page portfolio** for your work
* Learn **HTML & CSS**
* **Publish and host** your portfolio online

Bringing storytelling and coding together to make something that is useful to you, today.

<!-- 
* as a creative, you'll be telling the story of your work and your process for the rest of your working life 
* is there a jump in the story of your process (remember story lines?)
-->


# HTML & CSS crash course

We're going to learn how to:

* Write HTML to **structure** your content 
	* Create several types of **text** (paragraphs, headings, quotes)
	* Create **links** to other Web pages (eg: your blog)
	* Add **images** (eg: of your work)
	* **Embed** other media (eg: YouTube videos, tweets etc.)
	 
* Write CSS to **style** your content
	* Design your page's **typography**
	* Set your page's **colours**
	* Get images to fill up the whole browser's window, without loosing their original aspect ratio
	* Position elements in the horizontal and vertical centre of the page
	* Create a *curtain reveal* effect

The **demo** is at [j.mp/html-css-portfolio-demo](http://j.mp/html-css-portfolio-demo). Click `Remix` to reveal all its **source code**.

## Step by step

Go to [thimble.mozilla.org](https://thimble.mozilla.org/) and sign up (it's free). 

Then log in and click on `Start a project from scratch`.

### 1. Content first

It's good practice to build the **HTML** first, and then make it _stylish_ with CSS. Aka *content first*.

#### HTML skeleton

Thimble created an HTML skeleton for us, containing the basic **building blocks**: `html`, `head` and `body` tags.

Every HTML document, at the bare bones, needs to have this structure

```html
<!doctype html>
<html>
	<head>
		...
	</head>
	<body>
		...
	</body>
</html>	
```

#### Head

In the `head` we can change the `title`.  
	
Later, we'll add links to external resources like *stylesheets* and *meta* information.

What you put in the `head` is not visible in the page.

#### Body

We're dividing our page into sections, so let's create a few empty `section` tags inside the `body`.
	
```html
<section></section>
<section></section>
<section></section>
<section></section>
<section></section>
``` 

#### Headings

In the first section we'll add a `div`. Inside that, we'll add a **heading** (`h1`) and a **sub-heading** (`h2`). These will be the most important pieces of information in your page.

```html
<section>
	<div>
		<h1>Your name</h2>
		<h2>Your specialties, eg: film maker</h2>
	</div>
</section>
```

#### Images

In that same `div`, underneath the headings, we can add an **image** which could serve as a logo or a profile picture. 
  
```html	
<img src="profilepic.jpg" alt="Describe this image">
```

#### Text

We'll have two sections with **textual content**, so let's write something in there.  
	
```html
<section>
	<p>Write something here to introduce your project and the ideas behind it.</p>
	<p>A little information about the process you took from research through to the development.</p>
	<p>You process is important!</p>
</section>
```

`p` is for *paragraph*.

#### Hyperlinks

We can add **hyperlinks** to our content using the `a` element (`a` is for *anchor*).
	
```html
<a href="http://example.com">the clickable text</a>
```

For instance:
```html
<section>
	<p>Influenced by the playful approaches to image-making used by Dadaist <a href="http://www.whitechapelgallery.org/exhibitions/hannah-hoch/">Hannah Höch</a>, I gathered a collection of portraits (Vogue portraits from the 1920's-40's and more current artist portraits) to create a collage of anonymous parts.</p>
</section>
```

#### Contact details

Let's add our **contact details** to the final section.
 
```html
<section>
	<div>
		<h2>Say hello!</h2>
		<p>aimeebethmj@gmail.com</p>
	</div>	
</section>
```

### 2. Style later

Now the fun part: **CSS**!

#### Normalize

We want to tell the browser not to mess with our style.   
  
So we're going to use a little CSS utility called [**normalize.css**](https://necolas.github.io/normalize.css/), which resets the default browser's stylesheet and provides a consistent common ground to base our own styles. 

Search `normalize.css` in Google and click on the first link. 

Click download and save the file by going to *File* and *Save page as*.

Now upload that file to Thimble.

Let's include a `link` in the `head`, which will point to the `normalize.css` file.  
 
```html
<link rel="stylesheet" href="normalize.css">
```

#### Our style

As you can see, `normalize.css` has flattened our page. Now we can start building our own style. 

There's a `link` in our `head` which points to another CSS file called **style.css**. This is where we add our custom styles.

```html
<link rel="stylesheet" href="css/style.css">
```

#### Typography

We are going start with **typography**. 
	
We can grab a **font** from [Google Fonts](https://www.google.com/fonts): pick a typeface you like and then grab the `link` code for it and paste it in your page's head. 

Where? Between `normalize.css` and  `style.css`

```html
<link href='https://fonts.googleapis.com/css?family=Source+Code+Pro:400,300,700,900' rel='stylesheet' type='text/css'>
```

Let's give some ground rules to our page, by applying them to the `body` element. Then we can set the rules for headings, paragraphs and bold elements.

```css
body
{
	font-family: 'Lato', sans-serif;
}
```

#### Readability

To center the content sections and make them easier to read, we add `class="content"` to all the `section` elements that contain text in HTML.

Then in CSS we create a rule for those `section` elements *classified* as `content`. 


```css
.content 
{
	margin: 2rem auto;
	max-width: 40rem;
	padding: 0 1rem;
}
```

`.` is a shortcut for `class`.

#### Full-size

Let's work on the **full-size images**.   
  
First we want to get some `section` elements in our page to take the full browser height. So we create a `.full` class and give it a `height: 100%;` property.

```css
.full
{
	height: 100%;
}
```

This is not enough though. 

It is important to understand what `height: 100%;`means: _the full height of the parent element_. It doesn't magically mean *the height of the browser window*. So if you want your main container to have the height of the browser window, setting `height: 100%;` isn’t enough.

_Why?_ Because the parent of your `section` (`body`) has its height set by default to `auto`, which means it is sized according to its _content_. You can try adding `height: 100%;` to the `body` element to see… it is still not enough.

_Why?_ Because the parent of `body` (`html`) has also its height set by default to `auto`. Now what if you try to add `height: 100%;` to the `html` element? It works!

```css
html, body
{
	height: 100%;	
}
```

#### Background images

Now onto the **images**. We're going to use `background-image` to define a few images that will be applied to the background of our `.full` elements. 

We are going to add our `background-image` directly into our HTML. For each `section` with the class `.full` add in `style="background-image: url('image.jpg')"`

For example:
```html
<section class="full" style="background-image: url('image.jpg')">
	<div>
		<h1>Your name</h2>
		<h2>Your specialties, eg: film maker</h2>
		<img src="profilepic.jpg" alt="Describe this image">
	</div>
</section>
```

By default background-images *tile*, but we want them to take up the whole available screen space, without losing their aspect ratio (no squashing). 

We can achieve that with `background-size`. This property can take various values: pixel sizes, percentages, and then a couple of interesting keywords. 

* `contain` will scale the image so as to be as large as possible providing that it is **contained** within the background positioning area. 
* `cover` instead, will scale the image, this time to be as large as possible so that the background positioning area is completely **covered** by the background image.

We're going to add `background-size: cover;` to the `.full` rule (so that it will apply to all sections with the `full` class).
```css
.full
{
	height: 100%;
 		background-size: cover;
}
```

#### Image sizes

Next we're styling the **logo** or **profile picture**.

By default images will be added to the top-left corner of their *parent*.

If we want it to be centred, we need CSS. 

Let's give the `img` a class `profile`.
```html
<img class="profile" src="profilepic.jpg" alt="Describe this image">
```

We can set a height and width for our image
```css
.profile 
{
	height: 10rem;
	width: 10rem;
}
```

We also can make sure that the `img` is not bigger than its container

```css
.profile 
{
	height: 10rem;
	width: 10rem;
	max-width: 100%;
}
```

#### Aligning stuff
	
To center the image, we create two classes `h-centred` and `v-centred`.

```css
.h-centred
{
	display: flex;
	justify-content: center;
}
v-centred
{
	display: flex;
	align-items: center;
}
```

Let's add them to our HTML `section`.

```html
<section class="full h-centred v-centred" style="background-image: url('image.jpg')">
	<div>
		<h1>Your name</h2>
		<h2>Your specialties, eg: film maker</h2>
		<img class="profile" src="profilepic.jpg" alt="Describe this image">
	</div>
</section>
```

We can see the `div` has moved into the centre of the screen, but the content inside it is still aligned to the left. Let's add some CSS to fix that. Add some style into the `div`.

```html
<div style="text-align: center">
	<h1>Your name</h2>
	<h2>Your specialties, eg: film maker</h2>
	<img class="profile" src="profilepic.jpg" alt="Describe this image">
</div>
```

#### Scrolling effect

Now we want to get the **curtain reveal effect**, so that instead of scrolling with the rest of the page, the background-images will be revealed as we scroll up and down. That makes our page more interesting.

We can achieve this with another CSS property, `background-attachment`. With this property we have two options: 

* `scroll` (default): the background image will scroll with the rest of the content.
* `fixed`: the background image will remain stationary as the rest of the content is scrolled

Which one do we want? Obviously `fixed`.

Add `background-attachment: fixed;` to `.full`

```css
.full
{
	height: 100%;
 		background-size: cover;
 		background-attachment: fixed;
}
```

This **demo** is at [j.mp/html-css-portfolio-demo](http://j.mp/html-css-portfolio-demo). Click `Remix` to reveal all its **source code**.	



<!--- [ ] cropping images and saving them for Web-->