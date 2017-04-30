Fundamentals of web development

+++

Your browser

<i class="fa fa-chrome"></i>
<i class="fa fa-firefox"></i>
<i class="fa fa-edge"></i>
<i class="fa fa-safari"></i>
<i class="fa fa-opera"></i>

+++

````html
<html>
	<body>
		<p style="height=50px">Hello World!</p>
		<div><img src="example.png"/></div>
	</body>
</html>
````

+++

````html
<html>
	<body>
		<p style="height=50px">Hello World!</p>
		<div><img src="example.png"/></div>
	</body>
</html>
````

![DOM Rendering](assets/img/dom.png)

+++

Steps to render:

- Generates a Document Object Model (DOM) |
- Generates a CSS Object Model (CSSOM) |
- Layout coordinate calculation |
- Painting (the rendering) |

+++

When a style is changed:

````html
<html>
	<body>
		<p style="height=40px">Hello World!</p>
		<div><img src="example.png"/></div>
	</body>
</html>
````

- Repainting (only the <p> tag) |

+++

When a the structure is changed:

````html
<html>
	<body>
		<div><img src="example.png"/></div>
		<p style="height=40px">Hello World!</p>
	</body>
</html>
````

- Reflow (layout calculation + repainting) |

+++

Your browser will try to optimize

- Layout calculation, painting is expensive

+++

Hypertext Markup Language (HTML)

- Defines structure of a webpage
- HTML elements are the building blocks

Cascading Style Sheets (CSS)

- Defines the styles

JavaScript (JS)

- Coordinates the interactions on a page

+++

Think in a play:

+++

Resources

- [How browsers work](https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/)
- [Web page rendering 101](http://frontendbabel.info/articles/webpage-rendering-101/)
