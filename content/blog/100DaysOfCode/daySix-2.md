---
title: 18 - Uploading Images
date: '2019-02-03T00:00:03.284Z'
---

1. [Cloudinary](https://cloudinary.com/) - 10GBs for a free account.
2. Upload an image
   1. input type `file`
   2. `e.target.files`
   3. `data.append('file',files[0])`
   4. `data.append('upload_preset','squared')`(Only for Cloudinary)

What I learnt today is the workflow of an image uploading function with the help of html forms and 3rd party image server. But the function is pretty simple, it needs a validation between the client and server. Otherwise, it will make some unnecessary space and bandwidth cost to the server.
