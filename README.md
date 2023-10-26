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
export NAME="..."
export DESCRIPTION="..."
export REFERENCE_LINK="https://discord.gg/..."

export CURATOR_SPACE_ID=".."

export GUILD_ID="..."
export ROLE_NAME="..."
export ROLE_ID="..."

export ACCESS_TOKEN="..." #  Galxe API token
```

## Run the script

Set your current directory to ``.

```bash
bin/create-credential
```

The script load the `.env` file automatically.
