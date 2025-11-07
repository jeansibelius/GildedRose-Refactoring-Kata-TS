# Gilded Rose Requirements Specification

Hi and welcome to team Gilded Rose. As you know, we are a small inn with a prime location in a
prominent city ran by a friendly innkeeper named Allison. We also buy and sell only the finest goods.
Unfortunately, our goods are constantly degrading in `Quality` as they approach their sell by date.

We have a system in place that updates our inventory for us. It was developed by a no-nonsense type named
Leeroy, who has moved on to new adventures. Your task is to add the new feature to our system so that
we can begin selling a new category of items. First an introduction to our system:

- All `items` have a `SellIn` value which denotes the number of days we have to sell the `items`
- All `items` have a `Quality` value which denotes how valuable the item is
- At the end of each day our system lowers both values for every item

Pretty simple, right? Well this is where it gets interesting:

- Once the sell by date has passed, `Quality` degrades twice as fast
- The `Quality` of an item is never negative
- **"Aged Brie"** actually increases in `Quality` the older it gets
- The `Quality` of an item is never more than `50`
- **"Sulfuras"**, being a legendary item, never has to be sold or decreases in `Quality`
- **"Backstage passes"**, like aged brie, increases in `Quality` as its `SellIn` value approaches;
  - `Quality` increases by `2` when there are `10` days or less and by `3` when there are `5` days or less but
  - `Quality` drops to `0` after the concert

We have recently signed a supplier of conjured items. This requires an update to our system:

- **"Conjured"** items degrade in `Quality` twice as fast as normal items

Feel free to make any changes to the `UpdateQuality` method and add any new code as long as everything
still works correctly. However, do not alter the `Item` class or `Items` property as those belong to the
goblin in the corner who will insta-rage and one-shot you as he doesn't believe in shared code
ownership (you can make the `UpdateQuality` method and `Items` property static if you like, we'll cover
for you).

Just for clarification, an item can never have its `Quality` increase above `50`, however **"Sulfuras"** is a
legendary item and as such its `Quality` is `80` and it never alters.

# From the original author

Support this and all my katas via [Patreon](https://www.patreon.com/EmilyBache)\_

# Gilded Rose Refactoring Kata

You can find out more about this exercise in my YouTube video [Why Developers LOVE The Gilded Rose Kata](https://youtu.be/Mt4XpGxigT4). I also have a video of a worked solution in Java - [Gilded Rose Kata, Hands-on](https://youtu.be/OdnV8hc9L7I)

I use this kata as part of my work as a technical coach. I wrote a lot about the coaching method I use in this book [Technical Agile Coaching with the Samman method](https://leanpub.com/techagilecoach). A while back I wrote this article ["Writing Good Tests for the Gilded Rose Kata"](http://coding-is-like-cooking.info/2013/03/writing-good-tests-for-the-gilded-rose-kata/) about how you could use this kata in a [coding dojo](https://leanpub.com/codingdojohandbook).

## How to use this Kata

The simplest way is to just clone the code and start hacking away improving the design. You'll want to look at the ["Gilded Rose Requirements"](https://github.com/emilybache/GildedRose-Refactoring-Kata/blob/main/GildedRoseRequirements.md) which explains what the code is for. I strongly advise you that you'll also need some tests if you want to make sure you don't break the code while you refactor.

You could write some unit tests yourself, using the requirements to identify suitable test cases. I've provided a failing unit test in a popular test framework as a starting point for most languages.

Alternatively, use the Approval tests provided in this repository. (Read more about that in the section "Text-based Approval Testing").

The idea of the exercise is to do some deliberate practice, and improve your skills at designing test cases and refactoring. The idea is not to re-write the code from scratch, but rather to practice taking small steps, running the tests often, and incrementally improving the design.

## History of the exercise

This Kata was originally created by Terry Hughes (<http://twitter.com/TerryHughes>). It is already on GitHub [here](https://github.com/NotMyself/GildedRose). Bobby Johnson described the kata in an article titled "Refactor This: The Gilded Rose Kata", but unfortunately it is no longer on the internet. I found it on the Wayback Machine [here](https://web.archive.org/web/20240525015111/https://iamnotmyself.com/refactor-this-the-gilded-rose-kata/).

I translated the original C# into a few other languages, (with a little help from my friends!), and slightly changed the starting position. This means I've actually done a small amount of refactoring already compared with the original form of the kata, and made it easier to get going with writing tests by giving you one failing unit test to start with. I also added test fixtures for Text-Based approval testing with TextTest (see [the TextTests](https://github.com/emilybache/GildedRose-Refactoring-Kata/tree/main/texttests))

As Bobby Johnson points out in his article "Why Most Solutions to Gilded Rose Miss The Bigger Picture" (on the Wayback Machine [here](https://web.archive.org/web/20230530152324/https://iamnotmyself.com/why-most-solutions-to-gilded-rose-miss-the-bigger-picture/)), it'll actually give you
better practice at handling a legacy code situation if you do this Kata in the original C#. However, I think this kata
is also really useful for practicing writing good tests using different frameworks and approaches, and the small changes I've made help with that. I think it's also interesting to compare what the refactored code and tests look like in different programming languages.

## Contributing

Contributions are encouraged! You could add a translations of the specification
in another language or a new starting point for your favorite programming
language. Please see [CONTRIBUTING.md](./CONTRIBUTING.md) for more details.
