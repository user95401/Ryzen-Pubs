# Ryzen-Mods
Ryzen Mods Catalog Container...<br>
Mods will be stored at issues.

### Add mod
Just create an issue with related template.<br>
In issue body should be mod info in [INI style](https://en.wikipedia.org/wiki/INI_file).

### Hide away or bring back mod
Close opened issue to remove mod from listing, reopen to add mod again.

# Commands
Every issue comment is processed by workflow for commands.

- `!setlabels label,other-label` to toggle label.
```
ONLY issue creator can use that, 
"verified" and "featured" labels causes cancel WHOLE command.
```
- `!actualversion=v1.1.0` to set actual version. 
```
Its will be saved at user locally.

Mod crawling for latest comment contains "!actualversion=".
And will notify if rvalue is not founded in local user save.

All downloaded versions is saved in 
"geode/ryzen/mods/yourmod/.downloadedVersions"
```
