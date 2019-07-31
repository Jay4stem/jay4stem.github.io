### JavaScript - Web application development
## What is HTML?
Now, what is HTML? HTML stands for HyperText Markup Language.

It’s a way of displaying information on web pages in your browser.

One thing to remember is that HTML isn’t itself a programming language. It’s a markup language. Programming languages like PHP or Java use things like logic and conditions to control the content.

HTML doesn’t do those things, but it’s still extremely important. It makes up every single website in existence, after all!

Loading an HTML file in your browser
You can actually create an HTML file on your computer, and load it in your browser. It won’t be on the internet, so only your local computer can view it.

For real websites that anyone can access on the internet, the HTML files are stored on computers called servers. But the basic process is pretty similar.

To create your HTML file:

Go to your desktop or wherever you want to put the file.
Then right click and select “New” and “Text Document.” Make sure that the filename reads “index.html” and doesn’t end in “.txt.”
(If for some reason you can’t see the file extension, click on the “View” tab and make sure that the “File name extensions” checkbox is checked.)
When you have your file all set, you’ll want to open it in your browser.
If it has a Chrome or other browser icon on the left, that means you can double click to automatically open it. If it doesn’t, right-click and then select “Open with” and choose your favorite browser.
In the browser, everything will look blank, which is fine because the file doesn’t have anything in it yet.
Editing the file
Now that you have your file set up, you’re ready to start coding!

To edit your HTML file you’ll want to open it in a code editor. Right click the file, and either select “Open with” and the editor, or some editors will have a quick link from the menu.

You can use other programs like:

- Notepad++
- Sublime
- Atom
- Brackets

Now that you have the index file open in both your browser and your editor, we’ll start writing some code!

## HTML Tags
Let’s look at some of the basic features of HTML.

HTML is made up of tags.

Tags are special text that you use to mark up, or distinguish, parts of your web page. Hence the hypertext “markup” language.

These tags tell the browser to display whatever is inside the tag in a specific way.

Here’s one example of a tag in action:
```html
This is my very first website and I’m <b>extremely excited!!!!!</b>
You can see that the words “extremely excited” are in these <b> tags– “b” is for bold.
```

All right! You just wrote some HTML. Feel excited yet? 🙂

## Anatomy of an HTML tag
Let’s look at the tag again.

The tag before the phrase is called the opening tag — <b>

And the tag after the phrase is the closing tag —  </b>. You can see that the closing tag has a forward slash before the “b.”

Together, these two tags tell the browser to make whatever text is between them bold. And that’s exactly what’s happened.

Now maybe this is obvious, but when the browser loads the HTML, the tags themselves are invisible– they don’t show up on the page.

Pretty cool, eh? One reason I love making websites so much is that it’s almost like magic, being able to make things appear in your browser.

## Basic structure of an HTML document
Now, that line of text that we wrote is working because we saved the file as an HTML file that your browser can recognize.

But for real HTML on the internet, we need to add some more tags to the file in order for everything to work properly.

## Doctype and HTML tags
The very first tag you need is the doctype tag. It’s not exactly an HTML tag, but it tells the browser that this is an HTML5 document.

Here’s what it looks like: <!DOCTYPE html>

This tag doesn’t require a closing tag because it’s not surrounding any text, it’s just declaring that this is HTML.

Other doctypes that were used in the past are HTML 4 or XHTML. But right now HTML 5 is really the only doctype used.

After the doctype, you have an HTML tag. This one tells the web browser that everything inside it is HTML:
```html
<!DOCTYPE html>
<html>
 
</html>
```
I know, it seems a bit redundant since you already used the HTML doctype tag. But this tag ensures that everything inside it will inherit some necessary characteristics of HTML.

## Head and Body sections
Inside the main HTML tag, your content will usually be separated into two sections: the Head and the Body.

Here’s what that will look like in the code:
```html
<!DOCTYPE html>
<html>
   <head>

   </head>
   <body>

   </body>
</html>
```
The head tag contains information about the website and it’s also where you load CSS and JavaScript files. We won’t be covering those today, but just so you know.

The body tag is the main content in the web page. Everything that you see on the page will usually be in the body tag. So we need to move that sentence we made at the beginning into the body.

Here’s what that should look like:
```html
<body>
   This is my very first website and I'm <b>extremely excited!!!!!!</b>
</body>
```
When you reload the page in your browser, everything should look exactly the same as before.

Now let’s go into some of the basic tags that are commonly used in the head and in the body.

I’m not going to go through every single possible tag in existence, because there are more than a hundred. And that would take forever.

We’ll just be looking at the ones used most often, so that you can get a better idea of how an HTML page is put together.

# Basic Head Tags
## Meta Tags
The first tag that should be in your head is this meta tag. This sets the character encoding.
```html
<meta charset="utf-8">
```
UTF-8 is a type of Unicode encoding used in virtually all websites around the world. We need encoding because we need to translate the letters, numbers, and symbols that we use into bytes used by computers.

You can think of it as a sort of dictionary, translating human languages into computer-speak.

The next meta tag that should be on all websites is this viewport tag:
```html
<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
```
This one is important for responsive websites. Responsive means that the website can display properly on all devices– computers, tablets, and mobile phones.

The content in this tag is saying that it should make the width of the website the same width as whatever the device is that is viewing it.

For example, a mobile phone has a much smaller screen resolution, or size, as a laptop computer. This will let the website resize itself according to what the user is using.

The initial scale sets the zoom of the website. On browsers nowadays you can zoom in and out, making the website look bigger or smaller. We want it to be set at 1 by default, meaning not zoomed in or out.

## Title Tag
Aside from meta tags, one of the most important tags is the title tag:
```html
<title>My First Website</title>
```
As you can probably guess, this sets the title of the web page. If a website has different pages, each page may have its own title.

Once you’ve added all these tags into your code, this what the head tag should look like:
```html
<head>
   <meta charset="utf-8">
   <meta name="viewport" content="width=device-width, initial-scale=1">
   <title>My First Website</title>
</head>
```

## Basic Body Tags
Let’s look at the fun stuff now– the body tags control the content that you actually get to see.

Most of the basic body tags are based on things you could do in Word documents. You can create headlines, bold text, make lists, and even tables.

In the days before CSS, using these tags helped to organize and stylize your content so that it would be more easily understood by your reader.

Not all of these tags are still used as much as they used to be. Some of them aren’t needed anymore because we can now use CSS to achieve the same style.

But I think it’s still helpful to at least know what these basic tags are.

## Header Tags
Let’s look first at the headline or header tags, designated with the letter H. Each H tag also has a number after the H. They range from ``` <h1> to <h6>.```

The  ```<h1>``` tag is the highest in priority. It’s generally used for the title of the page.

We’re going to add an  ```<h1>``` tag to our web page. Inside the tag we will put the title of the webpage, My First Website.

We’ll also add a subtitle using the  ```<h2>``` tag, with the content: “An HTML Playground.”

And just for kicks, let’s add in the rest of the H tags, up to ```<h6>```.

So your body tag will look something like this:
```html
<body>
   <h1>My First Website</h1>
   <h2>An HTML Playground</h2>
   <h3>An HTML Playground</h3>
   <h4>An HTML Playground</h4>
   <h5>An HTML Playground</h5>
   <h6>An HTML Playground</h6>
</body>
```

You can see how the font sizes get progressively smaller from  ```<h1> to <h6>```.

Most websites don’t use all the H tags. Usually they will use  ```<h1>``` for the title,  ```<h2> for subtitle, and  <h3> ```sometimes for section titles. It’s pretty rare to use  ```<h4> through <h6>```.

## Paragraph
The next tag we’re gonna look at is the paragraph, or  <p> tag. Just like in Word, you can use paragraphs to separate your content into blocks. You can create a paragraph by surrounding your content with the <p> tags.

We’re going to make a paragraph with some placeholder text.

One of the easiest ways to find placeholder text is to Google for “lorem ipsum.” This is one site that I use pretty often.

Lorem ipsum text is nonsense Latin words that are used in publishing and design to fill in text in order to work on the layout.

So we’ll copy this paragraph here and put it into our code, inside a <p> tag. Let’s make a second paragraph too. We’ll copy some more text and put it into a second <p> tag.
    
```html
<p>
   Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
   Nullam facilisis arcu vel mollis finibus. Nunc facilisis 
   vel nisl lacinia cursus. Cras suscipit augue sed volutpat 
   tincidunt. Aenean dictum tincidunt urna, quis eleifend 
   quam mattis eu. Integer sollicitudin, nisl faucibus aliquam 
   ullamcorper, metus sapien scelerisque lorem, at ornare dui 
   orci non orci. Integer tempus consectetur metus, vitae 
   blandit nibh aliquam nec. Pellentesque vestibulum arcu eget 
   ante sollicitudin, id accumsan dui molestie. Suspendisse 
   vehicula semper dui id congue. Suspendisse sed velit sit 
   amet velit luctus varius. Ut condimentum tincidunt consequat. 
   Sed eu ligula non magna scelerisque auctor.
</p>

<p>
   Maecenas feugiat iaculis imperdiet. Duis vitae pellentesque 
   nunc, eget elementum metus. Nulla sollicitudin bibendum nibh, 
   sit amet semper tortor. Nunc rhoncus non arcu in scelerisque. 
   Donec magna mauris, congue ac dignissim rutrum, tincidunt 
   quis leo. Maecenas dictum orci in magna iaculis, in elementum 
   felis viverra. Aenean sit amet sapien odio. Donec molestie 
   est et nisl mattis dictum. Nullam at nibh aliquet, tincidunt 
   lorem et, facilisis enim. Praesent id felis sit amet quam 
   dignissim volutpat. Nam nec cursus mi, quis tincidunt justo.
</p>
```

And there we have it. The browser automatically adds some space between the paragraphs and other content:

## Line Break
Now, if you want to separate your content onto multiple lines, but you don’t want that space that comes with a paragraph, you can use a line break, or a <br> tag.

Let’s get some more lorem ipsum text and put it into our editor.

Now one thing to note about HTML is that it won’t automatically break lines.

If you press enter a couple of times in your content, nothing different will happen on the page. The same goes for hitting spacebar a bunch of times.

The browser will just give one space and that’s it. In order to create a line break, You need to add a <br> tag.

You can even add multiple line breaks to add more space in your content.
```html
Fusce sit amet rutrum lacus.<br><br><br><br><br/>
Sed efficitur laoreet nisl,ac faucibus velit hendrerit sit amet. 
Phasellus ac orci eget nisi porta accumsan a eget ex. Nam lacinia 
dolor at mi tristique rhoncus.Maecenas nisl est, rhoncus id cursus 
non, tempor a neque.
line-breaks
```
Void elements don’t require a closing tag
You’ll notice that there isn’t a closing <br> tag — it doesn’t need a closing tag because it isn’t used to surround text.

These types of tags that don’t have a closing tag are called void elements. Void meaning empty because they have no content.

One other note about this is that you might sometimes see the line break written as <br/> with the closing slash. This was a requirement for XHTML, but in HTML 5 it does not need a slash.

The browser will still read the tag correctly, but I’d still recommend writing void elements without that slash.

## Style tags
The next set of tags we’re going to look at are style tags. These tags add styles to the text.

They can be bold, like we did in the very beginning, then there’s also italics, underline, emphasized and strong tags.

Like we said before, these style tags aren’t used as much because you can now use CSS to style everything.

Let’s go through each of the style tags:

The ```<b>``` tag makes text bold.
The ```<i>``` tag makes text italic.
The ```<u>``` tag makes text underlined.
The ```<em>``` (emphasized) tag is usually interpreted as italics in browsers.
And the ```<strong>``` tag will usually be bold text.

Here’s demo code for what each of those would look like:
```html
<b>Sed efficitur laoreet nisl,</b><br> 
 <i>ac faucibus velit hendrerit sit amet.</i><br> 
 <u>Phasellus ac orci eget nisi porta accumsan a eget ex.</u><br>
 <em>Nam lacinia dolor at mi tristique rhoncus.</em><br>
 <strong>Maecenas nisl est, rhoncus id cursus non, tempor a neque.</strong>
And here’s what that code would look like in the browser:
```
## Horizontal Rule
The horizontal rule tag will create a horizontal line on your web page that goes all the way across.

You write it this way: <hr>

Like the line break tag, the horizontal rule is a void element, and just needs a single tag, without a closing tag.
```html
...
<strong>Maecenas nisl est, rhoncus id cursus non, tempor a neque.</strong>
<hr>
Phasellus venenatis dapibus laoreet. Sed in lacus a augue rutrum ultricies. 
Donec eget lacinia elit. Suspendisse commodo justo at lorem molestie, vitae 
tempus enim laoreet.
...
```


## Anchor Link
Links are one of the main ways that we get around the internet.

The link tag is written as an <a> tag. That A stands for “anchor,” because the link connects the two websites like a boat anchor connects the boat to whatever it’s anchoring to.

To create a link, first you put the <a> tag around the link text that you want to be clickable.

Aside from just the tag itself, the <a> tag requires an attribute, which means additional information inside the opening tag.

## Attributes
The attribute it uses is the href attribute. This is is short for hypertext reference. And the value is the URL of the destination website.

For example, if you want to link to the Google homepage, you would use the URL, https://www.google.com/.

URL stands for Universal Resource Locator, and it acts as an address that will give you the location of the web page or file that you want to load.

Another often used attribute in the <a> tag is “target.” This controls if the link that you click will open in the same page, or open in a new page or tab in your browser.

By default it will open the link in the same page. If you want the link to open in a new page, set target to “_blank.”

Here’s a demo of an anchor link:
```html
<a href="https://www.google.com/" target="_blank">Sed in lacus a augue rutrum</a>
```

## Images
The next thing we’ll look at is images. To put an image on your web page, you can use the image tag, written out as <img>.

The image tag is another void element that doesn’t require a closing tag.

Similar to the link tag, the image tag needs a URL. Instead of href like links use, the image tag has an attribute of src, meaning the source of the image.

Let’s find an image on the internet to use for this example– one really helpful place I go to for test images is https://placeholder.com/.

We’ll take the URL of an image from Placeholder.com and put it in the image source of the image we are creating:
```html
<img src="https://via.placeholder.com/600x300.jpg">
```

Alternatively you can download the image itself and put it in the same folder as your index.html file, and reference it this way:
```html
<img src="600x300.jpg">
```

One attribute that the <img> tag uses is border, which you can set to a number of pixels:
```html
<img src="https://via.placeholder.com/600x300.jpg" border="10">
```

## Lists
The next thing we’re going to look at is lists. HTML can create bulleted or numbered lists pretty easily.

Bulleted lists are called unordered lists, as opposed to the ordered lists that use numbers.

To create a list you’ll use the list tag– either ```<ol> or <ul>``` depending on if you’re making an ordered or unordered list.

We’re going to make an unordered list, of different types of fruits.

We’ll make our ```<ul>``` tag for the list.

Inside the list tag you’ll put your list items. Each item will go inside its own list item tag, written as ```<li>```.

We’ll add in apples, oranges, pineapples, mangoes, and dragonfruit:

```html
<ul>
   <li>apples</li>
   <li>oranges</li>
   <li>pineapples</li>
   <li>mangoes</li>
   <li>dragonfruit</li>
</ul>
```

## Nested lists
You can even nest lists inside one another. Let’s say I want to add different types of apples under apples. We would create a new list tag inside the list item in question, with its own list items.

So within the apple ```<li>``` tag, I’ll add a new ```<ul>``` tag under the “apple” text.

Then we’ll put in some different types of apples– golden delicious, gala, granny smith.

```html
<ul>
   <li>apples
      <ul>
         <li>golden delicious</li>
         <li>granny smith</li>
         <li>gala</li>
      </ul>
   </li>
   <li>oranges</li>
   <li>pineapples</li>
   <li>mangoes</li>
   <li>dragonfruit</li>
</ul>
```

## Nesting and Indentation
This brings me to an important aspect of writing good HTML. If you put an HTML tag inside another one, that is called nesting.

## Child and parent elements
An element inside another one is called a child element, and the outer element is called the parent element.

In order to organize parent and child elements, we indent the child element. This helps to distinguish it from the parent.

You can see with the list of fruits, I indented the main list items (apples, oranges, and mangoes). And then for the apple types I indented even more.

## Indenting makes code readable for humans
This helps keep the code clean. You and other people can quickly understand what it’s doing.

If all the HTML elements weren’t indented at all, and were on the same level, things would look more confusing. Just imagine having not just one element, but having lots and lots of different elements and tags, all nested in one another. It would take forever to parse out what the code is saying.

This practice of indenting is considered good practice not just for HTML, but for CSS, JavaScript, and basically programming language in existence.

It’s not necessary for the computers, but it is necessary for humans to read the code. At my first job, indenting was the first thing that I was taught during my training.

It’s pretty important. There’s nothing worse than having to work on someone else’s code and having it be a complete mess. So indenting is an easy way to make sure that you’re writing code that other people (and yourself) can go back and read.

## Table
And speaking of indenting and nested elements, the last HTML tag that we’re going to go through uses a lot of that. It’s the table.

Tables were originally used as an efficient way to organize data into rows and columns. To demonstrate, let’s make a table for a hypothetical monthly budget of a household.

## Building the table
To start, we’ll first need a ```<table>``` tag. Everything else in the table will be inside this tag.

Inside the table we’ll have table rows, table cells, and table headers for the column headers.

Then we’ll add in the first table row, using the ```<tr>``` tag.
    
```html
<table>
   <tr></tr>
</table>
```
    
Inside this row we’ll want to put the column headers. We can do this by using the <th> — table header — tags. By default the table headers are bold text and also centered within the cell.

Then we’ll just add in some budget categories here to build out this table. We’ll start with the month, and then have rent, utilities, groceries, eating out, and entertainment. I’m sure there are other categories that I’m forgetting, but we’re just keeping it simple here.

```html
<table>
   <tr>
      <th>Month</th>
      <th>Rent</th>
      <th>Utilities</th>
      <th>Groceries</th>
      <th>Eating Out</th>
      <th>Entertainment</th>
   </tr>
</table>
```
Then in the next row, we’ll add some data for the month of August. Since these are not headers, we will use the ```<td>``` tag, for table data.

All right. Let’s say our rent each month is what, $1500? Then we got $150 for utilities, $350 for groceries, $100 for eating out, and $50 for entertainment.
```html
<table>
   <tr>
      <th>Month</th>
      <th>Rent</th>
      <th>Utilities</th>
      <th>Groceries</th>
      <th>Eating Out</th>
      <th>Entertainment</th>
   </tr>
   <tr>
      <td>August</td>
      <td>$1500</td>
      <td>$150</td>
      <td>$350</td>
      <td>$100</td>
      <td>$50</td>
   </tr>
</table>
```

## Styling the table
It’s pretty basic looking, right? We can style the table a little bit with some of the built-in table attributes.

First we can add lines to the table by setting the border attribute to the table tag. We’ll set the border to 1 pixel thickness. If you use a bigger number, the border around the table will get wider. However the borders between the table cells are by default always 1 pixel wide.

You can also use cellpadding, which controls the amount of extra space inside each cell, from the text to the border. So let’s try a cellpadding of 10. And that gives just a bit more breathing room so it doesn’t seem as cramped.

The other attribute you can change is cellspacing. This controls the amount of space between cells. Personally I like no space between the cells so we’ll keep it at 0.

```html 
<table border="1" cellpadding="10" cellspacing="0">
```


## Best practices for tables
When you’re building an HTML table, one thing you need to make sure of is to have the same number of columns in every row in a table.

Otherwise things will get kinda messed up. I can show you what this looks like if I delete the Groceries cell.
```html
<table border="1" cellpadding="10" cellspacing="0">
   <tr>
      <th></th>
      <th>Month</th>
      <th>Rent</th>
      <th>Utilities</th>
      <!-- Groceries removed-->
      <th>Eating Out</th>
      <th>Entertainment</th>
   </tr>
   <tr>
      <td>August</td>
      <td>$1500</td>
      <td>$150</td>
      <td>$350</td>
      <td>$100</td>
      <td>$50</td>
   </tr>
</table>
```

If you look at the table in the browser, you can see how the headers now have shifted over one and there’s a weird blank space at the end because there isn’t a table cell there. So let’s put that back.

### Table cells can span multiple columns/rows
However, you can make a table cell span multiple columns. Let’s say we wanted to break out the Utilities to have two types of data, one for water and one for electricity. So we’ll say the electricity is $100 and water is $50.

To do this we will actually create an extra cell in the data and adjust the amounts of the Utilities. We have electricity first for $100 and water second for $50.

```html
<table border="1" cellpadding="10" cellspacing="0">
   <tr>
      <th>Month</th>
      <th>Rent</th>
      <th>Utilities</th>
      <th>Groceries</th>
      <th>Eating Out</th>
      <th>Entertainment</th>
   </tr>
   <tr>
      <td>August</td>
      <td>$1500</td>
      <td>$100</td><!-- $150 changed to $100-->
      <td>$50</td><!-- extra cell added for $50 -->
      <td>$350</td>
      <td>$100</td>
      <td>$50</td>
   </tr>
</table>
```

If we just load the table at this point you’ll see that it looks messed up again because of that extra cell in the second row. This next attribute will fix that.

## Colspan attribute
We want the Utilities header cell to be above both the $100 and the $50 cell.

To do this, we will add an attribute called colspan, i.e. column span, to the Utilities header cell. And set it to 2.

```html
<th colspan="2">Utilities</th>
```
This will make the Utilities cell span over 2 columns instead of just one.

## Rowspan attribute
In addition to colspan you can also use the rowspan attribute to make a cell span multiple rows.

Let’s say we had data for June, July and August, and we wanted to designate them as “Fall.”

I’m just going to copy and paste again, and use the August data to create June and July data too.

To create the cell for Fall, I want it to be to the left of the months, starting with June. So in the June row, I will create a new cell before June, and put “Fall” in it. Then I’ll set the rowspan of that cell to 3, so that it will span June, July and August.

And we need to add a spacer cell in the first row so that a total of 4 rows are spanned with that first column.
```html
<table border="1" cellpadding="10" cellspacing="0">
   <tr>
      <th></th>
      <th>Month</th>
      <th>Rent</th>
      <th colspan="2">Utilities</th><!-- This cell will span 2 columns in the row below it -->
      <th>Groceries</th>
      <th>Eating Out</th>
      <th>Entertainment</th>
   </tr>
    <tr>
      <td rowspan="3">Fall</td><!-- this cell will span 3 rows, June, July, & August -->
      <td>June</td>
      <td>$1500</td>
      <td>$100</td><!-- The $100 and $50 cells will be under the Utilities cell-->
      <td>$50</td>
      <td>$350</td>
      <td>$100</td>
      <td>$50</td>
   </tr>
   <tr>
      <td>July</td>
      <td>$1500</td>
      <td>$100</td>
      <td>$50</td>
      <td>$350</td>
      <td>$100</td>
      <td>$50</td>
   </tr>
   <tr>
      <td>August</td>
      <td>$1500</td>
      <td>$100</td>
      <td>$50</td>
      <td>$350</td>
      <td>$100</td>
      <td>$50</td>
   </tr>
</table>
Here’s what the final table looks like!
```

### Tables were used for website layouts
A bit of historical context about tables. Aside from containing data, web developers also used to use tables to layout web designs.

So for example if you have a website design with a header, main content, and a footer, you can create one big table with three rows. And you can then put all your content in those table cells. Table cells can contain any kind of HTML– images, links, text, you name it.

It was very handy back in the day. Nowadays tables aren’t really used very often. The only common exception that I can think of is for HTML emails, because some older email systems can’t use a lot of CSS, so coding like it’s 1999 is unfortunately the only option.

# Getting to Know CSS
CSS is a complex language that packs quite a bit of power.

It allows us to add layout and design to our pages, and it allows us to share those styles from element to element and page to page. Before we can unlock all of its features, though, there are a few aspects of the language we must fully understand.

First, it’s crucial to know exactly how styles are rendered. Specifically, we’ll need to know how different types of selectors work and how the order of those selectors can affect how our styles are rendered. We’ll also want to understand a few common property values that continually appear within CSS, particularly those that deal with color and length.

Let’s look under the hood of CSS to see exactly what is going on.

## The Cascade
We’ll begin breaking down exactly how styles are rendered by looking at what is known as the cascade and studying a few examples of the cascade in action. Within CSS, all styles cascade from the top of a style sheet to the bottom, allowing different styles to be added or overwritten as the style sheet progresses.

For example, say we select all paragraph elements at the top of our style sheet and set their background color to orange and their font size to 24 pixels. Then towards the bottom of our style sheet, we select all paragraph elements again and set their background color to green, as seen here.

```css
p {
  background: orange;
  font-size: 24px;
}
p {
  background: green;
}
```
Because the paragraph selector that sets the background color to green comes after the paragraph selector that sets the background color to orange, it will take precedence in the cascade. All of the paragraphs will appear with a green background. The font size will remain 24 pixels because the second paragraph selector didn’t identify a new font size.

Cascading Properties
The cascade also works with properties inside individual selectors. Again, for example, say we select all the paragraph elements and set their background color to orange. Then directly below the orange background property and value declaration, we add another property and value declaration setting the background color to green, as seen here.

```css
p {
  background: orange;
  background: green;
}
```

Because the green background color declaration comes after the orange background color declaration, it will overrule the orange background, and, as before, our paragraphs will appear with a green background.

All styles will cascade from the top of our style sheet to the bottom of our style sheet. There are, however, times where the cascade doesn’t play so nicely. Those times occur when different types of selectors are used and the specificity of those selectors breaks the cascade. Let’s take a look.

## Combining Selectors
So far we’ve looked at how to use different types of selectors individually, but we also need to know how to use these selectors together. By combining selectors we can be more specific about which element or group of elements we’d like to select.

For example, say we want to select all paragraph elements that reside within an element with a class attribute value of hotdog and set their background color to brown. However, if one of those paragraphs happens to have the class attribute value of mustard, we want to set its background color to yellow. Our HTML and CSS may look like the following:
### html
```html
<div class="hotdog">
  <p>...</p>
  <p>...</p>
  <p class="mustard">...</p>
</div>

```

### CSS
```css
.hotdog p {
  background: brown;
}
.hotdog p.mustard {
  background: yellow;
}
```
When selectors are combined they should be read from right to left. The selector farthest to the right, directly before the opening curly bracket, is known as the key selector. The key selector identifies exactly which element the styles will be applied to. Any selector to the left of the key selector will serve as a prequalifier.

The first combined selector above, .hotdog p, includes two selectors: a class and a type selector. These two selectors are separated by a single space. The key selector is a type selector targeting paragraph elements. And because this type selector is prequalified with a class selector of hotdog, the full combined selector will only select paragraph elements that reside within an element with a class attribute value of hotdog.

The second selector above, .hotdog p.mustard, includes three selectors: two class selectors and one type selector. The only difference between the second selector and the first selector is the addition of the class selector of mustard to the end of the paragraph type selector. Because the new class selector, mustard, falls all the way to the right of the combined selector, it is the key selector, and all of the individual selectors coming before it are now prequalifiers.

# the Box Model
CSS treats each element in your HTML document as a “box” with a bunch of different properties that determine where it appears on the page.
![Box Model](https://internetingishard.com/html-and-css/css-box-model/css-box-model-73a525.png)
### How Are Elements Displayed?
Before jumping into the box model, it helps to understand how elements are displayed. In Lesson 2 we covered the difference between block-level and inline-level elements. To quickly recap, block-level elements occupy any available width, regardless of their content, and begin on a new line. Inline-level elements occupy only the width their content requires and line up on the same line, one after the other. Block-level elements are generally used for larger pieces of content, such as headings and structural elements. Inline-level elements are generally used for smaller pieces of content, such as a few words selected to be bold or italicized.

## Display
Exactly how elements are displayed—as block-level elements, inline elements, or something else—is determined by the display property. Every element has a default display property value; however, as with all other property values, that value may be overwritten. There are quite a few values for the display property, but the most common are block, inline, inline-block, and none.

We can change an element’s display property value by selecting that element within CSS and declaring a new display property value. A value of block will make that element a block-level element.

```css
p {
  display: block;
}
```
A value of inline will make that element an inline-level element.

```css
p {
  display: inline;
}
```

Things get interesting with the inline-block value. Using this value will allow an element to behave as a block-level element, accepting all box model properties (which we’ll cover soon). However, the element will be displayed in line with other elements, and it will not begin on a new line by default.

```css
p {
  display: inline-block;
}
```
### Set up your folder and files:
To get started, let’s create a new folder called css-box-model and stick a new web page in it called boxes.html. Add the following code:
```html
<!DOCTYPE html>
<html lang='en'>
  <head>
    <meta charset='UTF-8'/>
    <title>Boxes Are Easy!</title>
    <link rel='stylesheet' href='box-styles.css'/>
  </head>
  <body>
    <h1>Headings Are Block Elements</h1>

    <p>Paragraphs are blocks, too. <em>However</em>, &lt;em&gt; and &lt;strong&gt;
       elements are not. They are <strong>inline</strong> elements.</p>

    <p>Block elements define the flow of the HTML document, while inline elements
       do not.</p>
  </body>
</html>
```
## Block Elements and Inline Elements
Each HTML element rendered on the screen is a box, and they come in two flavors: “block” boxes and “inline“ boxes.

All the HTML elements that we’ve been working with have a default type of box. For instance, ```<h1> and <p>``` are block-level elements, while ```<em> and <strong>``` are inline elements.
 
Let’s get a better look at our boxes by adding the following to box-styles.css:

```css
h1, p {
  background-color: #DDE0E3;    /* Light gray */
}

em, strong {
  background-color: #B2D6FF;    /* Light blue */
}
```
![Block and Inline boxes](https://internetingishard.com/html-and-css/css-box-model/block-boxes-and-inline-boxes-7cfa0a.png)

The background-color property only fills in the background of the selected box, so this will give us a clear view into the structure of the current sample page. Our headings and paragraphs should have gray backgrounds, while our emphasis and strong elements should be light blue.
This shows us a couple of very important behaviors associated with block and inline boxes:

    - Block boxes always appear below the previous block element. This is the “natural” or “static” flow of an HTML document when it gets rendered by a web browser.
    - The width of block boxes is set automatically based on the width of its parent container. In this case, our blocks are always the width of the browser window.
    - The default height of block boxes is based on the content it contains. When you narrow the browser window, the <h1> gets split over two lines, and its height adjusts accordingly.
    - Inline boxes don’t affect vertical spacing. They’re not for determining layout—they’re for styling stuff inside of a block.
    - The width of inline boxes is based on the content it contains, not the width of the parent element.

## Changing Box Behavior

We can override the default box type of HTML elements with the CSS display property. For example, if we wanted to make our ```<em> and <strong>``` elements blocks instead of inline elements, we could update our rule in box-styles.css like so:
```css
em, strong {
  background-color: #B2D6FF;
  display: block;
}
```
![Turning Inline to Block](https://internetingishard.com/html-and-css/css-box-model/turning-inline-into-block-boxes-772f4c.png)
Now, these elements act like our headings and paragraphs: they start on their own line, and they fill the entire width of the browser. This comes in handy when you’re trying to turn <a> elements into buttons or format ```<img/>``` elements (both of these are inline boxes by default).
 
## Content, Padding, Border, and Margin
The "CSS box model" is a set of rules that determine the dimensions of every element in a web page. It gives each box (both inline and block) four properties:

    - Content – The text, image, or other media content in the element.
    - Padding – The space between the box’s content and its border.
    - Border – The line between the box’s padding and margin.
    - Margin – The space between the box and surrounding boxes.

Together, this is everything a browser needs to render an element’s box. The content is what you author in an HTML document, and it’s the only one that has any semantic value (which is why it’s in the HTML). The rest of them are purely presentational, so they’re defined by CSS rules. 

### Padding
This adds 50 pixels to each side of the ```<h1>``` heading. Notice how the background color expands to fill this space. That’s always the case for padding because it’s inside the border, and everything inside the border gets a background.
```css
h1 {
  padding: 50px;
}
```
Sometimes you’ll only want to style one side of an element. For that, CSS provides the following properties:
 ```css
p {
  padding-top: 20px;
  padding-bottom: 20px;
  padding-left: 10px;
  padding-right: 10px;
}
```
### Shorthand Formats

Typing out all of these properties out can be tiresome, so CSS provides an alternative “shorthand” form of the padding property that lets you set the top/bottom and left/right padding with only one line of CSS. When you provide two values to the padding property, it’s interpreted as the vertical and horizontal padding values, respectively.

```css
p {
  padding: 20px 10px;  /* Vertical  Horizontal */
}
```

Let’s try this out by removing the 10px right padding from the previous rule. This should give us 20 pixels on the top and bottom of each paragraph, 10 pixels on the left, but none on the right:
```css
p {
  padding: 20px 0 20px 10px;  /* Top  Right  Bottom  Left */
}
```

### Borders
Try adding a border around our ```<h1>``` heading by updating the rule in box-styles.css:
```css
h1 {
  padding: 50px;
  border: 1px solid #5D6063;
}
```
Drawing a border around our entire heading makes it look a little 1990s, so how about we limit it to the bottom of the heading? Like padding, there are -top, -bottom, -left, and -right variants for the border property:
```css
border-bottom: 1px solid #5D6063;
```
## Margins
Margins define the space outside of an element’s border. Or, rather, the space between a box and its surrounding boxes. Let’s add some space to the bottom of each ```<p>``` element:
```css
p {
  padding: 20px 0 20px 10px;
  margin-bottom: 50px;          /* Add this */
}
```
This demonstrates a side-specific variant of the margin property, but it also accepts the same shorthand formats as padding.

Margins and padding can accomplish the same thing in a lot of situations, making it difficult to determine which one is the “right” choice. The most common reasons why you would pick one over the other are:

    - The padding of a box has a background, while margins are always transparent.
    - Padding is included in the click area of an element, while margins aren’t.
    - Margins collapse vertically, while padding doesn’t (we’ll discuss this more in the next section).

## Margins on Inline Elements

One of the starkest contrasts between block-level elements and inline ones is their handling of margins. Inline boxes completely ignore the top and bottom margins of an element. For example, watch what happens when we add a big margin to our ```<strong>``` element:
```css
strong {
  margin: 50px;
}
```
The horizontal margins display just like we’d expect, but this doesn’t alter the vertical space around our``` <strong>``` element one bit.

If we change margin to padding, we’ll discover that this isn’t exactly the case for a box’s padding. It’ll display the blue background; however, it won’t affect the vertical layout of the surrounding boxes.

## Generic Boxes

So far, every HTML element we’ve seen lends additional meaning to the content it contains. Indeed, this is the whole point of HTML, but there are many times when we need a generic box purely for the sake of styling a web page. This is what <div> and <span> are for.

Both ```<div> and <span>``` are “container” elements that don’t have any affect on the semantic structure of an HTML document. They do, however, provide a hook for adding CSS styles to arbitrary sections of a web page. For example, sometimes you need to add an invisible box to prevent a margin collapse, or maybe you want to group the first few paragraphs of an article into a synopsis with slightly different text formatting.

We’ll use a lot of ```<div>’s``` throughout the rest of this tutorial. 

For now, let’s create a simple button by adding the following to the bottom of our boxes.html file:
```html
<div>Button</div>
```

And here are the associated styles that need to go into box-styles.css. Most of these should be familiar from the last chapter, although we did throw in a new border-radius property:
```css
div {
  color: #FFF;
  background-color: #5995DA;
  font-weight: bold;
  padding: 20px;
  text-align: center;
  border: 2px solid #5D6063;
  border-radius: 5px;
}
```
This will give us a big blue button that spans the entire width of the browser:
Web page using ```<div>``` elements for buttons

Of course, these styles also apply to the invisible ```<div>``` we used to break the margin collapse in the previous section. Obviously, we need a way to select individual ```<div>’s``` if they’re to be of any practical use to us. That’s what class selectors are for, which we’ll introduce in the next chapter. In lieu of those, let’s just delete or comment out that invisible ```<div>```.

The only real difference between a ```<div> and a <span>``` is that the former is for block-level content while the latter is meant for inline content.

## Explicit Dimensions

So far, we’ve let our HTML elements define their dimensions automatically. The paddings, borders, and margins we’ve been playing with all wrap around whatever content happens to be inside the element’s box. If you add more text to our ```<em>``` element, everything will expand to accommodate it:

Web page showing an ```<em>``` element expanding as more content is added

But, sometimes our desired layout calls for an explicit dimension, like a sidebar that’s exactly 250 pixels wide. For this, CSS provides the width and height properties. These take precedence over the default size of a box’s content.

Let’s give our button an explicit width by adding the following property to box-styles.css:
```html
div {
  /* [Existing Declarations] */
  width: 200px;
}
````
Instead of being as wide as the browser window, our button is now 200 pixels, and it hugs the left side of the page:

Also notice that if you make the button’s title longer, it will automatically wrap to the next line, and the element will expand vertically to accommodate the new content. You can change this default behavior with the white-space and overflow properties.

## Content Boxes and Border Boxes

The width and height properties only define the size of a box’s content. Its padding and border are both added on top of whatever explicit dimensions you set. This explains why you’ll get an image that’s 244 pixels wide when you take a screenshot of our button, despite the fact that it has a width: 200px declaration attached to it.
Diagram: content-box measurements adding padding and border to width of the element

Needless to say, this can be a little counterintuitive when you’re trying to lay out a page. Imagine trying to fill a 600px container with three boxes that are all width: 200px, but they don’t fit because they all have a 1px border (making their actual width 202px).

Fortunately, CSS lets you change how the width of a box is calculated via the box-sizing property. By default, it has a value of content-box, which leads to the behavior described above. Let’s see what happens when we change it to border-box:
```html
div {
  color: #FFF;
  background-color: #5995DA;
  font-weight: bold;
  padding: 20px;
  text-align: center;
  border: 2px solid #5D6063;
  border-radius: 5px;
  
  width: 200px;
  box-sizing: border-box;  /* Add this */
}
```
This forces the actual width of the box to be 200px—including padding and borders. Of course, this means that the content width is now determined automatically:

This is much more intuitive, and as a result, using border-box for all your boxes is considered a best practice among modern web developers.

### Aligning Boxes

Aligning boxes horizontally is a common task for web developers, and the box model offers a lot of ways to do it. We already saw the text-align property, which aligns the content and inline boxes inside of a block-level element. Aligning block boxes is another story.

Try adding the following rule to our stylesheet. It will only align the content inside of our block boxes—not the blocks themselves. Our <div> button is still left-aligned regardless of the <body>’s text alignment:
```html
body {
  text-align: center;
}
```
There are three methods for horizontally aligning block-level elements: “auto-margins” for center alignment, “floats” for left/right alignment, and “flexbox” for complete control over alignment. Yes, unfortunately block-level alignment is totally unrelated to the text-align property.

## Centering With Auto-Margins

Floats and flexbox are complicated topics that we’ve devoted entire chapters to, but we do have the background to deal with auto-margins right now. When you set the left and right margin of a block-level element to auto, it will center the block in its parent element.

For example, we can center our button with the following:
```html
div {
  color: #FFF;
  background-color: #4A90E2;
  font-weight: bold;
  padding: 20px;
  text-align: center;

  width: 200px;
  box-sizing: border-box;
  margin: 20px auto; /* Vertical  Horizontal */
}
```
Note that this only works on blocks that have an explicit width defined on them. Remove that width: 200px line, and our button will be the full width of the browser, making “center alignment” meaningless.

## Resetting Styles

Notice that white band around our page? That’s a default margin/padding added by your browser. Different browsers have different default styles for all of their HTML elements, making it difficult to create consistent stylesheets.
One web page showing white border due to default margin/padding and another web page without the white border after a universal reset

It’s usually a good idea to override default styles to a predictable value using the “universal” CSS selector ```(*)```. Try adding this to the top of our box-styles.css file:
```html
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```
This selector matches every HTML element, effectively resetting the margin and padding properties for our web page. We also converted all our boxes to border-box, which, again, is a best practice.

![alt text](https://learn.shayhowe.com/assets/images/courses/html-css/opening-the-box-model/developer-tools.png)

## Positioning Content
One of the best things about CSS is that it gives us the ability to position content and elements on a page in nearly any imaginable way, bringing structure to our designs and helping make content more digestible.

There are a few different types of positioning within CSS, and each has its own application. In this chapter we’re going to take a look at a few different use cases—creating reusable layouts and uniquely positioning one-off elements—and describe a few ways to go about each.

## Positioning with Floats

One way to position elements on a page is with the float property. The float property is pretty versatile and can be used in a number of different ways.

Essentially, the float property allows us to take an element, remove it from the normal flow of a page, and position it to the left or right of its parent element. All other elements on the page will then flow around the floated element. An <img> element floated to the side of a few paragraphs of text, for example, will allow the paragraphs to wrap around the image as necessary.

When the float property is used on multiple elements at the same time, it provides the ability to create a layout by floating elements directly next to or opposite each other, as seen in multiple-column layouts.

The float property accepts a few values; the two most popular values are left and right, which allow elements to be floated to the left or right of their parent element.
```css
img {
  float: left;
}
```             
## Floats in Practice

Let’s create a common page layout with a header at the top, two columns in the center, and a footer at the bottom. Ideally this page would be marked up using the ```<header>, <section>, <aside>, and <footer>``` elements. Inside the ```<body>``` element, the HTML may look like this:
```html
<header>...</header>
<section>...</section>
<aside>...</aside>
<footer>...</footer>
```
## Layout without Floats Demo

Here the ```<section> and <aside>``` elements, as block-level elements, will be stacked on top of one another by default. However, we want these elements to sit side by side. By floating the ```<section>``` to the left and the ```<aside>``` to the right, we can position them as two columns sitting opposite one another. Our CSS should look like this:
```css
section {
  float: left;
}
aside {
  float: right;
}
```             
For reference, when an element is floated, it will float all the way to the edge of its parent element. If there isn’t a parent element, the floated element will then float all the way to the edge of the page.

When we float an element, we take it out of the normal flow of the HTML document. This causes the width of that element to default to the width of the content within it. Sometimes, such as when we’re creating columns for a reusable layout, this behavior is not desired. It can be corrected by adding a fixed width property value to each column. Additionally, to prevent floated elements from touching one another, causing the content of one to sit directly next to the content of the other, we can use the margin property to create space between elements.

Here, we are extending the previous code block, adding a margin and width to each column to better shape our desired outcome.
```css
section {
  float: left;
  margin: 0 1.5%;
  width: 63%;
}
aside {
  float: right;
  margin: 0 1.5%;
  width: 30%;
}
```
## Layout with Floats Demo
*Floats May Change an Element’s Display Value
When floating an element, it is also important to recognize that an element is removed from the normal flow of a page, and that may change an element’s default display value. The float property relies on an element having a display value of block, and may alter an element’s default display value if it is not already displayed as a block-level element.
For example, an element with a display value of inline, such as the ```<span>``` inline-level element, ignores any height or width property values. However, should that inline-level element be floated, its display value will be changed to block, and it may then accept height or width property values.
As we float elements we must keep an eye on how their display property values are affected.*

With two columns we can float one column to the left and another to the right, but with more columns we must change our approach. Say, for example, we’d like to have a row of three columns between our ```<header> and <footer>``` elements. If we drop our ```<aside>``` element and use three ```<section>``` elements, our HTML might look like this:
```html
<header>...</header>
<section>...</section>
<section>...</section>
<section>...</section>
<footer>...</footer>
```
To position these three ```<section>``` elements in a three-column row, instead of floating one column to the left and one column to the right, we’ll float all three ```<section>``` elements to the left. We’ll also need to adjust the width of the ```<section>``` elements to account for the additional columns and to get them to sit one next to the other.
```css
section {
  float: left;
  margin: 0 1.5%;
  width: 30%;
}
```
Here we have three columns, all with equal width and margin values and all floated to the left.

## Clearing & Containing Floats

The float property was originally designed to allow content to wrap around images. An image could be floated, and all of the content surrounding that image could then naturally flow around it. Although this works great for images, the float property was never actually intended to be used for layout and positioning purposes, and thus it comes with a few pitfalls.

One of those pitfalls is that occasionally the proper styles will not render on an element that it is sitting next to or is a parent element of a floated element. When an element is floated, it is taken out of the normal flow of the page, and, as a result, the styles of elements around that floated element can be negatively impacted.

Often margin and padding property values aren’t interpreted correctly, causing them to blend into the floated element; other properties can be affected, too.

Another pitfall is that sometimes unwanted content begins to wrap around a floated element. Removing an element from the flow of the document allows all the elements around the floated element to wrap and consume any available space around the floated element, which is often undesired.

With our previous two-column example, after we floated the ```<section> and <aside>``` elements, and before we set a width property value on either of them, the content within the ```<footer>``` element would have wrapped in between the two floated elements above it, filling in any available space. Consequently, the ```<footer>``` element would have sat in the gutter between the ```<section> and <aside>``` elements, consuming the available space.
Layout without Cleared or Contained Floats Demo

To prevent content from wrapping around floated elements, we need to clear, or contain, those floats and return the page to its normal flow. We’ll proceed by looking at how to clear floats, and then we’ll take a look at how to contain floats.
Clearing Floats

Clearing floats is accomplished using the clear property, which accepts a few different values: the most commonly used values being left, right, and both.
```css
div {
  clear: left;
}
```            
The left value will clear left floats, while the right value will clear right floats. The both value, however, will clear both left and right floats and is often the most ideal value.

Going back to our previous example, if we use the clear property with the value of both on the ```<footer>``` element, we are able to clear the floats. It is important that this clear be applied to an element appearing after the floated elements, not before, to return the page to its normal flow.
```css
footer {
  clear: both;
}
```         
Layout with Cleared Floats Demo
## Containing Floats

Rather than clearing floats, another option is to contain the floats. The outcomes of containing floats versus those of clearing them are nearly the same; however, containing floats does help to ensure that all of our styles will be rendered properly.

To contain floats, the floated elements must reside within a parent element. The parent element will act as a container, leaving the flow of the document completely normal outside of it. The CSS for that parent element, represented by the group class below, is shown here:
```css
.group:before,
.group:after {
  content: "";
  display: table;
}
.group:after {
  clear: both;
}
.group {
  clear: both;
  *zoom: 1;
}
```
              

There’s quite a bit going on here, but essentially what the CSS is doing is clearing any floated elements within the element with the class of group and returning the flow of the document back to normal.

More specifically, the ```:before and :after``` pseudo-elements, as mentioned in the Lesson 4 exercise, are dynamically generated elements above and below the element with the class of group. Those elements do not include any content and are displayed as table-level elements, much like block-level elements. The dynamically generated element after the element with the class of group is clearing the floats within the element with the class of group, much like the clear from before. And lastly, the element with the class of group itself also clears any floats that may appear above it, in case a left or right float may exist. It also includes a little trickery to get older browsers to play nicely.

It is more code than the clear: both; declaration alone, but it can prove to be quite useful.

Looking at our two-column page layout from before, we could wrap the ```<section> and <aside>``` elements with a parent element. That parent element then needs to contain the floats within itself. The code would look like this:

### HTML
```html
<header>...</header>
<div class="group">
  <section>...</section>
  <aside>...</aside>
</div>
<footer>...</footer>
```            
### CSS
```css
.group:before,
.group:after {
  content: "";
  display: table;
}
.group:after {
  clear: both;
}
.group {
  clear: both;
  *zoom: 1;
}
section {
  float: left;
  margin: 0 1.5%;
  width: 63%;
}
aside {
  float: right;
  margin: 0 1.5%;
  width: 30%;
}
```
Layout with Contained Floats Demo

The technique shown here for containing elements is know as a “clearfix” and can often be found in other websites with the class name of clearfix or cf. We’ve chosen to use the class name of group, though, as it is representing a group of elements, and better expresses the content.

As elements are floated, it is important to keep note of how they affect the flow of a page and to make sure the flow of a page is reset by either clearing or containing the floats as necessary. Failing to keep track of floats can cause quite a few headaches, especially as pages begin to have multiple rows of multiple columns.

# JavaScript
## History

JavaScript was introduced by Brendan Eich in 1995 for Netscape Communications. It was submitted few months later to Ecma International for consideration as an industry standard. The result standard version is ECMAScript.

Even if the name comes from a partnership between Netscape and Sun Microsystems (distributor of Java) JavaScript is not a "light" version of Java.

    A Brief History of JavaScript by Brendan Eich (video)

## Definition & properties

JavaScript is a scripting language that supports multiple programming styles. It differs from other languages such as C++, Java or PHP with its dynamic behaviour, its first-class functions and its prototype-based inheritance.

JavaScript lovers consider these features as the force of the language. It's very common for people who try to write JavaScript like they write code in other languages to hate it. Don't make this mistake!

    - Dynamic
    - Weakly typed
    - Multi-paradigm
    - Imperative
    - Functional
    - Object-oriented
    - First-class functions
    - Prototype-based

Usages

Even if it was originally designed to work in a browser environment, JavaScript is now used on several different platforms. Here are a few examples :

    - Web server
    - Browser addons/extensions
    - Mobile applications
    - Databases consoles
    - OpenOffice scripts/macros
    - Java applications

    - node.js
    - Building and extension for Firefox
    - Get started with Chrome extension development
    - PhoneGap
    - MongoDB
    - Mozilla Rhino

## Tools

Your browser should have two very useful tools to work with JavaScript :

    JavaScript Debugger
    JavaScript Console

There's also great tools on the web :

    JSfiddle (online playground)
    JS Bin (online playground)
    Codepen (online playground)
    tinkerbin (online playground)
    JSperf (online benchmarking tool)


    JavaScript Reference (MDN)
    ECMAScript documentation
    JavaScript Garden (github)
    Eloquent JavaScript

## Basic syntax

  1. JavaScript is case-sensitive.
  2. Lines end by semicolon ;.
  3. Block are delimited curly brackets by { }.
  4. Comments are between /* */ for multiple lines or after // for one line.
  
## Variables & Types

In JavaScript, Typing is dynamic. Therefore, there is NO type declaration before variable names. Instead we use a unique keyword : var. Note that a variable can be declared several times. If it's non-declared, the variable is automatically allocated at the first use.

### Number

Numbers like in any other languages are really important. Don't forget that a computer is primarly a super calculator. Integers and floats have the same type : Number. Of course, a variable can only be identified as type Number at execution time..

If you want to manipulate numbers, the objects Number and Math has lots of useful properties and methods. The other useful way to manipulate them is operators of course. See reference for more details.
```js
// Integer
var i;            // first declaration of i (type is undefined)
i = 2;            // i is now a integer (type is number)

In this example we see that floats can have strange behaviour, don't forget the internals of the float storage. It's stored as IEEE 754.

// Float
var i = -5.01;    // second declaration of i as a float (type is number)
j = 2;            // j was not declared, automatic assignement to 2
j = i + 1.12;     // j is now a float equal to 3.12 (still number)
// Be careful
var k = 0.1 + 0.2 // k => 0.30000000000000004

var l = new Number(7);    // DO NOT USE : type is object and not number

// Specials
var a = 10 / 0;           // => Infinity
var b = -10 / 0;          // => -Infinity
var c = Math.sqrt(-1);    // => NaN : Not a Number

    Number reference (MDN)
    Math reference (MDN)
    Why should you not use Number as a constructor? (stack overflow)
    The_Complete_JavaScript_Number_Reference, usage of new Number(2) (hunlock)
```

### String

Strings are really simple. Quotes or double quotes, no differences, some text in it and you're done. The most important property of a String when it comes to manipulation is length. It's not the only one, the String object contains a lot of useful properties and methods, see reference for more details.

The other way a good programer should manipulate string is regular expressions and as expected, JavaScript provides a regex engine and a RegExp object. Regex can be complicated to master, but the game is worth it since it's a multi language concept. See reference for more details.

var a = ""; // The empty string: it has zero characters
var b = 'There is no spoon.';
var c = "Only human.";
var d = 'pill="red"';
var e = "Free your mind.";
var f = "You're empty.\nSo are you."; // Type of all variables is string

var g = new String("Welcome to the real world.");
// DO NOT USE : type is object and not string

    String reference (MDN)
    Regex reference (MDN)
    regular-expressions.info
    Online testing tool (gskinner.com)

### Boolean

Nothing fancy here, true of false. You'll see later that other types of variables (Number, String...) can by evaluated as booleans according to some rules.

var realWorld = false;
var matrix = true;         // Type of all variables is boolean

var a = new Boolean(true); // DO NOT USE : type is object and not boolean

    Boolean reference (MDN)

### null and undefined

Both null and undefined are used for absence of a value. One is used when the variable has been initialiazed : null. The other one is used when the variable has not been initialized : undefined. It can be returned by function that have no return statement.
```js
var neo;      // Type is undefined
neo = null;   // Type is object
```
    Typeof null is object (MDN)
    undefined reference (MDN)

### Arrays

An array is an ordered colleciton of values. Values can be of different types. Each value is called an element and is positioned in the array with a numeric index starting at zero.

The Array object has several properties and methods. The most important property is length, it contains the size of the array. See reference for more details.

    Array reference (MDN)

### Creating

The easiest way to create an array is with square brackets and comma separated values in it. Note that you can create an array with 4 undefined elements, length will be 4.
```js
var a = [];                         // no elements
var b = new Array();                // equivalent to a
var c = [,,,,];                     // 4 elements, all undefined.
var d = new Array(4);               // equivalent to c
var e = ["the", 1, true];           // 3 elements of different types
var f = new Array("the", 1, true);  // equivalent to e
```
## Reading and writing

Reading and writing in arrays is done with brackets and equal assignment operator. Note that reading from and index that haven't been initialized doesn't generate any errors, it returns undefined.

You can insert values in non consecutive indexes, it create a what's called a "sparse array". The length is updated to maximum index + 1.
```js
var a = ["white"];    // Start with a one-element array

var b = a[0];         // b => "white"
var c = a[100];       // c => undefined (no error)

a[1] = 3.14;          // a => ["white", 3.14]
var i = 2;
a[i] = 3;             // a => ["white", 3.14, 3]
a[i + 1] = "rabbit";  // a => ["white", 3.14, 3, "rabbit"]
a[a[i]] = a[0];       // a => ["white", 3.14, 3, "white"]

var d = a.length;     // d => 4
```
## Adding and deleting

To add and delete elements from an array, you can use the methods from the Array object. There's a lot of useful ones, from simple pop and push to more complex ones like splice. See reference for more details.
```js
var a = ["follow", "the", "white", "rabbit"];

var b = a.pop();             // a => ["follow", "the", "white"]
                             // b => "rabbit"
var c = a.push("RABBIT");    // a => ["follow", "the", "white", "RABBIT"]
                             // c => 4 (new length)

var d = a.shift();           // a => ["the", "white", "RABBIT"]
                             // d => "follow"
var e = a.unshift("FOLLOW"); // a => ["FOLLOW", "the", "white", "RABBIT"]
                             // e => 4 (new length)

var f = a.splice(2, 1);       // a => ["FOLLOW", "the", "RABBIT"]
                              // f => "white"
var g = a.splice(1, 2, "ME"); // a => ["FOLLOW", "ME"]
                              // g => ["the", "RABBIT"]
```
## Operators

Operators are really powerful in JavaScript. Unlike in some other languages like C, operators are not only used to do maths, they are also very useful with strings.

    Operator Precedence reference (MDN)

## Arithmetic

Arithmetic operators work the same way as a lot of other programming languages. Note that + is used to concatenate strings.
```js
var a = 6 + 4;                    // a => 10
var b = -a;                       // b => -10
var c = 6 - 4;                    // c => 2

var d = 1, e = ++d;               // d and e are both 2
var f = 1, g = f++;               // f is 2, g is 1
var h = 7, i = --h;               // h and i are both 6
var j = 7, k = j--;               // j is 6, k is 7

var l = 3 * 3                     // l => 9
var m = 10 / 3                    // m => 3.3333333333333335
var n = 10 % 3                    // n => 1

var o = "Dodge" + " " + "this."   // o => "Dodge this.";
```
    Arithmetics operators reference (MDN)

## Equality

A particularity of JavaScript is the two kinds of equality comparison : strict and type-converting. Just remember that strict equal === compares both types and values and type-converting equal == converts one type to the other and just compares values.

Best practice is to always use the strict equality. It prevents a lot of mistakes.
```js
// Equality
var a = "2" == 2;    // a => true
var b = "2" != 2;    // b => false

// Strict equality
var c = "2" === 2;   // c => false
var d = "2" !== 2;   // d => true
```
    Comparison operators reference (MDN)

## Comparison

Like arithmetics, comparison operators work the same way as a lot of other programming languages. Note that these operators can be used to compare string.
```js
var a = 2 > 2;          // a => false
var b = 2 <= 2;         // b => true
var c = "2" >= 2;       // c => true
var d = 2 < 2;          // d => false
var e = 2 <= 2;         // e => true

var f = 'abc' < 'def'   // f => true
```
    Comparison operators reference (MDN)

## Logical
```js
var a = true && false;  // a => false
var b = true || false;  // b => true
var c = !true;          // c => false
```
    Logical operators reference (MDN)

## Bitwise

Bitwise operators help programmers to use numbers like sequences of 32 bits (zeros and ones). It's not always easy to understand what's going on but it's very useful, for example if you're implementing bitmasks.
```js
var a = 42 & 2   // a =>          2  (AND)
var b =  7 | 2   // b =>          2  (OR)
var c =  7 ^ 2   // c =>          7  (XOR)
var d = ~8       // d =>         -7  (NOT)
var e =  1 << 3  // e =>          8  (Shift left)
var f =  8 >> 2  // f =>          2  (Shift right)
var g = -1 >>  2 // g =>         -1
var h = -1 >>> 2 // h => 1073741823  (Shift right with zero fill)
```
    Bitwise operators reference (MDN)

## Assignement

Assignement operators saves you some place and can improve code readability. Use them carefuly!
```js
var a = 1, b = 0;
a += b    // a = a + b
a -= b    // a = a - b
a *= b    // a = a * b
a /= b    // a = a / b
a %= b    // a = a % b
a <<= b   // a = a << b
a >>= b   // a = a >> b
a >>>= b  // a = a >>> b
a &= b    // a = a & b
a |= b    // a = a | b
a ^= b    // a = a ^ b
```
    Assignment operators reference (MDN)

## in

The in operator is used to verify if a property is specified on an object. Be careful when you use it.
```js
var a = [1,9,4];
var b = (2 in a);          // b => true
var c = (9 in a);          // c => false
var d = (length in a);     // d => true
```
    in operator reference (MDN)

## typeof

typeof is used at compilation time to verify the type of a variable.
```js
var a = 3;
var b = typeof a;   // b => "number"
var c = "";
var d = typeof c;   // d => "string"
var e = true;
var f = typeof e;   // f => "boolean"
```
    in operator reference (MDN)

## Type conversions

JavaScript is not statically typed but you can determine the type of a variable at execution time. Conversion from one type to another can be done explicitly or implicitly. It's really important to understand implicit ones, they can help you to avoid strange behaviours and bugs.
Explicit

Explicit conversions can for example help you to convert a string to a number. Note that even if integers and floats are both number, using parseInt on a float removes the decimals and makes it by definition an integer.
```js
// to Number
var a = Number("10");         // a => 10
var b = Number(false);        // b =>  0
var c = parseInt("10", 10);   // c => 10
var d = parseInt(10.2);       // d => 10
var e = parseFloat("10.2");   // e => 10.2

// to String
var a = String(false);        // a => "false"
var b = String(10);           // b => "10"
var c = String(10.2);         // c => "10.2"
var d = (10).toString();      // d => "10"

// to Boolean
var a = Boolean(10);          // a => true
var b = Boolean(0);           // b => false
var c = Boolean(0.3);         // c => true
var d = Boolean("true");      // d => true
```
## Implicit

There's a lot of ways to convert a string to a number. Performances can differ a lot depending on the technique used and the plateform. A shorter syntax is often prefered for bandwith uses.

Look carefully how the + operator behaves with strings and numbers.
```js
// to Number
var a = +"10";            // a => 10
var b = "10" >> 0;        // b => 10
var c = "10" * 1;         // c => 10
var d = ~~"10";           // d => 10
var e = "2" * "5";        // e => 10 (both strings converts to number)

// to String
var a = 10 + "10";             // a => "1010"
var b = "10" + "10";           // b => "1010"
var c = 10 + " agents";        // c => "10 agents"
var d = 10 + 10 + " agents";   // d => "20 agents"

// to Boolean
var a = !!'morpheus';     // a => true
var b = !!'';             // b => false
var c = !!'0';            // c => true
var d = !!'1';            // d => true
```
    String to number comparison (jsperf.com)

## Statements

## Conditional

In JavaScript, conditionnal statements behaves pretty much like in other common languages.

Note that the conditional ternary operator should only be used in simple cases. It is often use for variable assignment and its usage is synonym of shorter syntax and readability. If you think it doesn't make your code better, use a classic if.
### if/else

In this case, normal equality is handy, used with null, it can test null || undefined.
```js
if (username == null) {  // if username is null or undefined,
  username = "Trinity";  // define it
}

if (bulletCount === 1) {
  bulletCount += ' bullet';
} else {
  bulletCount += ' bullets';
}

var user = (name == null) ? 'default user' : name;
```
    If...else reference (MDN)

### switch

Switch usage is often advised when you have too much if statements. Don't forget the break keyword. Note that you can use string unlike some other languages.
```js
var quote;
switch (characterName) {
  case 'Smith':
    quote = 'Goodbye, Mr. Anderson...';
    break;
  case 'Neo':
    quote = 'I know kung fu.';
    break;
  default:
    quote = 'What is the Matrix?';
    break;
}
```
    Switch reference (MDN)

### loops
```js
for (var i = 0; i < 10; i++) {
  doSomething();
}

var count = 0;
while (count < 10) {
  doSomething();
  count++;
}

var count = 100;
do {
  doSomething();
} while (--count > 0);
```
    Loops reference (MDN)

### for...in loops

for..in loops are used to iterate over properties of an object.

Array indexes are just enumerable properties with integer names. Therefore, for...in loops could be used to enumerate elements of an array.

Because of performance issues and in order to avoid bugs, use classic for loops instead of for..in with arrays.
```js
var a = [123, 456, 789];
for (var i in a) {      // DO NOT use with arrays
  doSomething(a[i]);
}
```
Because of performance issues and in order to avoid "bugs" and "strange behaviours", use classic for loops instead of for..in with arrays.

    for...in loops reference (MDN)
    for vs. for..in (JSperf.com)

Browser objects

Every JavaScript plateform/environment adds objects with global scope. They're meant to provide helpful features to developers. In web browsers the most important ones are : document and window.

Another object is present but only in modern browsers : console. Since it's not standard, implementations may differ, see references for more details. Remember that older browsers don't support it, so don't let console.log('foo') etc... in production code.

var title = document.title;
var href = window.location.href;
var userAgent = window.navigator.userAgent;

window.alert('Never send a human to do a machine\'s job.');
var bluePill = confirm('Take the blue pill?');
var name = prompt('What is your name?');

console.log('Perhaps we are asking the wrong questions.');
console.error('Nothing. Just had a little déjà vu.');
console.info('A déjà vu is usually a glitch in the Matrix.');
console.warn('The Matrix is a system, Neo. That system is our enemy.');

    document reference (MDN)
    window reference (MDN)
    Firefox web console (MDN)
    Chrome web console
    IE web console
    Opera web console
    Safari web console



