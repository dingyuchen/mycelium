---
id: dodgf8dws72bbit42h1r3x6
title: Golinks
desc: ''
updated: 1665666425553
created: 1665666018172
---

Golinks is a pretty simple concept:

you open your browser and type something like `go/nus` to go to your school's website for example.

In the backend, a DNS record should redirect your request to a server that stores the database of short links to actual links.

All that server needs to do is to simply return a `503` code with the full address of the school website, and voila.

## Implementation

Before we go into the implementation, we shall define the short-form url as "**alias**" and the full URL address as "**url**".

In my bootleg implementation, we only propose the following features:

1. A frontend for users to query existing aliases
2. A frontend for users to create a new alias to a website
3. A server that serves the frontend for empty or invalid aliases
4. The same server to reply with redirections upon a matching alias
