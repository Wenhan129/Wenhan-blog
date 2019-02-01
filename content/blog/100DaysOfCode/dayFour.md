---
title: 16 React Meets GraphQL - Notes
date: '2019-02-01T00:00:03.284Z'
---

# Day Four - 100 DaysOfCode

Well, looking back to past days' updates , using the main topic from the content as the title will be beneficial for reviewing. I will count the days inside the post instead as the title.

## Items as the Homepage

- Add items.js into the nav bar
- import gql from ‘graphql-tag’ - From Apollo team - Just put all the queries into one single file and then we can export it. - Write queries in a gql`` tagged string
- Query with Apollo team - `<Query query={THE_QUERIES_CREATED_BY_YOU}`
  - Now we need to put the queries created by us with gql.
  - The reason why we use a render props pattern instead of HOC is the Query component can help us to get the loading state of a request.
  - We must put a {} function inside within <Query> </Query>
  - ifError and ifLoading
- propTypes
  PropTypes.shape: you can shape your object, like
  `PropTypes.shape(Item {title: PropTypes.string.isRequired`jsx
- Link from next
  `<Link href={{pathname: '/item',query:{id:item.id}}}`
- format function wrote by Wes.
