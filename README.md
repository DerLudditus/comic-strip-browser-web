# Comic Strip Browser ... in your browser! (duh!)

The standalone PyQt6 app [Comic Strip Browser](https://github.com/DerLudditus/comic-strip-browser) has not only bugs but also the inconvenience of depending on a specific OS. There was a need for a simpler one, for which (almost) only a browser would be needed.

:white_check_mark: If you have Python installed locally so that a tiny proxy server can be launched, then you only need a browser. :point_down:

:rocket: [**comic-strip-browser-to-go**](./comic-strip-browser-to-go)

:white_check_mark: If you have a WordPress installation somewhere, you can upload a PHP version there and access it with a browser. :point_down:

:rocket: [**comic-strip-browser-for-wordpress**](./comic-strip-browser-for-wordpress)

A completely server-free HTML+JS version cannot be made due to CORS limitations. A bit more about that [on my blog](https://ludditus.com/2025/11/15/comic-strip-browser-in-your-browser/).


### Supported Comic Strips

1. **Calvin and Hobbes** - since 1985-11-18
2. **Peanuts** - since 1950-10-16
3. **Peanuts Begins** - since 1950-10-16 (Reprint series; for old dates can be identical to Peanuts, only in color)
4. **Garfield** - since 1978-06-19
5. **Wizard of Id** - since 2002-01-01 (Limited GoComics availability)
6. **Pearls before Swine** - since 2002-01-07
7. **Shoe** - since 2001-04-08 (Limited GoComics availability)
8. **B.C.** - since 2002-01-01 (Limited GoComics availability)
9. **Back to B.C.** - since 2015-09-21 (Recent reprint series)
10. **Pickles** - since 2003-01-01 (Limited GoComics availability)
11. **WuMo** - since 2013-10-13 (With gaps)
12. **Speed Bump** - since 2002-01-01 (Limited GoComics availability)
13. **Free Range** - since 2007-02-03
14. **Off the Mark** - since 2002-09-02 (Limited GoComics availability)
15. **Mother Goose and Grimm** - since 2002-11-25 (Limited GoComics availability)
16. **The Flying McCoys** - since 2005-05-09
17. **The Duplex** - since 1996-08-12
18. **Reality Check** - since 1997-01-01
19. **Adam@Home** - since 1995-06-20
20. **Ziggy** - since 1971-06-27

<img src="./Screenshots/Example 0 (not maximized).png" width="100%"/>

It is **not** without :bug: bugs, but once you get used to the various buttons, you can work around them. 

Some comic titles, especially in their early days, can have large gaps in availability: either they are weekly instead of daily, or they have entire months without a strip. In such cases, with Next/Previous, the app iterates a number of days, after which, if it stops without having found anything, you select another date yourself. 

There are two types of calendars:
- The large, clickable one (the arrows also work!) with buttons to navigate by month or by year.
- The dropdown-based one, meant for quick direct navigation to a desired date.

There are some bugs related to the interaction between these two calendars and between them and the top navigation buttons (`First`, `Previous`, `Next`, `Today`, `Random`). Nothing that could kill you, though. 

On your keyboard, `Home`/`End` mean `First`/`Today`.

### More details, in the README file for each of the two versions!

