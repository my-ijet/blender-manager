# blender-manager
IN DEVELOPMENT
cli Blender version manager (written in ysh https://oils.pub/)

Command: "get" is not supported yet,
other commands should work.

dependencies:
### arch linux
```sh
sudo pacman -S oils-for-unix
```

### Help
```
  Commands:
    update
        Find the latest version in the repo (https://download.blender.org/release/)
        then download and unpack it to <path>
        then remove the current version
        then set current to the downloaded version
    get latest|<version>
    current latest|<version>
        Set current to the specified version
    rm <version>
        Remove the specified version
        if the current version is removed, set current to the latest downloaded version
    purge
        Remove <path> and all of its contents
    ls, list [repo]
        List downloaded versions
        for the "repo" subcommand: list versions found in the Blender repository
  Flags:
    -p, --path [/opt/blender-manager/]
        Path to downloaded Blender versions
    -i, --install [false]
        Install a desktop file pointed to <path>/current/blender
        so frequent installation is not required
  <version> = MAJOR.MINOR[.PATCH]

```
