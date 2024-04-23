# Ryzen-Mods
Ryzen Mods Catalog Container...
Mods will stored at releases.

# Add mod
Every created issue (open or reopen) will event workflow that creating or updating release with issue data.

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
Close opened issue to remove mod from list, reopen to add mod again.

# Verifying?
Unverifyed mods has "pre-release" option enabled. Its by default...
Trusted people can verify mods, commands are (as issue comment):
- !verify
- !unverify
