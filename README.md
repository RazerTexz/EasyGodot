# Configuring The Workflow
The workflow variables are defined in [godot-export.yml](https://github.com/RazerTexz/EasyGodot/blob/main/.github/workflows/godot-export.yml).

## Workflow Variables
| Variable Name               | Description                                           |
|-----------------------------|-------------------------------------------------------|
| `KEYSTORE_DEBUG_ALIAS`      | The alias name for the debug keystore.                |
| `KEYSTORE_DEBUG_PASSWORD`   | The password for the debug keystore.                  |
| `KEYSTORE_RELEASE_ALIAS`    | The alias name for the release keystore.              |
| `KEYSTORE_RELEASE_PASSWORD` | The password for the release keystore.                |

# Mono Setup
Read [this](https://github.com/firebelley/godot-export?tab=readme-ov-file#mono-builds)

# Android Setup
> [!NOTE]
> Make sure to enable the `import_etc2_astc` option in project settings!

1. In the root of your project, make a folder named `.godot`
2. Inside the folder, make a file named `export_credentials.cfg`
3. Open the file and write this inside of it:
```gdscript
[preset.0]

script_encryption_key=""

[preset.0.options]

keystore/debug="KEYSTORE_DEBUG_PATH"
keystore/debug_user="KEYSTORE_DEBUG_ALIAS"
keystore/debug_password="KEYSTORE_DEBUG_PASSWORD"
keystore/release="KEYSTORE_RELEASE_PATH"
keystore/release_user="KEYSTORE_RELEASE_ALIAS"
keystore/release_password="KEYSTORE_RELEASE_PASSWORD"
```

# Credits
- [Godot Engine](https://godotengine.org)
- [FireBelley](https://github.com/firebelley) for the [workflow action](https://github.com/firebelley/godot-export).
