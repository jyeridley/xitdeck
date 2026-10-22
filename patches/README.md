# Xitter server patch

`0001-Add-Xitter-Pro-a-TweetDeck-style-deck-of-columns.patch` is the change
[Xittered/xitter](https://github.com/Xittered/xitter) needs for the deck: its
client hides its side bars inside a column and talks to the deck, client pages
may be framed only by the instance and `PRO_ORIGIN`, and the instance serves the
deck itself at `/i/pro` and on `PRO_ORIGIN`.

Apply it in a checkout of xitter:

```sh
git am /path/to/0001-Add-Xitter-Pro-a-TweetDeck-style-deck-of-columns.patch
```

then set `PRO_ORIGIN=https://pro.xitter.space` on the instance.
