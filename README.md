# Lume — releases

Public distribution point for **[Lume](https://mvtti.gumroad.com/l/lume)**, a
precision audio metering suite and visualiser for Windows.

This repository contains **no source code**. It exists so the app can check
whether a newer build is available, and so downloads have a stable home.

## What's here

- **`version.json`** — the update manifest. Lume fetches this (a plain `GET`,
  sending nothing about you or your machine) and compares it with its own
  version.

  ```json
  {
    "version": "1.0.0",
    "url": "https://mvtti.gumroad.com/l/lume",
    "notes": "Shown to the user when an update is found."
  }
  ```

  `version` is compared field-by-field and numerically, so `1.10.0` is correctly
  newer than `1.9.0`.

- **Releases** — built installers are attached to the
  [Releases](https://github.com/itsmvtti/lume-releases/releases) of this repo.

## Publishing an update

1. Build and sign the installer.
2. Attach it to a new GitHub Release here.
3. Bump `version` in `version.json`, point `url` at the download, and write a
   one-line `notes`. That is what triggers the in-app "update available" prompt.

## Issues

Bug reports and feature requests are welcome in
[Issues](https://github.com/itsmvtti/lume-releases/issues).
