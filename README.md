# XitDeck

Xitter Pro: a deck of columns side by side, like X Pro (TweetDeck), for a
[Xitter](https://github.com/Xittered/xitter) instance. Home, notifications,
searches, profiles, lists, communities, bookmarks, messages or any page of the
instance, each in its own column, as on X Pro:

- Columns: Home, Following (newest first), Notifications, Mentions, Search,
  Profiles, Lists, Communities, Explore, Trending, Messages, Bookmarks, Likes,
  Scheduled posts, or any page of the instance; drag to reorder, three widths,
  rename, duplicate, auto-refresh
- Filters on search, profile and Following columns: media, images, videos,
  links or quotes; with, without or only replies; people you follow; minimum
  likes, reposts and replies; Top or Latest
- Several decks, each with an emoji; duplicate, reorder, export and import
  them, and link to one with `#deck=<id>`
- The unread count on notification columns and in the tab title, with an
  optional sound and desktop notification
- A Post button with the instance's own composer
- Keyboard shortcuts (`?` lists them): `n` post, `a` add column, `/` search,
  `1`-`9` and `0` columns, `[` `]` decks, `r` reload, `s` side bar, `,` settings
- The instance's theme and accent colour

Not like X Pro: every column shows the same signed-in account (the instance's
cookies are shared), and decks are kept in the browser rather than the
account.

Every column is the instance's own client, narrowed to one column, so posting,
replying and the rest work in it as they do on the instance.

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
