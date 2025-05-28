# PSD/PSB File Optimizer

A wrapper script that optimizes PSD and PSB files by removing excessive metadata, resulting in smaller file sizes without affecting the content.

## Overview

This tool uses [psd_ockham](https://github.com/Playrix/psd_ockham) to reduce the size of Photoshop PSD and PSB files by removing unnecessary metadata. The script provides a convenient interface for batch processing files and displays a summary of space savings.

## Features

- Batch processing of multiple PSD/PSB files
- Support for organizing files in subfolders
- Preserves subfolder structure in the output directory
- Clear visual feedback on optimization results
- Automatic creation of input/output directories
- Preserves original files (optimized versions are saved separately)
- Copies non-PSD/PSB files unchanged to maintain complete directory structures
- Detailed summary of space savings

## Requirements

- macOS (the script is designed to run in macOS Terminal)
- [psd_ockham](https://github.com/Playrix/psd_ockham/releases) binary (must be downloaded separately)

## Installation

1. Clone or download this repository
2. Download the latest version of [psd_ockham](https://github.com/Playrix/psd_ockham/releases)
3. Place the `psd_ockham` binary in the same directory as the `optimize_psd` script
4. Make both files executable:
   ```bash
   chmod +x optimize_psd
   chmod +x psd_ockham
   ```

## Usage

1. Place your PSD/PSB files in the `input` directory (will be created automatically if it doesn't exist)
   - You can organize files in subfolders within the `input` directory
   - The subfolder structure will be preserved in the output
2. Run the script by double click or with terminal:
   ```bash
   ./optimize_psd
   ```
3. Optimized files will be saved in the `output` directory with the same folder structure as input
4. The script will display a summary of the optimization results, including:
   - Original file size
   - New file size
   - Space saved
   - Total space saved across all files

## How It Works

The script:
1. Checks for the presence of the required `psd_ockham` binary
2. Creates input/output directories if they don't exist
3. Recursively finds all files in the input directory, including those in subfolders
4. Processes each PSD/PSB file while preserving the subfolder structure in the output
5. Copies non-PSD/PSB files to the output directory unchanged
6. Displays a formatted table with optimization results
7. Shows the total space saved

## Credits

- Idea by Anastasiia Azartseva
- Implementation by Alex Azartsev
- [psd_ockham](https://github.com/Playrix/psd_ockham) by Playrix

## License

This project is licensed under the GNU General Public License v3.0 (GPL-3.0) - see the [GNU GPL v3](https://www.gnu.org/licenses/gpl-3.0.en.html) for details.

The GNU General Public License is a free, copyleft license for software and other kinds of works. This license ensures that:

- You are free to use, modify, and distribute this software
- Any modifications to the software must also be distributed under the GPL
- The source code must be made available when the software is distributed
- Any derivative works must be released under the same license

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.
