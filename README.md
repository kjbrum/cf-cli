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
    cf <task> <options>

Commands:
    clear-cache
        <domain>    The domain of which to clear the cache
```


## Config

#### CLOUDFLARE_EMAIL

You CloudFlare account email.

#### CLOUDFLARE_API_KEY

The API key associated with your account email. [Find it here](https://www.cloudflare.com/a/account/my-account)


## To-Do

- Add additional commands
    - `list` - display all the available domains
- Remove `jsawk` as a dependency


## License

Copyright © [Kyle Brumm](http://kylebrumm.com). Free to use on whatever and may be redistributed under the terms specified in the [license](LICENSE.md).
