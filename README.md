# Improved Asset Packer For Momentum

An improved asset packer script to make the process of creating and packing asset packs for the Momentum firmware easier. This script is designed to be backwards compatible with the original packer while adding new features for a better user experience.

# Features

This improved packer adds several features over the original:

-   **Pack specific asset packs**: No need to pack everything at once.
-   **Create command**: Quickly scaffold the necessary file structure for a new asset pack.
-   **Automatic file conversion**: Automatically convert and rename image frames for animations.
-   **Asset pack recovery**: Recover PNGs and metadata from compiled asset packs. (Note: Font recovery is not yet implemented).

# Setup

## Using `venv` (standard Python)

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

## Using `uv`

If you have [uv](https://docs.astral.sh/uv/) installed, you can use it to run the script. It will handle creating an environment and installing dependencies from [`pyproject.toml`](pyproject.toml) automatically.

After cloning the repository, you can run any script command like this:
```sh
uv run asset_packer.py help
```

# Usage

The script is invoked from the command line. Here are the available commands:

`python3 asset_packer.py help`
: Displays a detailed help message with all available commands.

`python3 asset_packer.py create <Asset Pack Name>`
: Creates a directory with the correct file structure to start a new asset pack.

`python3 asset_packer.py pack <./path/to/AssetPack>`
: Packs a single, specified asset pack into the `./asset_packs/` directory.

`python3 asset_packer.py pack all`
: Packs all valid asset pack folders found in the current directory into `./asset_packs/`. This is the default action if no command is provided.

`python3 asset_packer.py recover <./asset_packs/AssetPack>`
: Recovers a compiled asset pack back to its source form (e.g., `.bmx` to `.png`). The recovered pack is saved in `./recovered/<AssetPackName>`.

`python3 asset_packer.py recover all`
: Recovers all asset packs from the `./asset_packs/` directory into the `./recovered/` directory.

`python3 asset_packer.py convert <./path/to/AssetPack>`
: Converts and renames all animation frames in an asset pack to the standard `frame_N.png` format.

# More Information

-   **General Asset Info**: [https://github.com/Kuronons/FZ_graphics](https://github.com/Kuronons/FZ_graphics)
-   **Animation `meta.txt` Guide**: [https://flipper.wiki/tutorials/Animation_guide_meta/Meta_settings_guide/](https://flipper.wiki/tutorials/Animation_guide_meta/Meta_settings_guide/)
-   **Custom Fonts Guide**: [https://flipper.wiki/tutorials/f0_fonts_guide/guide/](https://flipper.wiki/tutorials/f0_fonts_guide/guide/)