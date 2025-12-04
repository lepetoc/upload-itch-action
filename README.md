# Upload to Itch — GitHub Action

This GitHub Action installs the Itch.io Butler CLI and uploads a build to your Itch.io project.
Butler handles patching, versioning, platform channels, and efficient differential uploads.

📘 Butler documentation:
https://itch.io/docs/butler/

## Features

- 🚀 Automatically installs the Butler CLI on the GitHub runner

- 🔑 Securely uses your Itch.io API key to authenticate uploads

- 📂 Upload any folder or .zip file as your game build

- 🏷️ Supports custom version tags, or allows Butler to generate one

- 🔄 Push to any Itch.io channel (e.g., windows, linux, html5)

- 🔧 Works on any workflow using composite actions

## Inputs

| Name        | Required | Description                                                                                                                                                        |
| ----------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `api_key`   | ✔️       | Your **Butler API key**. Generate one [using the Butler CLI](https://itch.io/docs/butler/login.html#logging-in).                                                   |
| `directory` | ✔️       | Directory or `.zip` file to upload.                                                                                                                                |
| `project`   | ✔️       | Your Itch project identifier in the form `user/project`.                                                                                                           |
| `channel`   | ✔️       | Upload channel such as `windows`, `linux`, `mac`, `html5`, etc. [Official documentation](https://itch.io/docs/butler/pushing.html#channel-names)                   |
| `version`   | ❌       | Optional version tag. If omitted, Butler auto-generates one. [Official documentation](https://itch.io/docs/butler/pushing.html#specifying-your-own-version-number) |
