# HTML 



![HTML](https://pixelmechanics.com.sg/wp-content/uploads/2019/06/html5-logo-for-web-development-1200x667.png)

----------------------------------

### What is HTML?

Known as “Hypertext Markup Language”, it is a standardised system for tagging text files to achieve font, colour, graphic and hyperlink effects on World Wide Web (WWW) pages. Other technologies besides HTML are used to describe a web page’s look (CSS) or interaction (JavaScript).
HTML job is to describes the structure of pages.
The HTML code is made up of characters that live inside angled
brackets (`<>`) ; Tags are often referred to as elements.
Tags usually come in pairs (example : `<p></p>`). The opening tag (`<p>`)and the closing tag (`</p>`) , Each HTML element tells the browser something about the information that sits between its opening and closing tags.



### Structure of HTML Page 
#### **Body, Head & Title**

*for example :*


`<html>`

`<head>`

`<title> Title of the Page </title>`

`</head>`

`<body>`

`<h2> Sub-Heading </h2>`

`<h1> Heading </h1>`

`<p> Paragraph <p>`

`</body>`

`</html>`

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

- HTML5: `<!DOCTYPE html>`

- HTML4: `<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional// EN" "http://www.w3.org/TR/html4/loose.dtd">`.

- Transitional XHTML 1.0: `<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0  Transitional//EN""http://www.w3.org/TR/xhtml1/DTD/ xhtml1-transitional.dtd">`.

- Strict XHTML 1.0: `<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0  Strict//EN""http://www.w3.org/TR/xhtml1/DTD/ xhtml1-Strict.dtd">`.

- XML Declaration: `<?xml version="1.0" ?>`.


![evolution](https://image.slidesharecdn.com/html5sgce2012-120626104830-phpapp02/95/everything-you-need-to-know-about-html5-in-15-min-3-728.jpg?cb=1340710247)


