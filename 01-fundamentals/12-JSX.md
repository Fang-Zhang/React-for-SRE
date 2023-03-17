## 1 One Sentence Explanation
JSX is a syntax sugar for Javascript, React doesn't force developer using JSX.<br>
We could implement React like below:
```js
class Hello extends React.Component {
    render() {
        return React.createElement('div', null, 'Hello ${this.props.toWhat}');
    }
}

ReactDOM.render(
    React.createElement(Hello, {toWhat: 'Hello'}, null),
    document.getElementById('root')
);
```
But with support of JSX, we could implement it like this:
```js
class Hello extends React.Component {
    render() {
        return <div>Hello ${this.props.toWhat}</div>;
    }
}

ReactDOM.render(
    <Hello toWhat="Hello" />,
    document.getElementById('root')
);
```
## 2 Core Concept
React doesn't want to import too many new concept and just inherit from exiting JS syntax.<br>

## 3 Solution Comparison (Separation of Concerns)
- Template: Bring lots of new concepts(like AngularJS) and weaken the separation of concerns.
- Template String: Bring complex structure description and no syntax prompt.
- JXON: Weak syntax prompt.

## 4 How to convert JSX into JS through Babel
[How](https://legacy.reactjs.org/blog/2020/09/22/introducing-the-new-jsx-transform.html#:~:text=Browsers%20don't%20understand%20JSX,JSX%20transform%20under%20the%20hood.)