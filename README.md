## Overview

The **Coomer Downloader** is a Python-based utility for downloading content from platforms such as **OnlyFans**, **Fansly**, and **CandFans** through the Coomer API. It simplifies the process of fetching and organizing media files, offering multi-threaded downloads and progress tracking for a seamless experience.

---

## Features

- Supports downloading from **OnlyFans**, **Fansly**, and **CandFans**.
- Multi-threaded downloads for faster performance.
- Progress bars for tracking both page loading and file downloads.
- Options to download all content or only specific media files (e.g., images, videos).
- Filters out thumbnails and zip files by default (configurable).

---

## Requirements

Before using the downloader, ensure you have Python installed along with the following libraries:

- `os`
- `requests`
- `urllib.parse`
- `pathlib`
- `tqdm`
- `concurrent.futures`

If any required library is missing, the script will attempt to install it automatically.

---

## Installation

1. Clone or download this repository.
2. Navigate to the directory containing the script.
3. Install dependencies manually (if required):
   ```bash
   pip install requests tqdm
   ```

---

## Usage

1. **Run the Script**  
   Start the downloader by running the script:
   ```bash
   python "coomer_dl.py"
   ```

2. **Provide the Artist URL**  
   Enter the URL of the artist's page (e.g., `https://coomer.su/onlyfans/user/{user_id}`).

3. **Select Download Option**  
   Choose to:
   - Download all files (`1`), or
   - Only media files (`2`).

4. **Choose Download Directory**  
   Specify the folder where files will be saved.

5. **Wait for Download Completion**  
   The script will display progress bars for page loading and file downloads.  

   Once complete, a confirmation message will be displayed.

---

## File Filtering

By default, the downloader excludes:
- **Thumbnails**: Files with `_thumb` in their names.
- **Zip Files**: Files with the `.zip` extension.

The filtering behavior can be adjusted in the script.

---

## Customization

- **Supported Platforms**  
  The script uses a dictionary for platform API endpoints. Add or modify entries in the `platform_api_endpoints` dictionary to extend platform support.

- **Media File Extensions**  
  To support additional file types, add extensions to the `media_file_extensions` set.

- **Thread Count**  
  The number of concurrent downloads is set to `5`. Adjust the `max_workers` parameter in the `ThreadPoolExecutor` for different performance levels.

---

## Known Limitations

- The script relies on the Coomer API and may not function if the API changes or becomes unavailable.
- Large-scale downloads may require sufficient disk space and bandwidth.

---

## Disclaimer

This tool is intended for personal use. Ensure that you have the necessary permissions to download content. The author is not responsible for any misuse of this tool.

---

## License

This project is open-source and distributed under the MIT License. Feel free to modify and distribute it as needed.
