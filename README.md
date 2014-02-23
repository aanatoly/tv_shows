tv_shows
========

This script checks http://kickass.to site for the availability of new episodes
of TV shows, optionally opening links to the new episodes in the browser.
It can also check http://www.subtitleseeker.com for subtitles.

```
# show new episodes
$ ./tv_shows -n 'black sails' 
New episodes: s01e01, s01e02, s01e03, s01e04, s01e05

# show new episodes and number of subtitles
$ ./tv_shows -n 'black sails' -s
New episodes: s01e01, s01e02, s01e03 + 86, s01e04 + 100, s01e05 + 49
```
