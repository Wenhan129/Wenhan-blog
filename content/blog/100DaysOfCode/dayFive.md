---
title: 17 Creating Items with Mutations - Notes
date: '2019-02-02T00:00:03.284Z'
---

# Day Five - 100 DaysOfCode

- form
- fieldset
- onChange handler to change the value bound with state.
  Here what inspired me from Wes’s code is he used one single function to handle all the changes from various input.

```jsx
handleChange = e => {
  const { name, type, value } = e.target

  const val = type === 'number' ? parseFloat(value) : value
  this.setState({ [name]: val })
}
```

So the only thing that we need to do is to assign different values to the name attributes of the forms.

- onSubmit - Don’t forget the preventDefault()!
- export the queries and mutations.
- A very strange format of a mutation:

```jsx
const CREATE_ITEM_MUTATION = gql`
  mutation CREATE_ITEM_MUTATION(
    $title: String!
    $description: String!
    $price: Int!
    $image: String
    $largeImage: String
  ) {
    createItem(
      title: $title
      description: $description
      price: $price
      image: $image
      largeImage: $largeImage
    ) {
      id
    }
  }
`
```

- wrap all your forms inside a Mutation component.

```jsx
<Mutation mutation={CREATE_ITEM_MUTATION} variables={this.state}>
{(createItem, {loading,error})=>(...)
</Mutation>
```

- Error component wrote by Wes.
- Set the `<fieldset disabled={loading} aria-busy={loading}>`
- a loading bar use css animation.
- Route to the item we created.

```js
Router.push({
  pathname: '/item',
  query: { id: res.data.createItem.id },
})
```
