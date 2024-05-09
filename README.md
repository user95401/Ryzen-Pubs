# Ryzen-Mods
Ryzen Mods Catalog Container...
Mods will be stored at issues.

# Add mod
Just create an issue with special template. 
In issue body should be mod info in [INI style](https://en.wikipedia.org/wiki/INI_file).

Main section is `mod`, values can be in it:
Values: 
- `file`: used to make download link like `github.com/user/repo/releases/download/{mod.release}/{mod.file}` <br>Examples: me.mod.geode, me.mod.dll, mod.dll
- `repo`: ur repository path for getting info and some project files <br>Examples: user95401/Ryzen, omgmodding/better-gd, ur-username/mod-name
- `release`: it\'s better to set 'latest' but u can [set exact release](https://docs.github.com/en/rest/releases/releases?apiVersion=2022-11-28#get-the-latest-release) with mod. <br>Examples: latest, tag/v1.0.0, 153706099
- `desc`: small description about your mod, supports color tags
### Full INI example:
```ini
[mod]
file = noname.mod.geode
repo = user/mod
release_tag = latest
desc = <cg>helluva cool mod</c>
```

# Release Settings
You can specify some [INI styled](https://en.wikipedia.org/wiki/INI_file) data in release body.
Main section is `release`, values can be in it:
- `download_link`: [**__Direct download link__**](https://en.wikipedia.org/wiki/Direct_download_link) that points up to your file. It can be used if u can\'t host release file at GitHub releases.
### Full INI example:
```ini
[release]
download_link = https://yo.cloud/uploads/my_tp.zip
```

# Mod variants
Pack (.zip), Geode Mod (.geode), Standalone Mod (.dll/.so)
| Variant        | Label | Install Path                            | MetaInf File      | Logo File                  |
|----------------|-------|-----------------------------------------|-------------------|----------------------------|
| Pack           | pack  | geode/config/geode.texture-loader/packs | none or pack.json | pack.png/repo_owner_avatar |
| Geode Mod      | mod   | geode/mods                              | none or mod.json  | logo.png/repo_owner_avatar |
| Standalone Mod | mod   | geode/ryzen/loadit                      | none or mod.json  | logo.png/repo_owner_avatar |

Files is getting at GitHub repo btw
```java
fmt::format(
    "https://raw.githubusercontent.com/{}/{}/{}",
    ini()->GetValue("mod", "repo"),
    repoJson()["default_branch"].as_string(),
    type() == ModType::Mod ? "logo.png" : "pack.png"
)
```

# Hide away or bring back the mod
Close opened issue to remove mod from listing, reopen to add mod again.

# Commands
Every issue comment is processed by workflow for commands.
- `!setlabels label,other-label` to toggle label. Only issue creator can use that, `verify` label will be ignored
