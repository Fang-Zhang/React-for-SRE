# Class Component VS Functional Component
## Common Points
- Final Usage: No matter [HOC(Higher-Order Component)](https://reactjs.org/docs/higher-order-components.html), or asynchronous invoke, both of them could be the basic component for UI rendering. Based on this, the invoke method and final display result is same for both of them. Customers could differentiate them just from daily using.
## Different Points
- Scenario
- Special feature:<br>
  Class Component -> Support inherit<br>
  Functional Component -> Doesn't support inheritance, but low coupling
- Design Pattern:<br>
  Class Component -> OOP(Object Oriented Programming), wrap the business logic in the life cycle.<br>
  Functional Component -> FP(Functional programming), split the rendering and business logic.<br>
```js
const PostList = ({posts}) => (
    <ul>{posts.map((post) => <li>{post.title}</li>)}</ul>
)
const PostListWithData = lifecycle({
    componentDidMount(){
        fetchPosts().then(posts => {this.setState({posts})})
    }
})(PostsList);
```
vs
```js
import React, { useState, useEffect } from 'react';

function App (){
    const [data, setData] = useState({posts:[]});
    useEffect(
        async() => {
            const result = await fetchPosts();
            setData(result.data);
        },[]
    );

    return(
        <ul>{data.posts.map((post => <li>{post.title}</li>))</ul>
    )
}

export default App;
```
- Future Trend: Functional Component -> Hooks<br>
  Because **this** is hard to maintain, and business logic is distributed around all life cycles.<br>