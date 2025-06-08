# chrome-default-jamfpro
This script can be used in Jamf Pro to set Chrome as default browser on Macs 
# Chrome Default Browser Setup Script for macOS

## Description

This Bash script automates the process of setting Google Chrome as the default browser for HTTP and HTTPS protocols on macOS systems. It's designed to run with user-level permissions and includes logging for troubleshooting purposes.

## Key Features

- Detects the currently logged-in user (skips execution if no user or root is detected)
- Sets Chrome as the default handler for both HTTP and HTTPS URLs
- Rebuilds the macOS LaunchServices database to apply changes
- Restarts Finder to ensure changes take effect immediately
- Includes comprehensive logging to `/tmp/set_chrome_default.log`

## Usage

1. Save the script as `chrome.sh`
2. Make it executable: `chmod +x chrome.sh`
3. Run it: `./chrome.sh`

## Requirements

- macOS operating system
- Google Chrome installed (with bundle identifier `com.google.chrome`)
- Standard user permissions (won't run as root)

## Notes

- The script is non-destructive and adds to existing URL handlers rather than replacing them
- Logs are written to `/tmp/set_chrome_default.log` for troubleshooting
- Changes take effect immediately after script completion

This script is particularly useful for IT administrators managing macOS environments or users who want to ensure Chrome is their default browser across all scenarios.
