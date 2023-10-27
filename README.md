# Galxe Role Workaround

## Setup

### Install dependencies

- `jq`
- `curl`

### Get the API token

Get the galxe API key.

<https://galxe.com/accountSetting?tab=AccessToken>

### Create config

Create `.env` file:

```bash
export NAME="..." # Galxe credential name
export DESCRIPTION="..." # Galxe credential description
export REFERENCE_LINK="https://discord.gg/..." # a Discord invite to a server with the role

export CURATOR_SPACE_ID="..." # Galxe space ID

export GUILD_ID="..." # the ID of the Discord server
export ROLE_NAME="..." # the name of the Discord role
export ROLE_ID="..." # the ID of the Discord role

export ACCESS_TOKEN="..." #  Galxe API token
```

## Run the script

Set your current directory to the root directory of your local clone of this repo.

```bash
bin/create-credential
```

The command above loads the `.env` file automatically.
