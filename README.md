# Jellyfin.Plugin.ThePornDB

This metadata provider helps fill Jellyfin/Emby with information for your adult videos by pulling from [ThePornDB](https://theporndb.net)

> This is a fork of [ThePornDatabase/Jellyfin.Plugin.ThePornDB](https://github.com/ThePornDatabase/Jellyfin.Plugin.ThePornDB) that adds tag filtering (blacklist/whitelist) and tag mappings. It is periodically rebased on upstream `main`.

[![GPL 2.0 License](https://img.shields.io/github/license/bugfloyd/Jellyfin.Plugin.ThePornDB)](./LICENSE)
[![Current Release](https://img.shields.io/github/release/bugfloyd/Jellyfin.Plugin.ThePornDB)](https://github.com/bugfloyd/Jellyfin.Plugin.ThePornDB/releases/latest)
[![Build status](https://img.shields.io/github/actions/workflow/status/bugfloyd/Jellyfin.Plugin.ThePornDB/release.yml)](https://github.com/bugfloyd/Jellyfin.Plugin.ThePornDB/releases/tag/latest)

------------

## Install
- Repository (Jellyfin only):
  - Add to the list this URL `https://raw.githubusercontent.com/bugfloyd/Jellyfin.Plugin.ThePornDB/main/manifest.json`
- Manual:
  - Download Archive from [Latest Release](https://github.com/bugfloyd/Jellyfin.Plugin.ThePornDB/releases/latest)
  - Follow the [Instruction](https://jellyfin.org/docs/general/server/plugins/index.html)

## Compatibility

| Plugin version | Jellyfin version |
|----------------|------------------|
| 2.0.0.0+       | 12.x             |
| 1.7.0.1        | 10.11.x          |

Jellyfin only offers plugin versions whose target ABI matches the server, so a 10.11 server keeps getting 1.7.0.1 from the repository and a 12.x server gets 2.x.

## Upgrading Jellyfin 10.11 → 12
1. Upgrade the Jellyfin server to 12.
2. In Dashboard → Plugins → Catalog, open ThePornDB and install the latest 2.x version (or wait for the "Update Plugins" scheduled task to pick it up).
3. Restart Jellyfin.

Until step 2 is done, the 1.7.0.1 build may fail to load on Jellyfin 12. Plugin settings, including tag filters and mappings, are kept across the upgrade.
