<!--

- [ ] QUIZ?
- [ ] Lato / Lekton?
- [ ] make sure we're using Chrome

-->

# Web stories day 3

### Today, Saturday 30th of January

1. [Recap](#recap) of what we have learned so far
* [Crash course](#crash-course) in **HTML & CSS** to build an one-page **portfolio**
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


# Crash course

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

- [ ] Here's [all the code for the finished thing]().
- [ ] Animated gif

### Step by step

Go to [thimble.mozilla.org](https://thimble.mozilla.org/) and sign up (it's free). Then log in and click on `Start a project from scratch`.

It's good practice to build the **HTML** first, and then make it _stylish_ with CSS. Aka *content first*.

1. Thimble created an HTML skeleton for us, containing the basic building blocks: `html`, `head` and `body` tags.
* In the `head` we can change the `title`.
* We're dividing our page into sections, so let's create a few empty `section` tags.
	
	```html
	<section></section>
	<section></section>
	<section></section>
	<section></section>
	<section></section>
	``` 
* In the first section we'll add a *heading* and a *sub-heading*. These will be the most important pieces of information in your page.

	```html
	<h1>Your name</h2>
	<h2>Your specialties, eg: film maker</h2>
	```






 
 an image, which could serve as a logo  
  
	```html
	<div class="logo">
		<img src="images/logo.png" alt="Describe this image">
	</div>
	```
* We'll have two sections with textual content, so let's write something in there.  
  
	Copy-paste something appropriate from the Web (using `right-click` > `Inspect Element` and then copying the HTML code for the part(s) you want to use in your page).



- [ ] cropping images and saving them for Web