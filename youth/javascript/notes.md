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
Let’s look first at the headline or header tags, designated with the letter H. Each H tag also has a number after the H. They range from <h1> to <h6>.

The  <h1> tag is the highest in priority. It’s generally used for the title of the page.

We’re going to add an  <h1> tag to our web page. Inside the tag we will put the title of the webpage, My First Website.

We’ll also add a subtitle using the  <h2> tag, with the content: “An HTML Playground.”

And just for kicks, let’s add in the rest of the H tags, up to <h6>.

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

You can see how the font sizes get progressively smaller from  <h1> to <h6>.

Most websites don’t use all the H tags. Usually they will use  <h1> for the title,  <h2> for subtitle, and  <h3> sometimes for section titles. It’s pretty rare to use  <h4> through <h6>.

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
The next set of tags we’re going to look at are style tags– these tags add styles to the text.

They can be bold, like we did in the very beginning, then there’s also italics, underline, emphasized and strong tags.

Like we said before, these style tags aren’t used as much because you can now use CSS to style everything.

Let’s go through each of the style tags:

The <b> tag makes text bold.
The <i> tag makes text italic.
The <u> tag makes text underlined.
The <em> (emphasized) tag is usually interpreted as italics in browsers.
And the <strong> tag will usually be bold text.

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

To create a list you’ll use the list tag– either <ol> or <ul> depending on if you’re making an ordered or unordered list.

We’re going to make an unordered list, of different types of fruits.

We’ll make our <ul> tag for the list.

Inside the list tag you’ll put your list items. Each item will go inside its own list item tag, written as <li>.

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

So within the apple <li> tag, I’ll add a new <ul> tag under the “apple” text.

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

Child and parent elements
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
To start, we’ll first need a <table> tag. Everything else in the table will be inside this tag.

Inside the table we’ll have table rows, table cells, and table headers for the column headers.

Then we’ll add in the first table row, using the <tr> tag.
    
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
Then in the next row, we’ll add some data for the month of August. Since these are not headers, we will use the <td> tag, for table data.

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
table-missing-cell

If you look at the table in the browser, you can see how the headers now have shifted over one and there’s a weird blank space at the end because there isn’t a table cell there. So let’s put that back.

Table cells can span multiple columns/rows
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
table-months

Tables were used for website layouts
A bit of historical context about tables. Aside from containing data, web developers also used to use tables to layout web designs.

So for example if you have a website design with a header, main content, and a footer, you can create one big table with three rows. And you can then put all your content in those table cells. Table cells can contain any kind of HTML– images, links, text, you name it.

It was very handy back in the day. Nowadays tables aren’t really used very often. The only common exception that I can think of is for HTML emails, because some older email systems can’t use a lot of CSS, so coding like it’s 1999 is unfortunately the only option.


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



