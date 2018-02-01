# dokku robots.txt

Creates a [robots.txt](https://en.wikipedia.org/wiki/Robots_exclusion_standard) for applications that can be set to allow or disallow web crawlers to the app. This is useful for deploying websites that you do not want indexed by search engines. For instance, you may want to deploy a production app with robots allowed and a staging app with robots disallowed.

## requirements

- dokku 0.4.x+

## installation

```shell
# on 0.4.x+
sudo dokku plugin:install https://notabug.org/candlewaster/dokku-robots.txt.git robots.txt
```

## commands

```
robots.txt:disallow <app>, Discourages web crawlers from indexing this app
robots.txt:allow <app>,    Doesn't discourage web crawlers from indexing this app
```

## usage

```shell
# Discourage web crawlers from indexing myapp
dokku robots.txt:disallow myapp

# Don't discourage web crawlers from indexing myapp
dokku robots.txt:allow myapp

# View robots.txt for myapp
dokku robots.txt myapp
```
