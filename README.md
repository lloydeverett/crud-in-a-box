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

There are lots of these (see [Rails Jabloon](https://www.getsjabloon.com/pricing) or [Laravel Spark](https://spark.laravel.com/) for example). They mostly focus on online SaaS businesses use cases and try to cover a wide range of problems in that context, though you will have to part with at least about $100 USD. The SaaS service [Outseta](outseta.com) also deserves a mention; it's seems like a really solid product for a new SaaS business.

My main apprehension with starter packs is that experience with them is unlikely to translate well to other use cases. They're usually tied to a specific tech stack and as I say they are usually oriented around SaaS businessses. If one needs to, for instance, add auth to a back office application then it doesn't really make sense to reach for Laravel Spark's auth and prior experience with it isn't going to count for much, while experience with Firebase Auth or Keycloak could well come in handy. They also seem to go against the principle of doing one thing and doing it well. Still, if you're committed to the product and the tech stack then it could definitely make sense to use one of these.

## Takeaways


