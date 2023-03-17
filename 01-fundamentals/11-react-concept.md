# React Concept: What's the React? (or How to understand React?)
## 1 One Sentence Explanation <br>
React is a JS library for building UI, try to resolve the reuse of view level through the components.<br>
So, its essential is a component framework, and its thinking model is:<br>

> View = fn (props, state, context)<br>

**fn**: Could be class component, pure function component, or side effect.<br>
There are only **components** in React, no pages, no controllers, no models.<br>
<br>

## 2 It's **core concepts** are:<br>

- **Declarative**:<br>
Pretty straightforward, it's easy to understand and compose it. And making code more predictable and easier to debug. If using code illustration, you could find out the benefit as below:<br>

Change:
```html 
<div class="block" />
```
```js
const block = $('.block');
block.css('color', 'green');
```
to<br>
```js
const Block = (props) => <div style={{color: 'green'}} />;
```
- **Component-Based**:<br>
Build encapsulated components that manage their state, then compose them to make complex UIs. That means: low coupling in the system, high cohesion in each function.<br>

- **Learn Once, Write Anywhere**:<br>
No assumption about other technology stack, so you can develop new features in React without rewriting existing code. Meanwhile, React can render on server using Node, and power mobile apps using React Native(of course, React 360 for VR and Electron for desktop are the instances as well). Specificity, they are all benefit from the virtual DOM.<br>

## 3 Disadvantage:<br>
React is just a library, not a comprehensive framework. Some spots, React doesn't implement them by itself, but leave them to the community, such as [React Route](https://reactrouter.com/en/main), [Component Test](https://www.freecodecamp.org/news/testing-react-hooks/). These increase the learning curve about he [Eco-System of React](#EcoSystem).