tv_shows
========

Prints info about TV shows: next episode air date, avalable torrents,
show status and more.

Lets search for `dragons`.

```
tv_shows dragons

TV                              Available                 
Dragons                                                   
Dragons Den Ca                  s10e01, s10e02, s10e03    
Dragons Den Uk                  s13e04                    
Dreamworks Dragons Race To The  s03e01                    
Edge                                                      
```

It also can print trends
```
tv_shows --trends

TV                              Refs  
Heroes Reborn                   6    
The Big Bang Theory             6    
Arrow                           5    
Gotham                          5    
How to Get Away with Murder     5    
Quantico                        5    
The Flash 2014                  5    
American Horror Story           4    
Blindspot                       4    
Game of Thrones                 4    
Homeland                        4    
Limitless                       4    
South Park                      4    
Supernatural                    4    
Marvels Agents of S H I E L D   3    
Scandal US                      3    
The Originals                   3    
```

## Configuration
Configuration is kept in `~/.config/tv_shows` dir.

```
CDIR=~/.config/tv_shows
mkdir -p "$CDIR"
```



### Currently watched TV shows
It can deduce watched shows from downloaded torrents. Just point `tv_shows`
to the torrent download directory, it will get show names from all "some name
sXXeXX" files.

To do so, in a config directory, create soft link to the torrent download
dir. Link's name must be `torrents`.

```
cd "$CDIR"
ln -sf ~/Downloads/torrents torrents
```

It will also update permanent list (see berow).

### Permanent List
To always get updates for some show, just add a file to the `watchlist` direcory
For example: to follow 'Vikings'

```
mkdir -p "$CDIR/watchlist"
cd "$CDIR/watchlist"
touch "Vikings s02e10"
```

### Rare List
Has same structure as permanent list, use `tv_shows --rare` to query it.

For example: to follow 'Extant' and 'Dark Matter'
```
mkdir -p "$CDIR/rare"
cd "$CDIR/rare"
touch "Extant s02e10"
touch "Dark Matter s01e13"
tv_shows --rare

TV                              Sean    Status                    
Dark Matter                     s01e13  On Air                    
Extant                          s02e10  Cancelled                 
```

