# comickfzf
Fzf script for downloading comicks/mangas from comick.app

![Preview](https://i.imgur.com/uhiqBW8.gif)

## Dependencies
- jq
- parallel
- aria2c
- xargs
- ueberzug
- awk

## How to install
1. clone the project
2. copy `comickfzf` to one of `PATH` directories

### Usage
first the script needs to store trend mangas in `$CACHE_SESSION` directory using (it takes some time be patient :) )
```sh
comickfzf update
```
and then run 
```sh
comickfzf fzf
```

#### Searching for a manga
use `search` option
```
comickfzf search <name>
```
this command fetch result from comick.app and then open fzf with the `<name>`
