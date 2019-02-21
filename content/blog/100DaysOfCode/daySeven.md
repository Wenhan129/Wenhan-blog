---
title: 19 - Updating Items with Queries and Mutations
date: '2019-02-21T00:00:03.284Z'
---

## Mutation and Query in Prisma

- `updateItem()`
- `item(where:):Item`

## Mutation and Query in Yoga

- `updateItem(parent, args, ctx, info)` 1. Take a copy of the updates 2. Remove the ID from the updates 3. Run the update method
- `item: forwardTo('db')`

## Jump back to Front End Project

1. `UpdateItem.js` in components/
2. `Update.js` in pages
   1. Get the id from upper level and pass it to the `UpdateItem`

## Create an UpdateItem component

- SINGLE_ITEM_QUERY - Pass the ID - Get the ID, title, description and price.
- Wrap the `<Mutation>` inside `<Query>` - Extract `loading` and `data` from `<Query>` - Don’t forget to return `<Mutation>` component. - Check the item router to render the page
- Set the defaultValue to the forms by the data from server - defaultValue={data.item.title}
- Pass the `updateItem` from `<Mutation>` to `<Form onSubmit>` - e.preventDefault()
