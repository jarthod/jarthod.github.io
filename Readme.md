This repo holds the sources of my personal website https://adrienjarthon.com

It's built using the most simple ruby tools: `erb` and `yaml` (both part of standard library). So all you need to build is a working `ruby` installation.

The source is basically [index.html.erb](index.html.erb) (and [experiences.yml](experiences.yml) for the experience timeline).

## Build
```
erb index.html.erb > index.html
```

During heavy development we can rebuild continuously:
```
xdg-open index.html
watch -n 2 "erb index.html.erb > index.html"
```

Check for dead links
```
sudo apt install linkchecker
linkchecker --check-extern index.html
```

## Deploy
```
git add . && git commit -m "new version" && git push
```

## Changelog
_(excluding minor design and content changes)_

- 2024-06: Add PPL + some emoji + fix all dead links
- 2022-02: Timeline update + add rdap / remove mongo-log-replay + minor tweaks
- 2021-07: End of RC + add updown in timeline + couple fixes
- 2020-03: v2 using simpler tools. Removing middleman, custom font, GA
- 2015-04: Add timeline visualisation
- 2015-03: Switch to `middleman` for more simplicity
- 2014-12: Initial version using `jekyll` and github pages