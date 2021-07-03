# HTML 



![HTML](https://pixelmechanics.com.sg/wp-content/uploads/2019/06/html5-logo-for-web-development-1200x667.png)

----------------------------------

### What is HTML?

Known as “Hypertext Markup Language”, it is a standardised system for tagging text files to achieve font, colour, graphic and hyperlink effects on World Wide Web (WWW) pages. Other technologies besides HTML are used to describe a web page’s look (CSS) or interaction (JavaScript).

**PS**: for the **JavaScript** page click **[here](https://haneenhaashlamoun.github.io/reading-notes/201/class-01a)** 

HTML job is to describes the structure of pages.
The HTML code is made up of characters that live inside angled
brackets (`<>`) ; Tags are often referred to as elements.
Tags usually come in pairs (example : `<p></p>`). The opening tag (`<p>`)and the closing tag (`</p>`) , Each HTML element tells the browser something about the information that sits between its opening and closing tags.



### Structure of HTML Page 
#### **Body, Head & Title**

*for example :*


>`<html>`
>
>`<head>`
>
>`<title> Title of the Page </title>`
>
>`</head>`
>
>`<body>`
>
>`<h2> Sub-Heading </h2>`
>
>`<h1> Heading </h1>`
>
>`<p> Paragraph <p>`
>
>`</body>`
>
>`</html>`

#### **Tags Attributes** 

**Attributes define additional characteristics or properties of the element such as width and height of an image. Attributes are always specified in the start tag (or opening tag) and usually consists of name/value pairs like name="value" . Attribute values should always be enclosed in quotation marks.**


![HTMLTAG](https://tutorial.techaltum.com/images/element.png)

### Creating My First WebPage

Web pages can be created and modified by using professional HTML editors.
However, for learning HTML we recommend a simple text editor like Notepad (PC) or TextEdit (Mac). 

Here is the steps to explain :

- Open text editor .

- Some HTML *(for example put the above code)*.
!["notepad"](https://www.w3schools.com/html/img_notepad.png)

- Save the HTML Page :
Save the file on your computer. Select File > Save as in the Notepad menu.
Name the file "index.htm" and set the encoding to UTF-8 (which is the preferred encoding for HTML files).
![save](https://www.w3schools.com/html/img_saveas.png)

- View the HTML Page in Your Browser, The result will look much like this:
![page](https://www.w3schools.com/html/img_chrome.png)

PS : To learn HTML you need to know what tags are
available for you to use, what they do, and where they
can go. Here is a link to learn more about it *[HTML Tags](https://www.w3schools.com/TAGS/default.ASP)*.


---------------------------------------------

### HTML Versions 

Since the web was first created, there have
been several different versions of HTML.
Each new version was designed to be an improvement on the last (with new elements and attributes added and older code
removed).



![versions](https://cdn.educba.com/academy/wp-content/uploads/2019/07/Versions-of-Html.png.webp)

|version       |Release Date  |Features      | 
|--------------|--------------|--------------|
| HTML4        |Released 1997 |Although HTML 4 had some presentational elements to control the appearance of pages, authors are not recommended to use them any more. (Examples include the `<center>` element for centering content on a page, `<font>` for controlling the appearance of text, and `<strike>` to put a line through the text — all of these can be achieved with CSS instead.)|
| XHTML1.0      |Released 2000 |In 1998, a language called XML was published. Its purpose was to allow people to write new markup languages. Since HTML was the most widely used markup language around, it was decided that HTML 4 should be reformulated to follow the rules of XML and it was renamed XHTML. This meant that authors had to follow some new, more strict rules about writing markup For example:1. Every element needed a closing tag (except for empty elements such as `<img />`). 2- Attribute names had to be in lowercase. etc... It could also  be used with other data formats such as Scalable Vector Graphics (SVG) — a graphical language written in XML, MathML (used to mark up mathematical formulae), and CML (used to mark up chemical formulae).|
| HTML5        |Released 2000 |In HTML5, web page authors  do not need to close all tags, and new elements and  attributes will be introduced. At the time of writing, the HTML5 specification had not been completed, but the major  browser makers had started to implement many of the new  features, and web page authors were rapidly adopting the new markup.|


### DOCTYPEs
Because there have been several versions of HTML, each web page should begin with a DOCTYPE declaration to tell a browser which version of HTML the page is using (although browsers usually display the page even if it is not included).

- HTML5: 
>`<!DOCTYPE html>`

- HTML4: 
>`<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional// EN" "http://www.w3.org/TR/html4/loose.dtd">`.

- Transitional XHTML 1.0: 
>`<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0  Transitional//EN""http://www.w3.org/TR/xhtml1/DTD/ xhtml1-transitional.dtd">`.

- Strict XHTML 1.0: 
>`<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0  Strict//EN""http://www.w3.org/TR/xhtml1/DTD/ xhtml1-Strict.dtd">`.

- XML Declaration: 
>`<?xml version="1.0" ?>`.


![evolution](https://image.slidesharecdn.com/html5sgce2012-120626104830-phpapp02/95/everything-you-need-to-know-about-html5-in-15-min-3-728.jpg?cb=1340710247)

### Comments IN HTML 

If you want to add a comment to your code that will not be visible in the  user's browser, you can add the text between these characters like this:

`<!-- comment goes here -->`

### Other HTML Features 
### (Attributes & Elements)


- The id and class attributes allow you to identify
particular elements.
- The `<div>` and `<span>` elements allow you to group
block-level and inline elements together.
- `<iframes>` cut windows into your web pages through
which other pages can be displayed.
- The `<meta>` tag allows you to supply all kinds of
information about your web page.
- Escape characters are used to include special
characters in your pages such as <, >, and ©.

--------------------------

## HTML5 Layout

 - Traditional HTML Layouts 
 For a long time, web page authors used `<div>` elements to group together related elements on the page (such as the elements that form a header, an article, footer or sidebar). Authors used class or id attributes to indicate  the role of the `<div>` element in the structure of the page.

- New Html 5 Layout Elements
HTML5 introduces a new set of elements that allow you to divide up the parts of a page. The names of these elements indicate the kind of content you will find  in them. They are still subject to change, but that has not stopped many web  page authors using them already.

**These are some elements of HTML5**
- Headers & Footers `<header> <footer>`
- Navigation `<nav>`
- Articles `<article>`
- Asides `<aside>`
- Sections `<section>`
- Heading Groups `<hgroup>`
- Figures `<figure> <figcaption>`
- Sectioning Elements `<div>`


**Helping Older Browsers Understand**

Older browsers that do not know the new HTML5 elements will automatically treat them as inline elements. Therefore, to help older browsers, you should include  the line of CSS on the left which states which new elements should be rendered  as block-level elements. 
You do not need to understand JavaScript to use it. You can just link to a copy that Google hosts on its servers. It should be placed inside a conditional comment which checks if the browser version is less than (hence the lt) IE9.

>`<!--[if lt IE 9]>`
>`<script src="http://html5shiv.googlecode.com/svn/trunk/html5.js"></script>`
>`<![endif]-->`

----------------------------
----------------------------

*LAST But not LEAST*

## Process & Design

- **You need to know How to approach building a site**
- **You need to Understanding your audience and their needs**
- **You need to know How to present information visitors want to see**

#### **Step 1 : you need to ask these questions :**

- Who is the Site For? 
Every website should be designed for the target audience—not just for yourself  or the site owner. It is therefore very important to understand who your target audience is.

- Why People Visit YOUR Website ?
Now that you know who your visitors are, you need to consider why they are  coming. While some people will simply chance across your website, most will  visit for a specific reason.

- What Information Your Visitors Need ?
You know who is coming to your site and why they are coming, so now you need to work out what information they need in order to achieve their goals quickly and effectively.

- How Of ten People Will Visit Your Site ?
Some sites benefit from being updated more frequently than others. Some  information (such as news) may be constantly changing, while other content  remains relatively static.


#### **Step 2 : Site Maps**

Now that you know what needs to appear on your site, you can start to organize  the information into sections or pages.

![sitemap](https://justmakeawebsite.com/wp-content/uploads/2020/05/sitemap-template.jpg)


#### **Step 3 : WireFrames**
A wireframe is a simple sketch of the key information that needs  to go on each page of a site. It shows the hierarchy of the  information and how much space it might require.

![WireFrames](https://i.pinimg.com/originals/08/66/8b/08668befd34d816306ca9013a1ae9e3d.png)

#### **Step 4 : Getting your message across using design**

The primary aim of any kind of visual design is to communicate.  Organizing and prioritizing information on a page helps users  understand its importance and what order to read it in.
and you need to cover these 3 points :

    1- CONTENT: Web pages often have a lot of information to communicate.
    
    2- Prioritizing: By making parts of the page look distinct from surrounding content, designers draw attention to (or away from) those items.

    3- Organizing: Grouping together related content into blocks or chunks makes the page look simpler (and easier to understand).

#### **Step 5 : Visual hierarchy**

Most web users do not read entire pages. Rather, they skim to find
information. You can use contrast to create a visual hierarchy that gets
across your key message and helps users find what they are looking for.
By controling (Size, Color and Style)

Visual hierarchy refers to the order in which your eyes perceive what
they see. It is created by adding visual contrast between the items being
displayed. Items with higher contrast are recognized and processed first.

*example for step 4 & 5*

![webpage](https://i.pinimg.com/originals/be/bc/33/bebc33eb19d2142725256746f892d1cd.jpg)


#### **Step 6 : grouping and Similarity**

When making sense of a design, we tend to organize visual elements
into groups. Grouping related pieces of information together can make a
design easier to comprehend. Here are some ways this can be achieved.


#### **Step 7 : Designing Navigation**

Site navigation not only helps people find where they want to go, but also
helps them understand what your site is about and how it is organized.
Good navigation tends to follow these principles...

- **Concise** Ideally, the navigation should be quick and easy to read. It is a good idea to try to limit the number of options in a menu to no more  than eight links. These can link to section homepages which in turn link to other pages.

- **Clear** Users should be able to predict the kind of information that they will find on the page before clicking on the link. Where possible,  choose single descriptive words for each link rather than phrases.

- **Selective** The more pages a site contains, the larger the number of navigation items there will be. Although secondary navigation will change  from page to page, it is best to keep the primary navigation exactly the  same.

![navbar](https://www.orbitmedia.com/wp-content/uploads/2016/09/website-navigation-primary-nav.jpg)


all rights reserved to Copyright: © *HTML & CSS Design and Build Websites* by **Jon Duckett**
