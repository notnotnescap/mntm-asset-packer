# mtm-asset-packer

An improved asset packer script to make the process of creating and packing asset packs for the Momentum firmware easier. This script is designed to be backwards compatible with the original packer while adding new features for a better user experience.

# Features

This improved packer adds several features over the original:

-   **Pack specific asset packs**: No need to pack everything at once.
-   **Create command**: Quickly scaffold the necessary file structure for a new asset pack.
-   **Automatic file conversion**: Automatically convert and rename image frames for animations.
-   **Asset pack recovery**: Recover PNGs and metadata from compiled asset packs. (Note: Font recovery is not yet implemented).
-   **Backwards compatibility**: Works the same way as the original packer by default, so you can use it without changing your workflow.

# Setup

## Using [uv](https://docs.astral.sh/uv/) (recommended)

If you don't have `uv` installed, follow [these](https://docs.astral.sh/uv/getting-started/installation/) instructions.

You can quickly run the script without needing to install with this command:
```sh
uvx mtm-asset-packer help
```

If you want to install it globally, use this command:
```sh
uv tool install mtm-asset-packer
mtm-asset-packer help
```

## Using venv

1.  Clone this repository and navigate into its directory.
2.  Create and activate a virtual environment:
    ```sh
    python3 -m venv venv
    source venv/bin/activate
    ```
3.  Install the required dependencies from [`requirements.txt`](requirements.txt):
    ```sh
    pip install -r requirements.txt
    ```


# Usage

If you run the script directly, replace `mtm-asset-packer` with `python3 mtm_asset_packer.py` in the commands below.

`mtm-asset-packer help`
: Displays a detailed help message with all available commands.

`mtm-asset-packer create <Asset Pack Name>`
: Creates a directory with the correct file structure to start a new asset pack.

`mtm-asset-packer pack <./path/to/AssetPack>`
: Packs a single, specified asset pack into the `./asset_packs/` directory.

`mtm-asset-packer pack all`
: Packs all valid asset pack folders found in the current directory into `./asset_packs/`. This is the default action if no command is provided.

`mtm-asset-packer recover <./asset_packs/AssetPack>`
: Recovers a compiled asset pack back to its source form (e.g., `.bmx` to `.png`). The recovered pack is saved in `./recovered/<AssetPackName>`.

`mtm-asset-packer recover all`
: Recovers all asset packs from the `./asset_packs/` directory into the `./recovered/` directory.

`mtm-asset-packer convert <./path/to/AssetPack>`
: Converts and renames all animation frames in an asset pack to the standard `frame_N.png` format.

# More Information

-   **General Asset Info**: [https://github.com/Kuronons/FZ_graphics](https://github.com/Kuronons/FZ_graphics)
-   **Animation `meta.txt` Guide**: [https://flipper.wiki/tutorials/Animation_guide_meta/Meta_settings_guide/](https://flipper.wiki/tutorials/Animation_guide_meta/Meta_settings_guide/)
-   **Custom Fonts Guide**: [https://flipper.wiki/tutorials/f0_fonts_guide/guide/](https://flipper.wiki/tutorials/f0_fonts_guide/guide/)
