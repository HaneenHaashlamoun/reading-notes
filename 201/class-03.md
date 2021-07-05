# HTML

![html](https://www.techfry.com/images/articles/html/html-lists.jpg)

---------------------------
## **HTML Lists**

Types of lists in HTML:

- Unordered List: List of bullet points
- Ordered List: Sequence of numbers or letters instead of bullet points
- Definition List: To specify a term and its definition

![lists](https://i0.wp.com/image.slidesharecdn.com/me-140302002718-phpapp02/95/html-basic-by-abdullaal-baset-8-638.jpg?cb=1393720372?resize=91,91)

------------------------------------------


 A **definition list** is a list of terms and corresponding definitions. Definition lists are typically formatted with the term on the left with the definition following on the right or on the next line. The definition text is typically indented with respect to the term.
- `<dl>` tag defines the description list.
- `<dt>` tag defines data term.
- `<dd>` tag defines data definition (description).

![definition](https://www.wikitechy.com/step-by-step-html-tutorials/img/html-images/code-explanation-definition-list-dl-tag-in-html.png)

-------------------------------------------------

A **nested list** is a list that appears as an element in another list. In this list, the element with index 3 is a nested list. If we print( nested[3] ), we get [10, 20] . ... First, extract the nested list, then extract the item of interest.

![nested](https://i.stack.imgur.com/rqAiC.jpg)

------------------------------------------

## **HTML BOXES**


>In web development, the CSS box model refers to how HTML elements are modeled in browser engines and how the dimensions of those HTML elements are derived from CSS properties. It is a fundamental concept for the composition of HTML webpages. 
*Wikipedia*

![box](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model/box-model-devtools.png)

- Content - The content of the box, where text and images appear
- Padding - Clears an area around the content. The padding is transparent
- Border - A border that goes around the padding and content
- Margin - Clears an area outside the border. The margin is transparent.

** The padding and margin properties are very helpful
in adding space between various items on the page.

**Box Properties and values :**

|Property   |Value      |explaination   |
|-----------|-----------|-------------- |
|Box Dimensions (width, height)| **pixels**,  **percentages**, or **ems**. Traditionally, pixels have been the most popular method because they allow designers to accurately control their size.|box is sized just big enough to hold its  contents. To set your own dimensions for a box you can  use the height and width properties.|
|Limiting Width (min-width, max-width)|**pixels**,  **percentages**, or **ems**.|min-width property specifies the smallest size a box can be displayed at when the browser window is narrow, and the max-width property indicates the maximum width a box can stretch to when the browser window is wide.|
|Limiting Height (min-height, max-height)|**pixels**,  **percentages**, or **ems**.|to limit the width of a box on a page, you may also want to limit the height of it. This is achieved using the  min-height and max-height properties.|
|Overflowing Content (overflow)|- **hidden**: hides any extra content that does not fit in the box / - **scroll**: adds a scrollbar to the box so that users can  scroll to see the missing content.|The overflow property tells the browser what to do if  the content contained within a box is larger than the box itself.|
|Border Width(border-width)|**thin/ medium/ thick**|The border-width property is used to control the width of a border.|
|Border Style (border-style)|`=======>`|![border](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRv_YazNeHEX5pHph95k1KrxDiayCe45JmA9BJFVUdpn88BYL3pZJgkXf9YK6OeSqdkAVE&usqp=CAU)|
|Border Color (border-color)|the color of a border using either RGB values, hex codes or CSS color names|It is possible to individually control the colors of the borders on different sides of a box using: border-top-color/ border-right-color/ border-bottom-color/ border-left-color|
|Shorthand (border)|`=======>`|The border property allows you to specify the width,  style and color of a border in one property (and the  values should be coded in that specific order).|
|Inline/Block (display)|**-inline/ -block/ -inline-block/ -none**|allows you to turn an inline element into a block-level  element or vice versa, and can also be used to hide an element from the page.|
|Hiding Boxes (visibility)|**-hidden/ -visible** |to hide boxes from users but It leaves a space where the element would have been.|

*© Haneen Hashlamoun using Design and Build Websites by Jon Duckett*


