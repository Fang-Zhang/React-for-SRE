#
# Common Mistakes when Design a Component
- Design a Component as a Page
- A Component comprises lots of code(more than one thousand lines)
# Component Design Pattern
## Principle of Design Pattern
- According to the Business Scenario
- Presentational(Stateless functional components) and Container Component Pattern
```js
const ItemsList = (props) => {
    return (
    <ul>
        {props.items.map((item) => (
        <li key={item.id}>
            <a href={item.url}>{item.name}</a>
        </li>
        ))}
    </ul>
    );
};
```
- Provider Pattern
- Compound Components Pattern
- The Higher-Order Components Pattern
- 