# sydthekid
thoughts on music 

# minimum headers for published post 
```---
   title: "a break down of Zuboff's The Age of Surveillance Capitalism"
   date: 2020-11-02T16:39:00-06:00
   draft: false
   showDate: true
   ---
```

# draft content headers example 
```
---
title: "The Chicks Change Their Name"
date: 2020-07-07T09:02:19-07:00
expirydate: 2020-07-07T09:02:19-07:00
draft: true
type: "content"
showDate: true
---
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
