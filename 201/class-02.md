# HTML 



![HTML](https://pixelmechanics.com.sg/wp-content/uploads/2019/06/html5-logo-for-web-development-1200x667.png)

----------------------------------

When creating a web page, you add tags (known as markup) to the contents of the page. These tags provide extra  meaning and allow browsers to show users the appropriate structure for the page.

The main two types of tags:
### **Structural markup**: the elements that you can use to describe both headings and paragraphs

- **Headings:**  `<h1>` `<h2>` ... `<h6>`
![heading](https://www.seoptimer.com/blog/wp-content/uploads/2018/09/header-tags-min.png)

- **Paragraphs:`<p>`**
To create a paragraph, surround the words that make up  the paragraph with an opening `<p>` tag and closing `</p>` tag.
you can control the style of it with the tags :
`<b>` `<i>` `<sup>` `<sub>`
just like this:
![p](https://t4tutorials.com/wp-content/uploads/2017/02/text-formating-in-html.png)

- **Line Breaks & Horizontal Rules**
    1. `<br/>` if you wanted to add a line break inside the middle of a paragraph you can use the line break tag `<br/>`.

    2. `<hr/>` To create a break between themes such  as a change of topic in a book or a new scene in a  play you can add a horizontal rule between sections using the `<hr/>` tag.

- **Visual Editors & Their Code views:**
Content management systems and HTML editors such as  Dreamweaver usually have two views of the page you are  creating: a visual editor and a code view.

    1. *Visual editors* often resemble word processors.  Although each editor will differ slightly, there are some features that are common to most editors that  allow you to control the presentation of text.
    ![visual](https://www.drupal.org/files/project-images/classic_example_0.png)
    
    2. *Code views* show you the code created by the  visual editor so you can manually edit it, or so you  can just enter new code yourself. It is often activated using a button with an icon that says HTML 
    or has angled brackets. White space may be added to  the code by the editor to make the code easier to read.
    ![code](https://www.drupal.org/files/issues/view-beforepatch.png)

    

### **Semantic markup**: which provides extra information; such as where emphasis is placed in a sentence, that  something you have written is a quotation (and who said  it), the meaning of acronyms, and so on.
There are some text elements that are not intended to affect the
structure of your web pages, but they do add extra information to the
pages — they are known as semantic markup.

- **Strong & Emphasis:** `<strong>` + `<em>`
    1. By default, browsers will show the contents of a  `<strong>` element in bold.
    2. By default browsers will show the contents of an  `<em>` element in italic.
    ![b](https://i.ytimg.com/vi/aivHOczcXzQ/maxresdefault.jpg)

- **Quotations:** `<blockquote>` + `<q>`
    1. The `<blockquote>` element is used for longer quotes that  take up an entire paragraph. Note how the `<p>` element is  still used inside the `<blockquote>` element.
    2. The `<q>` element is used for shorter quotes that  sit within a paragraph. Browsers are supposed to put  quotes around the `<q>` element, however Internet  Explorer does not — therefore many people avoid using the `<q>` element.

- **Abbreviations & Acronyms:** `<abbr>` 
If you use an abbreviation or an acronym, then the `<abbr>` element can be used. A title attribute on the  opening tag is used to specify the full term.

- **Citations & Definitions:** `<cite>` + `<dfn>`
    1. In HTML5, <cite> should not really be used for a  person's name — but it was allowed in HTML4, so most  people are likely to continue to use it. 

    2. The `<dfn>` element is used to indicate the  defining instance of a new term.

![tags](https://image4.slideserve.com/7536495/html-quotation-and-citation-elements-l.jpg)


- **Author Details:** The `<address>` element has quite a  specific use: to contain contact details for the author of the page.

- **Changes to Content:** 
    1. The `<ins>` element can be used to show content that has been inserted into a document,  while the `<del>` element can show text that has been  deleted from it.
    2. `<s>` The `<s>` element indicates something that is no longer accurate or relevant (but that should not be deleted). Visually the content of an `<s>` element will  usually be displayed with a line through the center.

    










