# XitDeck

Xitter Pro: a deck of columns side by side, like X Pro (TweetDeck), for a
[Xitter](https://github.com/Xittered/xitter) instance. Home, notifications,
searches, profiles, lists, communities, bookmarks, messages or any page of the
instance, each in its own column; several decks, columns you drag to reorder
and size, and a Post button.

Every column is the instance's own client, narrowed to one column, so posting,
replying and the rest work in it as they do on the instance. Decks and columns
are kept in each browser.

## Hosting

It is one static page: `index.html` and `config.js`. Put them on any static
host, e.g. at `https://pro.xitter.space`.

1. Set `origin` and `instance` in `config.js` to your instance.
2. On the instance, set `PRO_ORIGIN` to the deck's address
   (`PRO_ORIGIN=https://pro.xitter.space`). The instance lets only that address
   frame its pages, and its client hides its side bars inside the deck.
3. The deck must be on the same site as the instance (a subdomain of it): the
   columns use the instance's own sign-in cookies. People sign in on the
   instance.

An instance with this support also serves the deck itself at `/i/pro`, and on
`PRO_ORIGIN` when that name points at the instance's server, so hosting this
page separately is optional.

## License

AGPL-3.0-only, as Xitter.
