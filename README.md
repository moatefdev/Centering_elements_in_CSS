This repo includes the files of the images and codes I used in my blog and in dev.to which taking about How to center elements in CSS easily in many diiferent ways?
[My blog link](https://codingtips5.home.blog/)
[Dev.to link](https://dev.to/mohamed_gt57/how-to-center-elements-in-css-46nc)

## [Table Of Contents](#top)
   1. **[Introduction](#intro)**
   2. **[Horizontally: Centering Inline Elements](#center-inline-ele)**
   3. **[Horizontally: Centering Block Elements](#center-block-ele)**
   4. **[Horizontally: Centering More Than Block Elements](#center-multi-block-ele)**
   5. **[Vertically: Centering Inline Element - Single Line](#center-v-singleline)**
   6. **[Vertically: Centering Inline Element - Multiple lines](#center-v-multi-inlineele)**
   7. **[Vertically: Center Block Element With known Height](#center-v-knownH)**
   8. **[Vertically: Center Block Elements with unknown Height](#center-v-unknownH)**
   9.  **[Vertically: Center Block Elements Using Flexbox](#center-v-flexbox)**
   10. **[Both Horizontal & Vertical: Fixed Height and Width](#center-both-fixedHW)**
   11. [**Both Horizontal & Vertical : Unknown Height and Width**](#center-both-unknownHW)
   12. [**Both Horizontal & Vertical: Using Flexbox**](#center-both-flexbox)
   13. [**Both Horizontal & Vertical: Using CSS Grid**](#center-both-grid)
   14. [**Conclusion**](#conclusion)

<a href="https://dev.to/mohamed_gt57/how-to-center-elements-in-css-46nc/#center-inline-ele"><h2 id="intro">1 - Introduction</h2></a>

In this post you will learn how to center elements in CSS in many different ways, but before we get started please notice that we will use some advanced techniques in __*CSS3*__ like: __*flexbox*__ and __*grid*__ and those techniques are not explained in this post so I will provide some source in the Conclusion section below at the end of that post, so you can learn more about them and You will find the source files in [**Github.com**](https://github.com/moatefdev/Centering_elements_in_CSS)

Horizontally

* * *

<a href="https://dev.to/mohamed_gt57/how-to-center-elements-in-css-46nc/#center-inline-ele"><h2 id="center-inline-ele">2 - Horizontally: Centering Inline Elements</h2></a>

In this method I will use **_text-align: center;_** technique.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/c2gcmk43ikbfa4iz0ag1.png)

<a href="https://dev.to/mohamed_gt57/how-to-center-elements-in-css-46nc/#center-block-ele"><h2 id="center-block-ele">3 - Horizontally: Centering Block Elements</h2></a>

In the method I will use **_margin: auto_** technique.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/awiy56exdjwnp4hjao5s.png)

<a href="https://dev.to/mohamed_gt57/how-to-center-elements-in-css-46nc/#center-multi-block-ele"><h2 id="center-multi-block-ele">4 - Horizontally: Centering More Than Block Elements</h2></a>

In this method we do not have just one technique as we did before but we have 3 techniques to center the elements horizontally.

Techniques used:

1. display: inline-block;
2. display: flex; and justify-content; center for the parent element.
3. margin: auto (as we did before).

Technique 1 & Technique 2 (Same result):

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/0rsptko3wctgjch5467p.png)

Technique 3:

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/ory2z5qnrmr92pte0503.png)

[**⬆ Go to top ⬆**](https://dev.to/mohamed_gt57/how-to-center-elements-in-css-46nc/#top)

Vertically

* * *

<a href="https://dev.to/mohamed_gt57/how-to-center-elements-in-css-46nc/#center-v-singleline"><h2 id="center-v-singleline">5 - Vertically: Centering Inline Element - Single Line</h2></a>

In this method we will use two techniques for centering; first, we will use **_padding: ( top and bottom )_** values to center the content inside the element vertically, and also use **_line-height: with the same value of the height_** after setting the height value.

For example:

1. **_padding: 10px 0;_** **Notice:** it is not matter to set the left and right value as I set to 0 in this example because it will not effect the centering of the content of an element vertically, but only the value of the padding top and bottom will center the content vertically.
2. **_line-height:_** if you set the height of an element to 100px, so you have to set the value of the line-height prop (for property) to 100px too and if you set the height to 200px you will also need to set the line-height prop to 200px and so on.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/ydikiot2my3so1js9qk4.png)

<a href="https://dev.to/mohamed_gt57/how-to-center-elements-in-css-46nc/#center-v-multi-inlineele"><h2 id="center-v-multi-inlineele">6 - Vertically: Centering Inline Element - Multiple lines</h2></a>

**Part 1:** In this method we will use 3 techniques to center the elements vertically.

1 - Using a **_table_** **tag in HTML** will align the element vertically without writing any CSS code/style that is because the table element has its default CSS prop "**_vertical-align: middle;_**" which we will use in the next method.

2 - Setting a **_display: table;_** to the parent element (a <div> for example) and then setting a **_display: table-cell;_** and **_vertical-align: middle;_** to the child element(s); **Notice**: by setting a display: table; to an element in this way you are telling the browser to render the element as a **_table_** element, in brief display: table; Lets the element behave like a table element; By setting the display: table-cell; and vertical-align: middle; to the child element so it will behave as a **_td_** inside/nested in a **_tr_** element.

For more information about display prop with its all props and vertical-align prop.

* Display: table; and display: table cell in [W3](https://www.w3schools.com/cssref/pr_class_display.asp) and [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/display).

* Vertical-align: in [W3](https://www.w3schools.com/cssref/pr_pos_vertical-align.asp), [CSS Tricks](https://css-tricks.com/almanac/properties/v/vertical-align/) and [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/vertical-align).

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/n1z8a59bhngdncvybmq5.png)

**Part 2:** In this method we will use another technique called " ghost element ".

This technique is a full-height pseudo-element is placed inside the container and the text is vertically aligned with that pseudo-element.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/54uncmylfkff3lt9o8gz.png)

<a href="https://dev.to/mohamed_gt57/how-to-center-elements-in-css-46nc/#center-v-knownH"><h2 id="center-v-knownH">7 - Vertically: Center Block Element With known Height</h2></a>

In this method we will use **_position_** prop **_and margin-top_** with a negative value to center the element vertically, **In case of we know the height of the element.**

For example:

If we want to center a **_paragraph_** inside a **_div_** we will give the **_div_** which is the parent element a **position: relative;** and the **_p_** which is the child element a **position: absolute;** and a margin-top: and the value will be equal to the height of the element **_p_** but in a negative value. so if the paragraph's height is 50px we will set the **margin-top: -25px**;

**Please note:** that if you set a padding prop to the child element you will need to increase the margin-top as a negative value as well. For example: if you set the padding to 20px you will need to set the margin-top to -35px.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/8d8gf7n7ebp36ih8mfmy.png)

<a href="https://dev.to/mohamed_gt57/how-to-center-elements-in-css-46nc/#center-v-unknownH"><h2 id="center-v-unknownH">8 - Vertically: Center Block Elements with unknown Height</h2></a>

In this method we will use **transform: translate(**x, **y);** technique as a negative value for y.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/c86m5qqdxxgn9j34774k.png)

<a href="https://dev.to/mohamed_gt57/how-to-center-elements-in-css-46nc/#center-v-flexbox"><h2 id="center-v-flexbox">9 - Vertically: Center Block Elements Using Flexbox</h2></a>

In this method we will use the **_Flexbox_** technique to center element vertically.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/ild921sav99xvxrzq8jo.png)

<a href="https://dev.to/mohamed_gt57/how-to-center-elements-in-css-46nc/#center-both-fixedHW"><h2 id="center-both-fixedHW">10 - Both Horizontal & Vertical : Fixed Height and Width</h2></a>

In this method we will use some techniques same as the techniques we use before in this post you can make sure from the sources on Github the link in the Intro section at the top.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/bzjd0jp0vjzg8857794y.png)

<a href="https://dev.to/mohamed_gt57/how-to-center-elements-in-css-46nc/#center-both-unknownHW"><h2 id="center-both-unknownHW">11 - Both Horizontal & Vertical : Unknown Height and Width</h2></a>

In this method we will also use some techniques same as the techniques we use before in this post you can make sure from the sources on Github the link in the Intro section at the top.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/qkb1qzwhtk276vox3lte.png)

<a href="https://dev.to/mohamed_gt57/how-to-center-elements-in-css-46nc/#center-both-flexbox"><h2 id="center-both-flexbox">12 - Both Horizontal & Vertical: Using Flexbox</h2></a>

In this method we will use **_flexbox_** technique.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/wfz96rkjgxde5yib2hbw.png)

<a href="https://dev.to/mohamed_gt57/how-to-center-elements-in-css-46nc/#center-both-grid"><h2 id="center-both-grid">13 - Both Horizontal & Vertical: Using CSS Grid</h2></a>

In the method we will use **_CSS Grid_** technique to center the element horizontally and vertically. For more information about CSS Grid look at the conclusion section below at the end of this post.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/iq026mepe44xzv06fasx.png)

[**⬆ Go to top ⬆**](https://dev.to/mohamed_gt57/how-to-center-elements-in-css-46nc/#top)

<a href="https://dev.to/mohamed_gt57/how-to-center-elements-in-css-46nc/#conclusion"><h2 id="conclusion">14 - Conclusion</h2></a>

Now, you can totally center elements in CSS with many different way so easy.

And before you go, let me tell please share this post if you benefited from it and Happy New Year 🎄❄💖🎁🎄 Merry Christmas!

**The source of this post**: **[Unique Coderz Academy](https://www.youtube.com/playlist?list=PLtFbQRDJ11kE--j12SU0X5pnXiM0WsWVQ)** Youtube channel but in **_Arabic_** Language.

**For other resources:**

* Centering in CSS: in [CSS Tricks](https://css-tricks.com/centering-css-complete-guide/), [W3](http://w3schools.com/css/css_align.asp) and [FCC](https://www.freecodecamp.org/news/how-to-center-things-with-style-in-css-dc87b7542689/)
* [Flexbox 30](https://github.com/samanthaming/Flexbox30)
* [A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
* [What The Flexbox?!](https://flexbox.io/)
* [MDN web docs: Flexbox](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox)
* [MDN web docs: Basic Concepts of flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox)
* [Yoksel: Flex Cheatsheet](https://yoksel.github.io/flex-cheatsheet/)
* [JoniBologna.com: Flexbox Cheatsheet](http://jonibologna.com/flexbox-cheatsheet/)
* [A Complete Guide to Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)
* [CSS Grid](https://cssgrid.io/)
