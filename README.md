# **YouTube Watch Later Exporter**

A Chrome extension to export your YouTube "Watch Later" playlist as a JSON file.

## **Features**

*   Automatically collects video titles and URLs from your YouTube Watch Later playlist.
*   Exports the collected data as a downloadable JSON file.
*   Simple and lightweight popup interface to trigger the export process.

## **Installation**

Clone or download this repository:  
```
git clone https://github.com/afnan-nex/yt-watchlater-exporter
```
1.  Open Chrome and navigate to `chrome://extensions/`.
2.  Enable **Developer mode** (toggle in the top-right corner).
3.  Click **Load unpacked** and select the folder containing the extension files.
4.  The extension should now appear in your Chrome extensions list.

## **Usage**

1.  Click the extension icon in Chrome to open the popup.
2.  Click the **Export Now** button to open your YouTube Watch Later playlist.
3.  The extension will automatically collect video data and download it as `watch_later_videos.json` after a short delay (to ensure the page is fully loaded).
4.  If no videos are found, an alert will notify you.

## **Files**

*   `manifest.json`: Defines the extension's configuration, permissions, and content scripts.
*   `content.js`: Contains the logic to scrape video titles and URLs from the Watch Later playlist and trigger the JSON download.
*   `popup.html`: The HTML for the extension's popup interface.
*   `popup.js`: Handles the button click event to open the Watch Later playlist.
*   `style.css`: Basic styling for the popup interface.

## **Permissions**

The extension requires the following permissions:

*   `tabs`: To open the YouTube Watch Later playlist.
*   `scripting`: To execute scripts on the YouTube page.
*   `host_permissions` for `https://www.youtube.com/\*`: To access and scrape the Watch Later playlist page.

## **Notes**

*   The extension waits 5 seconds after the page loads to ensure all video elements are available before scraping.
*   If the export fails, ensure you are logged into YouTube and the Watch Later playlist (`https://www.youtube.com/playlist?list=WL`) is accessible.
*   The exported JSON file contains an array of objects with `title` and `url` fields for each video.

## **License**

This project is licensed under the MIT License. See the [LICENSE](https://grok.com/chat/LICENSE) file for details.

## **Contributing**

Contributions are welcome! Please feel free to submit a pull request or open an issue for any bugs or feature requests.

## **Author**

Afnan Siddiqui

© 2025 Afnan Siddiqui
