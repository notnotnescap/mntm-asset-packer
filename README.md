# Improved Asset Packer For Momentum
 An attempt to improve the asset packer script to make it more accessible and easier to use.

# Setup

1. Clone the repository
2. Create virtual environment `python3 -m venv venv`
3. Activate the virtual environment `source venv/bin/activate`
4. Install the requirements `pip3 install -r requirements.txt`

# Usage

```python3 asset_packer.py help```<br>
Displays help message

```python3 asset_packer.py create <Asset Pack Name>```<br>
Creates a directory with the correct file structure that can be used to prepare for the packing process.

```python3 asset_packer.py pack <./path/to/AssetPack>```<br>
Packs the specified asset pack into './asset_packs/Asset\ Pack\ Name'

```python3 asset_packer.py pack all```<br>
Packs all asset packs in the current directory into './asset_packs/'

```python3 asset_packer.py```<br>
same as *asset_packer.py pack all* (this is to keep compatibility with the original asset_packer.py)

```python3 asset_packer.py recover <./asset_packs/AssetPack>```<br>
    Recovers png frames from a compiled anim. (currently only works with anims) Recovered assets are saved in './recovered/example_anim'

```python3 asset_packer.py recover all```<br>
    Recovers all asset packs in './asset_packs/' into './recovered/'


```python3 asset_packer.py convert <./path/to/AssetPack>```<br>
Converts all frames to .png files and renames them to the correct format. (requires numbers in filenames)


# Features added to the original asset packer
note : the improved asset packer is backwards compatible with the original asset packer
- Packing specific asset packs
- A create command to create the necessary file structure for an asset pack
- Automatic file renaming and conversion
- Asset pack recovery from compiled state
