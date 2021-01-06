# CRUD-in-a-box

If you're building software, you typically want to validate the product as quickly as possible. Most of the time developers don't want to spend all their time working on a product that will never have a userbase. Even so, it's all too easy to start reinventing the wheel. This is a compilation of tools that seem to solve common boilerplate problems in software effectively. I've focused on solutions that are either free or inexpensive so that one can test out ideas without too much upfront investment.

Mind you, this is a difficult role for tools to fill: they need to straddle the line between making too many assumptions to be applicable and making too few assumptions to be helpful. Still, I think some of them get it right.

## Useful links

[Ask HN: SaaS frameworks for startups](https://news.ycombinator.com/item?id=22209821)

[Ask HN: What's the fastest tool for basic CRUD?](https://news.ycombinator.com/item?id=22091012)

[Ask HN: How do you currently solve authentication? | Hacker News](https://news.ycombinator.com/item?id=22157166)

[An excellent twitter thread](https://twitter.com/flybayer/status/1220406529901223936)

[A Rails evangelist](https://news.ycombinator.com/item?id=17858711)

Also: [Does it scale? Who cares!](https://jacquesmattheij.com/does-it-scale-who-cares/)

## Starter packs

There are lots of these (see [Rails Sjabloon](https://www.getsjabloon.com/pricing), [Laravel Spark](https://spark.laravel.com/) or [ABP.IO](https://abp.io/) for example). They mostly focus on online SaaS businesses use cases and try to cover a wide range of problems in that context, though you will have to part with at least about $100 USD. The SaaS service [Outseta](outseta.com) also deserves a mention; it's seems like a really solid product for a new SaaS business.

My main apprehension with starter packs is that experience with them is unlikely to translate well to other use cases. They're usually tied to a specific tech stack and as I say they are usually oriented around SaaS businessses. If one needs to, for instance, add auth to a back office application then it doesn't really make sense to reach for Laravel Spark's auth and prior experience with it isn't going to count for much, while experience with Firebase Auth or Keycloak could well come in handy. They also seem to go against the principle of doing one thing and doing it well. Still, if you're committed to the product and the tech stack then it could definitely make sense to use one of these.

## Implementing CRUD

I find GraphQL especially promising. [Postgres](https://www.postgresql.org/) + [Hasura OSS](https://hasura.io/opensource/) + [React Admin](https://marmelab.com/react-admin/) seems like a great combination. Refer to [React Admin Low Code](https://github.com/cpursley/react-admin-low-code) and [React Admin Hasura Firebase](https://github.com/dvasdekis/react-admin-hasura-firebase). It's also worth looking at [KeystoneJS](https://www.keystonejs.com/). Make sure to also use code generation in lieu of writing API calls on the client yourself.

Otherwise, Rails and Django seem to have good ecosystems if you're looking for a more traditional approach. They both seem quite good at bridging the gap between the relational database and your object models. You could perhaps even find some way to get a GraphQL API out of them and then use them in combination with React Admin, though they also have their own packages for admin dashboards: Django has an inbuilt solution and Rails has [ActiveAdmin](https://activeadmin.info/).

## Authentication

Some people suggest you should ship your own auth, but I'm not sure I agree. There are many, many ways to accidentally mess up security and at some point you'll probably want SSO or 2FA anyway.

[Firebase Auth](https://firebase.google.com/docs/auth) is free and it seems like a great option though relying on a third party does make me a bit uncomfortable. [Keycloak](https://www.keycloak.org/) is a self-hosted and well supported but allegedly quite difficult to set up. I think I'll also have to take a look at what's available from the Rails ecosystem in terms of self-hosted auth.

## Tools for an online SaaS business

### Payments

[Stripe](https://stripe.com/) seems like the go-to for this. They've been making it a bit easier to accept payments without making your own customer billing portal: see [Stripe Billing Customer Portal](https://stripe.com/blog/billing-customer-portal) and [Stripe Checkout](https://stripe.com/en-gb-us/payments/checkout).

### Email

Do not try to manage sender reputation yourself and separate transactional email from marketing email. [Postmark](https://postmarkapp.com/) is great for the former and [Mailgun](https://www.mailgun.com/) seems to do both.

### Sites

I'm quite fond of [Umso](https://www.umso.com/) for landing pages and [Hugo](https://gohugo.io/) for other static sites. [Vanta.js](https://www.vantajs.com/) has cute header animations. Beyond that, I'll have to do a bit more research in this area.
