
<h1 align="center">
  <br>
  <img src="https://raw.githubusercontent.com/corollari/waspline-reader/master/promo/wasp.png" width="200"></a>
  <br>
  WaspLine Reader
  <br>
</h1>

<h4 align="center">FOSS version of <a href="http://www.beelinereader.com/" target="_blank">BeeLine Reader</a>, a web browser extension that uses color-gradients to help with reading</h4>

<p align="center">
  <a href="#install">Install</a> •
  <a href="#build">Build</a> •
  <a href="#credits">Credits</a> •
  <a href="#to-do">TO-DO</a> •
  <a href="#license">License</a>
</p>

![screenshot](https://raw.githubusercontent.com/corollari/waspline-reader/master/promo/screenshot.png)

## Install
The extension can be installed through [Chrome's Web Store](https://chrome.google.com/webstore/detail/waspline-reader/ndlnnojbbcbdpkccfmcgbopalpbmhbhm) or [Firefox Add-ons](https://addons.mozilla.org/en-US/firefox/addon/waspline-reader/).

## Build
```bash
git clone --recursive https://github.com/corollari/waspline-reader.git
cd waspline-reader
bash build.sh
```

## Safari Extension
You can also install this extension on Safari on macOS. However, it’s more involved.

1. First, follow the build instructions.
2. Then run the following:

    ```bash
    xcrun safari-web-extension-converter extension/ --copy-resources --project-location xcode-project --macos-only --bundle-identifier com.waspline-reader.macos-extension --no-open
    xcodebuild -scheme "WaspLine Reader" DSTROOT=".." archive -project xcode-project/WaspLine\ Reader/WaspLine\ Reader.xcodeproj/
    open xcode-project/Applications/WaspLine\ Reader.app/
    ```

    You will see an app launch called WaspLine Reader. It will have a button that says “Quit and Open Safari Extensions Preferences”. However, the extension won’t show up in Safari just yet. You first need to enable the Develop menu in Safari and allow unsigned extensions.
    
3. Launch Safari. In the menu bar, choose Safari > Preferences. Select the Advanced tab, and check the “Show Develop menu in menu bar” option.
4. In the Safari menu bar, tick Develop > Allow Unsigned Extensions. (This setting is reset when you quit Safari, but the extension will stay installed.)
5. Finally, you can enable the extension: Choose Safari > Preferences. Select the Extensions tab. Find WaspLine Reader in the list on the left, and enable it by selecting the checkbox.
6. You’ll now see WaspLine Reader in the Safari toolbar. To enable it: Click the WaspLine Reader icon in the Safari toolbar and tick “Enable WaspLine” in the pop-up. You’ll need to reload any already opened tabs for it to take effect.

## Credits
The following external resources have been included as part of the project:
- A [slightly modified version](https://github.com/corollari/js-line-wrap-detector) of [jsLineWrapDetector](https://github.com/xdamman/js-line-wrap-detector) is used to separate the text in lines
- The [wasp icon](https://icons8.com/icon/6558/wasp) used in the extension comes from Icons8's Free License icon collection
- The landing page is a heavily modified version of [Elevate](https://www.styleshout.com/free-templates/elevate/), a web template provided by [StyleShout](https://www.styleshout.com/)

The extension has been greatly improved by @InvisibleUp, and the Safari build instructions are due to @yatharth.

## TO-DO
- [ ] Integrate Readability into the extension so the color gradients are only applied to the main text

## License
The Unlicense
