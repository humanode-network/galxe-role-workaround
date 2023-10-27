# Galxe Role Workaround

Galxe has a bug in their system that does not allow selecting a linked role (BotBasher-powered roles for instance) via their web app UI.

It is absolutely capable of working with linked roles and allows creating them via the API just fine.

Here is the tooling to make the API requests that matches what the credential creation UI does, but without the needless restrictions, since you fill in the parameters however you like.

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
