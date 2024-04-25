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

Full ini example:
```ini
[mod]
file = noname.mod.geode
repo = user/mod
release_tag = latest
```

# Hide away or bring back the mod
Close opened issue to remove mod from listing, reopen to add mod again.
