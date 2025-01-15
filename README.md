# Improved Asset Packer For Flipper Zero
 An attempt to improve the asset packer script to make it more accessible and easier to use.

# This is a work in progress and nothing really works yet.

# Setup

1. Clone the repository
2. Create virtual environment `python -m venv venv` (depends on your python version)
3. Activate the virtual environment `source venv/bin/activate`
4. Install the requirements `pip install -r requirements.txt`

# Usage

`python3 auto_asset_packer.py help`
Displays help message

`python3 auto_asset_packer.py create <Asset Pack Name>`
Creates a directory with the correct file structure that can be used to prepare for the packing process. (does not work yet)

`python3 auto_asset_packer.py pack all`
Packs all asset packs in the current directory into './asset_packs/'

`python3 auto_asset_packer.py pack <./Asset\ Pack\ Name>`
Packs the specified asset pack into './asset_packs/Asset\ Pack\ Name' (does not work yet)

# Roadmap
- [ ] create command
- [ ] pack specific asset pack command
- [ ] automatic file renaming
- [ ] automatic file conversion
- [ ] verbose error messages
- [ ] hopefully replace the current asset packer script
