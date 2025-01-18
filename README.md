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

```python3 asset_packer.py convert <./Asset\ Pack\ Directory>```
Converts all frames to .png files and renames them to the correct format. (requires numbers in filenames)

```python3 asset_packer.py pack all```<br>
Packs all asset packs in the current directory into './asset_packs/'

```python3 asset_packer.py```<br>
same as *asset_packer.py pack all* (this is to keep compatibility with the original asset_packer.py)

```python3 asset_packer.py pack <./Asset\ Pack\ Directory>```<br>
Packs the specified asset pack into './asset_packs/Asset\ Pack\ Name'

# Roadmap
- [x] pack specific asset pack command
- [x] create command
- [x] automatic file renaming
- [x] automatic file conversion
- [ ] convert .bm or .bmx files back to .png -> recover command
- [ ] hopefully replace the current asset packer script
- [ ] GUI?
