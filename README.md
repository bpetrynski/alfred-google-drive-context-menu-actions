# Alfred Google Drive Context Menu Actions

An Alfred Workflow to trigger context menu actions in Google Drive.

## Overview

This workflow allows you to perform right-click context menu actions on files within Google Drive directly from Alfred.

## Features

- Copy Google Drive link to clipboard
- Open files with Google Drive apps
- Share files using Google Drive sharing options

## Requirements

- Alfred Powerpack
- macOS with Google Drive installed

## Installation

1. Download the workflow file.
2. Double-click to import into Alfred.
3. Ensure Google Drive is running in the background.

## Usage

Select a file in Finder and activate Alfred workflow with the designated keyword or hotkey. Choose from the following actions:
- Copy Google Drive Link URL to Clipboard
- Open with Google Drive
- Share with Google Drive

## Script Example

Below is a snippet of the AppleScript used in this workflow:

```applescript
on run
  tell application "System Events" to tell application process "Finder"
    set selectedFile to value of attribute "AXFocusedUIElement"
    tell selectedFile to perform action "AXShowMenu"
    delay 0.5
    keystroke "Copy link to clipboard"
    -- Sends enter
    key code 36
  end tell  
end run
```
