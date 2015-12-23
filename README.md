# CloudFlare CLI - (WIP)

> A command line tool for communicating with the CloudFlare API.


## Install

__Dependencies:__

- [Jsawk](https://github.com/micha/jsawk) - Used to parse the JSON responses.

```
$ curl https://raw.githubusercontent.com/kjbrum/cf-cli/master/cf > ~/bin/cf
$ chmod +x ~/bin/cf
```


## Usage

```
CloudFlare CLI - v0.0.1

A command line tool for communicating with the CloudFlare API.

Usage:
    cf <command> <options>

Commands:
    cleanup         Remove all config files
    clear-cache
        <domain>    The domain of which to clear the cache
    help            Display this help text
    init            Initialize necessary config files
    list            List all the available domains
    update          Download the latest version of cf
    version         Display the current version
```


## Config

#### CLOUDFLARE_EMAIL

Your CloudFlare account email.

#### CLOUDFLARE_API_KEY

The API key associated with your account email. [Find it here](https://www.cloudflare.com/a/account/my-account)


## To-Do

- Add additional commands
    - `analytics`
        - `--since|-s` (-<num minutes or absolute timestamp>)
        - `--until|-u` (-<num minutes or absolute timestamp >)
        - `--continuous|-c` (true, false)
    - `dsn`
        - `--type|-t` (A, AAAA, CNAME, TXT, SRV, LOC, MX, NS, SPF)
        - `--name|-n` ("example.com")
        - `--order|-o` (type, name, content, ttl, proxied)
        - `--direction|-d` (asc, desc)
    - ~~`list`~~
        - `--name|-n` ("example.com")
        - `--status|-s` (active, pending, initializing, moved, deleted, deactivated)
        - `--order|-o` (name, status, email)
        - `--direction|-d` (asc, desc)
    - ~~`clear-cache`~~
        - `--files|-f` (["http://www.example.com/css/styles.css","http://www.example.com/js/script.js"])
        - `--tags|-t` (["some-tag","another-tag"])
- Remove `jsawk` as a dependency
- Create a function that builds the request URL (base + endpoint + query string) instead of needing different functions for eveything


## License

Copyright © [Kyle Brumm](http://kylebrumm.com). Free to use on whatever and may be redistributed under the terms specified in the [license](LICENSE.md).
