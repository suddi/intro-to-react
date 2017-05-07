## Workshop

+++

In 7 steps, we're going to go from nothing to our 1st React app

+++

Signup at [codenvy.io](https://codenvy.io/site/login)

It's free

+++

### NPM

- A package manager for JavaScript |
- A means for developers to share code with each other |
- React is also on NPM |

+++

### Step 1

````sh
npm init

# name: My First React App
# version: (1.0.0)
# description:
# entry point: (index.js) app/index.js
# test command:
# git repository:
# keywords:
# author: Suddi
# license: (ISC)

````

+++

You should have a file named `package.json`:

````json
{
	"name": "My First React App",
	"version": "1.0.0",
	"description": "",
	"main": "app/index.js",
	"scripts": {
		"test": "echo \"Error: no test specified\" && exit 1"
	},
	"author": "Suddi",
	"license": "ISC"
}
````

+++

### Step 2

````sh
npm install --save-dev \
	react@^15.5.4 \
	react-dom@15.5.4 \
	webpack@2.4.1 \
	babel-core@6.24.1 \
	babel-loader@6.4.1 \
	babel-preset-react@6.24.1
````

+++

Your `package.json` file should now look like this:

````json
{
	"name": "My First React App",
	"version": "1.0.0",
	"description": "",
	"main": "app/index.js",
	"scripts": {
		"test": "echo \"Error: no test specified\" && exit 1"
	},
	"author": "Suddi",
	"license": "ISC",
	"devDependencies": {
		"babel-core": "6.24.1",
		"babel-loader": "6.4.1",
		"babel-preset-react": "6.24.1",
		"react": "15.5.4",
		"react-dom": "15.5.4",
		"webpack": "2.4.1"
	}
}
````

+++

### Step 3

Create a file `public/index.html`:

````html
<html>
<html>
	<head>
	    <title>My First React App</title>
	    <style>
	        .button {
	            height: 100px;
		        text-align: center;
		        width: 100%;
	        }
	    </style>
	</head>
	<body>
	    <div id="app"></div>
	    <script src="bundle.js"></script>
	</body>
</html>
````

+++

### Step 4

Create a file `app/index.js`:

````js
const React = require('react');
const ReactDOM = require('react-dom');

const ClickMe = React.createClass({
    handleClick: function () {
        return alert('Hello World!');
    },

    render: function () {
        return (
            <button
                className="button"
                onClick={this.handleClick}>
                Click me
            </button>
        );
    }
});

ReactDOM.render(
    <ClickMe/>,
    document.getElementById('app')
);
````

+++

### Step 5

Create one more file `webpack.config.js`:

````js
module.exports = {
    entry: [
        './app/index.js'
    ],

    output: {
        filename: './public/bundle.js'
    },

    module: {
        rules: [
            {
                test: /\.js$/,
                include: __dirname + './app',
                loaders: ['babel-loader']
            }
        ]
    }
};
````

+++

### Step 6

Add a line in `package.json` to allow NPM to build our React project:

````js
"scripts": {
    "build": "webpack",
    "test": "echo \"Error: no test specified\" && exit 1"
}
````

+++

### Step 7

Let's run it!

````sh
npm run build
````

+++

Your site is ready...
