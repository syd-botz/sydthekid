# sydthekid
thoughts on music 

# draft content headers example 

```
_____
title: "The Chicks Change Their Name"
date: 2020-07-07T09:02:19-07:00
expirydate: 2020-07-07T09:02:19-07:00
draft: true
type: "content"
_____
```

# publishing a post 
  - change headers to correct date and draft status
  - rebuild ```hugo -D -t sam```
  - push changes to github
  
# create pages

Run:

```sh
hugo new page.md
```

# posts

To create a new post, run:

```sh
hugo new posts/your-post-title.md
```


# preview site locally

Use Hugo's built-in server to see your site in action as you make changes.

```sh
hugo serve -t sam
```
