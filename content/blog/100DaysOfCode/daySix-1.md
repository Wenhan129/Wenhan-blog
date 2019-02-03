---
title: Write Better Code in React - Notes
date: '2019-02-03T00:00:03.284Z'
---

<!-- # Write Better Code in React - Notes -->

Okay, tonight I read an interesting article. Well, the title is a self-telling one and I did learn some good stuffs from it.  
[How to Write Better Code in React](https://blog.bitsrc.io/how-to-write-better-code-in-react-best-practices-b8ca87d462b0)

## Linting Tool

> Say you want to reference a new property called this.props.hello in your render() function. Your linter will immediately go red and say: 
> `’hello' is missing in props validation (react/prop-types)`

Yeah, this will become quite useful.
[Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript)
[airbnb react/jsx style guide](https://github.com/airbnb/javascript/tree/master/react)
[eslint-plugin-react](https://www.npmjs.com/package/eslint-plugin-react)

Found an interesting thing from Airbnb’s style guide:

- Ordering for `class extends React.Component`:
  1. optional `static` methods
  2. `constructor`
  3. `getChildContext`
  4. `componentWillMount`
  5. `componentDidMount`
  6. `componentWillReceiveProps`
  7. `shouldComponentUpdate`
  8. `componentWillUpdate`
  9. `componentDidUpdate`
  10. `componentWillUnmount`
  11. _clickHandlers or eventHandlers_ like `onClickSubmit()` or `onChangeDescription()`
  12. _getter methods for `render`_ like `getSelectReason()` or `getFooterContent()`
  13. _optional render methods_ like `renderNavigation()` or `renderProfilePicture()`
  14. `render`

## propTypes and defaultProps

For an _not required_ prop, we need to define it within `defaultProps`. The reason behind this is that if a prop is required, every time we call the component, we are going to pass a value to the prop anyway. But the _not required_ props, the `defaultProps` method guarantees that it will have a value predefined.

## Know when to make new components

> While there aren’t any hard and fast rules on when to move your code into a component, ask yourself:

- Is your code’s functionality becoming unwieldy?
- Does it represent its own thing?
- Are you going to reuse your code?

> If any of these question’s answer is yes, then you need to move your code into a component.
> Keep in mind that the last thing anyone wants to see in your code is a giant 200–300 line component full of crazy bells and whistles.
> Couldn’t agree more. Should keep in the mind often.

## Component vs PureComponent vs Stateless Functional Component

I’ve never ever used a `PureComponent` before.

> Usually, when a component gets a new prop into it, React will re-render that component. But sometimes, a component gets new props that haven’t really changed, but React will still trigger a re-render.
> Using PureComponent will help you prevent this wasted re-render.

I checked an article about the concept behind `PureComponent` and then I found out it will do a shallow value comparison during the `shouldComponentUpdate` method. So it will reduce the unnecessary re-render of the components.

## Use Bit to share components

Never tried that before, sounds like an ad. Will check.

## Use React Dev Tools

No doubt.

## Use Inline Conditional Statements

```jsx
<div className="one-col">
  {isRole('affiliate', user._id) && <MyAffiliateInfo userId={user._id} />}
</div>
```

This is quite inspiring, sometimes I just wrote a pile of very complex spaghetti code for the conditional operations instead using a function and the conditional operators.

## Use Snippet Libraries whenever possible

Why not? Saved a lot time and consistent code format.  
[ES7 React/Redux/GraphQL/React-Native snippets](https://marketplace.visualstudio.com/items?itemName=dsznajder.es7-react-js-snippets)
