[![add-on registry](https://img.shields.io/badge/DDEV-Add--on_Registry-blue)](https://addons.ddev.com)
[![tests](https://github.com/kwasib/ddev-keydbmanager/actions/workflows/tests.yml/badge.svg?branch=main)](https://github.com/kwasib/ddev-keydbmanager/actions/workflows/tests.yml?query=branch%3Amain)
[![last commit](https://img.shields.io/github/last-commit/kwasib/ddev-keydbmanager)](https://github.com/kwasib/ddev-keydbmanager/commits)
[![release](https://img.shields.io/github/v/release/kwasib/ddev-keydbmanager)](https://github.com/kwasib/ddev-keydbmanager/releases/latest)

# DDEV KeyDB Manager

## Overview

This add-on integrates KeyDB Manager into your [DDEV](https://ddev.com/) project.

## Requirements

Before installing this add-on, the [KeyDB service](https://github.com/kwasib/ddev-keydb) must be available:

```bash
ddev add-on get kwasib/ddev-keydb
```

## Installation

```bash
ddev add-on get kwasib/ddev-keydbmanager
ddev restart
```

After installation, make sure to commit the `.ddev` directory to version control.

## Usage

| Command | Description |
| ------- | ----------- |
| `ddev keydbmanager` | Open KeyDB Manager in your browser (`https://<project>.ddev.site:5000`)  |
| `ddev describe` | View service status and used ports for Keydbmanager |
| `ddev logs -s keydbmanager` | Check Keydbmanager logs |

## Advanced Customization

To change the Docker image:

```bash
ddev dotenv set .ddev/.env.keydbmanager --keydbmanager-docker-image="eqalpha/keydbmanager:latest"
ddev add-on get kwasib/ddev-keydbmanager
ddev restart
```

Make sure to commit the `.ddev/.env.keydbmanager` file to version control.

All customization options (use with caution):

| Variable | Flag | Default |
| -------- | ---- | ------- |
| `KEYDBMANAGER_DOCKER_IMAGE` | `--keydbmanager-docker-image` | `eqalpha/keydbmanager:latest` |

## Credits

**Contributed and maintained by [@kwasib](https://github.com/kwasib)**
