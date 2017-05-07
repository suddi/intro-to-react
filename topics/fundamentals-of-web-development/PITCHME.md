## Fundamentals of web development

+++

````html
<html>
	<head>
		<style text="text/css">
			.button {
				height: 100px;
				text-align: center;
				width: 100%;
			}
		</style>
		<script type="text/javascript">
			function handleClick() {
				alert('Hello World!');
			}
		</script>
	</head>
	<body>
		<button
			id="app" class="button" onclick="handleClick()">
			Click me
		</button>
	</body>
</html>
````

[See the code](https://jsfiddle.net/suddi/xmj93Lzd/)

+++

### Hypertext Markup Language (HTML)

````html
<html>
	<head>
		<style type="text/css"></style>
		<script type="text/javascript"></script>
	</head>
	<body>
		<button
			id="app" class="button" onclick="handleClick()">
			Click me
		</button>
	</body>
</html>
````

- Defines structure of a webpage
- HTML elements are the building blocks

+++

### Cascading Style Sheets (CSS)

````css
.button {
	height: 100px;
	text-align: center;
	width: 100%;
}
````

- Defines the styles

+++

### JavaScript (JS)

````js
function handleClick() {
	alert('Hello World!');
}
````

- Coordinates the interactions on a page

+++

### Consider a play

- HTML is the script |
- CSS is the costumes |
- JS is the director |
- Then who is the actor? |

+++

### Your browser

<i class="fa fa-chrome"></i>
<i class="fa fa-firefox"></i>
<i class="fa fa-edge"></i>
<i class="fa fa-safari"></i>
<i class="fa fa-opera"></i>

+++

### How does your browser render?

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
<br/>
- Repainting only the element |

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
<br/>
- Reflow (layout calculation + repainting) |

+++

Your browser will try to optimize
<br/>
- Layout calculation, painting is expensive

+++

### Resources

- [How browsers work](https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/)
- [Web page rendering 101](http://frontendbabel.info/articles/webpage-rendering-101/)
