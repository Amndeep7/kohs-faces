![Koh's Faces Icon](icons/icon.svg "Koh's Faces Icon")

# Koh's Faces

| Add-on/Extension Repository/Store |
| --- |
| [Firefox](https://addons.mozilla.org/en-US/firefox/addon/kohs-faces/) |
| [Chrome](https://chrome.google.com/webstore/detail/kohs-faces/hjbiodcicoonaniboaeogfcecldjhcbb)

---

A WebExtension that adds additional, "non-official" commentfaces to /r/anime's commentface line-up.

## Why?
Reddit doesn't provide a large amount of space on their spritesheet for subreddits to play with, so the mods have been reluctant to add or remove commentfaces due to it being a massive pain on their end to make it all fit.  This extension and associated scripts solve both of these issues by externalizing the storage of commentfaces and making it easy for subscribers to add faces that they desire to the repository.

## How can I add my own?
Submit a pull request and I will almost certainly approve it so long as it doesn't violate Reddit's or /r/anime's rules and doesn't look bad (too big, too small, too grainy, etc.).

More detailed instructions:
1. (Make an account and) log into Github.
2. Click on `commentfaces.css`.
3. In the row where it says `Raw`, `Blame`, etc., there's a button that looks like a pencil, click that button.
4. Copy one of the ones already there and modify it to fit what you want to make:
	- Change the name of the source
	- Change the name of the commentface (has to start with a double `##`)
	- Change the url (has to be a direct link to the picture or sprite sheet)
	- Change the height and width (make sue to match the actual size of the picture since these measurements will not cause the picture to scale)
	- Change the animation specific values
5. Provide a commit message specifying the show and the commentface names and maybe a little something to make my day.
6. Submit the pull request.
7. Ping me on Reddit if I don't get to it fast enough.

If you're looking to make an animated commentface, I've found [ezgif](https://ezgif.com/gif-to-sprite/) to be a useful tool.  Just make sure to copy and paste the generated sprite sheet onto imgur or other host cause I believe ezgif doesn't host the pictures for too long.

---

## Building the extension
### System dev-dependencies
  * Inkscape - Cmdline tool to convert icon.svg into a set of resized PNG files
  * Unix-like operating system - The build script at least assumes you got bash
  * web-ext - Mozilla's script for "compiling" extensions

### Build process
Run `build` to generate the icons.

Run `web-ext build` to generate the extension artifact.
