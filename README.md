# Ryzen-Mods
Ryzen Mods Catalog Container...
Mods will stored at issues.

# Add mod
Just create issue with special template. 

In issue body should be mod info in ini style.

Main section is `mod`.

Values: 
- `file`: used to make download link like `github.com/user/repo/releases/download/{mod.release_tag}/{mod.file}` <br>Examples: me.mod.geode, me.mod.dll, mod.dll
- `repo`: ur repository path for getting info and some projec files <br>Examples: user95401/Ryzen, omgmodding/better-gd, ur-username/mod-name
- `release_tag`: its better to set 'latest' but u can set exact tag of release with mod
- `desc`: small description about ur mod, supports color tags

Full ini example:
```ini
[mod]
file = noname.mod.geode
repo = user/mod
release_tag = latest
desc = <cg>helluva cool mod</c>
```

# Hide away or bring back the mod
Close opened issue to remove mod from listing, reopen to add mod again.

# Release Settings
You can specify some ini styled data in release body.
Main section is `release`, values can be init:
- `download_link`: [**__Direct download link__**](https://en.wikipedia.org/wiki/Direct_download_link) that points up to your file. Its can be used if u cant host release file at github releases.

# Commands
Every issue comment is processed by workflow for commads.
- `!setlabels label,other-label` to toggle label. Only issue creator can use that, `verify` label will be ignored
