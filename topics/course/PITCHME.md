## Course

+++

### What can I expect in the course?

````js
const numbers = [1, 2, 3];
numbers.map(number => number + 1);
numbers.filter(number => number % 2 === 1);
numbers.reduce((result, number) => result + number, 0);
console.log.call(null, 'Hello', 'World!');
console.log.apply(null, ['Hello', 'World!']);
console.log.bind(null, 'Hello', 'World!')();
````

- Version control and JavaScript fundamentals

+++

### What can I expect in the course?

````js
const Example = React.createClass({
	propTypes: {
		location: PropTypes.shape({
			pathname: PropTypes.string.isRequired
		}).isRequired
	}
});
````

- React dataflow and Props

+++

### What can I expect in the course?

````js
componentDidMount: function () {
	return request
		.get(this.props.route.path)
		.end(function (error, response) {
			return error ? error : this.setState({
				data: response.body
			});
		}.bind(this));
}
````

- Handling state and AJAX in React
- React component lifecycle functions

+++

### What can I expect in the course?

````js
function (config) {
	return (
		<Router history={browserHistory}>
			<Route path='/' component={Main}>
				<IndexRoute config={config} component={Home}/>
				<Route path='*' component={NotFound}/>
			</Route>
		</Router>
	);
}
````

- ReactDOM and ReactRouter
- Developing a single page application

+++

### What can I expect from the course?

- Develop your own React application
- Deployed and viewable online
- Fundamental understanding of React

+++?include=topics/questions/PITCHME.md
+++?include=topics/end/PITCHME.md
