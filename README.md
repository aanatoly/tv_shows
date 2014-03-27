tv_shows
========

This script checks http://kickass.to site for the availability of new episodes
of TV shows, optionally opening links to the new episodes in the browser.
It can also check http://www.subtitleseeker.com for subtitles.


Show new episodes for 'Black Sails' TV show
```bash
$ ./tv_shows -s -n 'black sails' 
TV            Old      New
Black Sails            s01e01 + subs, s01e02 + subs, s01e03 + subs, s01e04 +
                       subs, s01e05 + subs, s01e06 + subs, s01e07 + subs,
                       s01e08 + subs
```

Show new episodes for all shows in a db
```bash
$ ./tv_shows -a -s
TV              Old      New
Black Sails     s01e08
Grimm           s03e16   in 7 days
Justified       s05e11   in 4 days
Rake            s03e07
The Blacklist   s01e17   in 3 days
The Originals   s01e17   in 18 days
Vikings         s02e03   s02e04 + subs
```
