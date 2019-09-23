---
title: Adeus Mundo Imundo
date: 2019-02-07
tags: ['Markdown', 'Releases']
description: "A new static site generator baby is born. It's highly inspired by Gatsby.js (React based) but built on top of Vue.js. We have been working on it for a year and will have a beta ready soon. You can expect this baby to grow up fast!"

---

Cθ οδιο μθcιθσ ηισ, εθμ αλιι γραεcε δελιcατισσιμι ιδ, θτ παθλο qθαλισqθε εοσ. Ειρμοδ οπτιον qθαεστιο ιν μει. Cετεροσ αccθσαμθσ vιμ τε. Ενιμ cονσθλ ατομορθμ πρι ιν, νο ιγνοτα σθσcιπιαντθρ εοσ. Νονθμεσ προβατθσ vολθπτατιβθσ εαμ θτ, ωισι φιερεντ δελεcτθσ αδ vελ. Πριμισ εριπθιτ vθλπθτατε νο μει, τε qθι λεγιμθσ σθσcιπιτ περιcθλισ. Ερατ προπριαε ετ δθο, ιριθρε cορπορα μενανδρι εα εθμ.

We think **Gridsome** is a missing piece to the Vue.js ecosystem. What Gatsby.js does for React.js is a game changer in how we build websites.  React.js is excellent, but we think Vue.js is more approachable for most web designers and devs getting started with JAMstack. Gridsome is the Vue.js alternative to Gatsby.

With **Gridsome** you get a universal GraphQL layer for all your connected data sources. This is like a single source of truth for your Web-site data, ready to be used in any page or component. Connect to any CMS or API, including Google Spreadsheet, Airtable, Instagram Feed, local markdown files, and so on.

Here is an example on how to query posts from the GraphQL layer in a page.


```html
<template>
  <Layout>
    <h2>Latest blog posts</h2>
    <ul>
      <li v-for="edge in $page.allWordPressPost.edges" :key="edge.node.id">
        {{ edge.node.title }}
      </li>
    </ul>
  </Layout>
</template>

<page-query>
query Blog {
  allWordPressPost (limit: 5) {
    edges {
      node {
        _id
        title
      }
    }
  }
}
</page-query>
```

You don't need to know GraphQL or Vue to get started with Gridsome - It's a great way to get introduced to both.


The GraphQL layer and all the data can be explored in a local GraphQL playground. The playground is usually located at `https://localhost:8080/___explore` when a Gridsome development project is running.




#### Perfect scores on Google Lighthouse - automagically 💚

One of the main goals of Gridsome is to make a framework that let you build websites that are optimized "out-of-the-box." It follows the [PRPL-pattern by Google.](https://developers.google.com/web/fundamentals/performance/prpl-pattern/) You don't need to be a performance expert to make fast websites with Gridsome. Your site gets almost perfect scores on Google lighthouse out-of-the-box. These are some of the performance steps that Gridsome takes care of:

- Image compressing & lazy-loading ⚡️
- CSS & JS minification ⚡️
- Code-splitting ⚡️
- HTML compressing ⚡️
- Critical CSS (Plugin) ⚡️
- Full PWA & Offline-support (plugin) ⚡️


#### A better way to build websites

Gridsome is built for the JAMstack workflow - a new way to build websites that gives you better performance, higher security, cheaper hosting, and a better developer experience. Generate prerendered (static) pages at build time for SEO-purpose and add powerful dynamic functionality with APIs and Vue.js.

We believe the SSGs / JAMstack trend is just getting started. When you have first started to make websites this way there is no way back. You feel almost "dirty" when going back to a traditional WordPress / CMS setup.

Try running the new Chrome Lighthouse (Audit tab in Developer tools) on a WordPress site - It is impossible to get good scores even with the best caching plugins and hosting. With Gridsome you don't even need caching plugins. Website optimization is taken care of at build time.

This is what we think is very exciting and is why we are building Gridsome. It is the **perfect SPA & PWA front-end solution** for any headless CMS or content APIs.


#### Whats next

In the next couple of months we're going to continue to improve the docs, create tutorials, add more source & transformer plugins and fix bugs.

#### Contribute to Gridsome

We're currently just two brothers working on this, so any contribution is very welcome. We're passionate about building a faster web and make website building fun again.

You can also support us by giving [a GitHub star ★](https://github.com/gridsome/gridsome/stargazers) and spread the word :)
