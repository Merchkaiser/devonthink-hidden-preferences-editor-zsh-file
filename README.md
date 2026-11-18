# DEVONthink Curated Preferences Editor

A macOS GUI for browsing and changing a curated set of **DEVONthink preferences**, including advanced and hidden settings. This standalone **zsh** utility builds and launches a temporary **Swift/AppKit** preferences editor using Apple's `xcrun swift` toolchain—no Homebrew or separate app build is required.

> Unofficial community utility; not affiliated with or endorsed by DEVONtechnologies.

## What it does

- Browse and search settings organized into categories, with descriptions and source notes.
- Edit supported Boolean settings, choices, numeric ranges, text, and multiline text.
- Use native macOS pickers for folders, fonts, colors, text encodings, and file extensions.
- Explore settings related to the DEVONthink interface, files and indexing, Markdown, PDFs and media, OCR, search, metadata, feeds, web browsing, sync/server, and AI/chat.
- Optionally show error alerts, minimize the launching Terminal window, and relaunch DEVONthink after the editor closes.

The editor exposes only the preferences and control types defined in its script. Hidden or legacy preferences can change between DEVONthink versions and may have no effect.

## Requirements

- macOS
- DEVONthink installed
- Apple's Swift toolchain available as `xcrun swift` (install Apple Command Line Tools if needed)

## Run

The script in this repository is currently named `MOVED TO GOOGLE DRIVE - Script` (despite its contents being the utility). From the repository directory, run:

```sh
chmod +x "MOVED TO GOOGLE DRIVE - Script"
./"MOVED TO GOOGLE DRIVE - Script"
```

You can alternatively rename the downloaded script to `DEVONthink_Curated_Preferences_Editor.zsh` and run it with `zsh DEVONthink_Curated_Preferences_Editor.zsh`.

## Before changing preferences

**Back up your DEVONthink preferences first.** Quit DEVONthink before editing settings where practical. The utility attempts to quit DEVONthink before writing changes; if it cannot, it asks you to quit the app and try again. Review each setting carefully: undocumented, hidden, and version-specific preferences may behave unexpectedly.

The script creates temporary Swift source files at launch and removes them when it exits. It does not install a separate application.

## Optional script settings

The following variables near the top of the script control optional behavior:

```sh
DO_YOU_WANT_ERROR_POPUPS__YES_NO="YES"
MINIMIZE_LAUNCHING_TERMINAL__YES_NO="YES"
RELAUNCH_DEVONTHINK_AFTER_EDITOR_CLOSES__YES_NO="NO"
```

## Troubleshooting

- **`xcrun` or Swift not found:** install or configure Apple's Command Line Tools, then verify `xcrun --find swift` works in Terminal.
- **DEVONthink is still running:** quit DEVONthink completely and retry before changing preferences.
- **A setting is missing or has no effect:** availability and behavior can depend on your DEVONthink version; some keys are hidden, legacy, or unsupported.

## License and disclaimer

No license is currently specified in this repository. Unless a license is added, do not assume the code is available for reuse under an open-source license. This is an unofficial community project, provided as-is, with no warranty or affiliation with DEVONtechnologies.
