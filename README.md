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

## Usage
first the script needs to store trend mangas in `$CACHE_SESSION` directory using (it takes some time be patient :) )
```sh
comickfzf update
```
and then run 
```sh
comickfzf fzf
```

### Searching for a manga
use `search` option
```
comickfzf search <name>
```
this command fetch result from comick.app and then open fzf with the `<name>`

### Enviroment variables
| Env           | Description                                                                                    |
|---------------|------------------------------------------------------------------------------------------------|
| CURL_CMD      | used to fetch jsons, and %s will be replaced by url eg. curl --socks5 127.0.0.1:9080 '%s'      |
| ARIA2C_OPTS   | options for aria2c, it used to download manga images                                           |
| PARALLEL_OPTS | gnu parallel options                                                                           |
| DL_FOLDER     | used to save cbz files                                                                         |
| SESSION_CACHE | manga detailes are stored inside this folder default is $HOME/.cache/comick                    |
| DETAIL_BELOW  | if set the fzf preview detail(eg. title) will be belew of the image                            |
| CHAPTER_LIMIT | the limit of chapters info stored                                                              |
| LANGUAGE      | language used as `lang` query string in apis                                                   |
