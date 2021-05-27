[![Version](https://vsmarketplacebadge.apphb.com/version-short/usernamehw.errorlens.svg)](https://marketplace.visualstudio.com/items?itemName=usernamehw.errorlens)
[![Installs](https://vsmarketplacebadge.apphb.com/installs-short/usernamehw.errorlens.svg)](https://marketplace.visualstudio.com/items?itemName=usernamehw.errorlens)
[![Rating](https://vsmarketplacebadge.apphb.com/rating-short/usernamehw.errorlens.svg)](https://marketplace.visualstudio.com/items?itemName=usernamehw.errorlens)
[![Trending](https://vsmarketplacebadge.apphb.com/trending-monthly/usernamehw.errorlens.svg)](https://marketplace.visualstudio.com/items?itemName=usernamehw.errorlens)

ErrorLens turbo-charges language diagnostic features by making diagnostics stand out more prominently, highlighting
the entire line wherever a diagnostic is generated by the language and also prints the message inline.

![Demo image](https://raw.githubusercontent.com/usernamehw/vscode-error-lens/master/img/demo.png)

## Features

- Highlight lines containing diagnostics
- Append diagnostic as text to the end of the line
- Show icons in gutter
- Show message in status bar

<!-- COMMANDS_START -->
## Commands (6)

|Command|Description|
|-|-|
|errorLens.toggle|Error Lens: Toggle (Enable/Disable) All Decorations|
|errorLens.toggleError|Error Lens: Toggle Errors|
|errorLens.toggleWarning|Error Lens: Toggle Warnings|
|errorLens.toggleInfo|Error Lens: Toggle Info|
|errorLens.toggleHint|Error Lens: Toggle Hint|
|errorLens.copyProblemMessage|Error Lens: Copy Problem Message|
<!-- COMMANDS_END -->
<!-- SETTINGS_START -->
## Settings (36)

> **Error Lens** extension settings start with `errorLens.`

|Setting|Default|Description|
|-|-|-|
|fontFamily|""|Font family of message. If the new font breaks layout - try to use smaller fontSize.|
|fontWeight|"normal"|Font Weight of message.`"normal"` is alias for 400, `"bold"` is alias for 700)|
|fontStyleItalic|**false**|When enabled - shows message in italic.|
|fontSize|""|Font size of message (CSS units).|
|margin|"4ch"|Distance between the end of the line and the message (CSS units).|
|padding|""|Padding of the message. Visible difference when `message` colors are set. [issues/23](https://github.com/usernamehw/vscode-error-lens/issues/23). Example: `2px 1ch`.|
|borderRadius|"3px"|Border radius of the message. Visible difference when `message` colors are set. [issues/23](https://github.com/usernamehw/vscode-error-lens/issues/23). Example: `5px`.|
|enabledDiagnosticLevels|["error","warning","info","hint"]|Customize which diagnostic levels to highlight.|
|annotationPrefix|["ERROR: ","WARNING: ","INFO: ","HINT: "]|Specify diagnostic message prefixes (when `addAnnotationTextPrefixes` is enabled). For example, emoji: ❗ ⚠ ℹ.|
|addAnnotationTextPrefixes|**false**|When enabled - prepends diagnostic severity ('ERROR:', 'WARNING:' etc) to the message. (Prefixes can be configured with `annotationPrefix` setting).|
|addNumberOfDiagnostics|**false**|When enabled - prepends number of diagnostics on the line. Like: `[1/2]`.|
|messageEnabled|**true**|Controls whether inline message is shown or not (Including background highlight).|
|statusBarMessageEnabled|**false**|When enabled - shows message in status bar.|
|statusBarColorsEnabled|**false**|When enabled - use message decoration foreground as color of Status Bar text.|
|statusBarMessageType|"activeLine"|Pick what to show in Status Bar: closest message or only message for the active line.|
|exclude|[]|Specify messages that should not be highlighted (RegExp).|
|excludeBySource|[]|Specify sources that should not be highlighted (string). Example: `["eslint"]`|
|excludePatterns|[]|Exclude files by using glob pattern. Example `["**/*.{ts,js}"]`|
|light||Specify color of decorations for when the light color theme is active.|
|delay|**0**|**EXPERIMENTAL** Delay (ms) before showing problem decorations (0 to disable).|
|onSave|**false**|When enabled - updates decorations only on document save.|
|onSaveTimeout|**1000**|Time period (ms) that used for showing decorations after the document save.|
|followCursor|"allLines"|Highlight only portion of the problems.|
|followCursorMore|**0**|Augments `followCursor`.<br>Adds number of lines to top and bottom when `followCursor` is `activeLine`.<br> Adds number of closest problems when `followCursor` is `closestProblem`|
|gutterIconsEnabled|**false**|When enabled - shows gutter icons (In place of the debug breakpoint icon).|
|gutterIconsFollowCursorOverride|**true**|When enabled and `followCursor` setting is not `allLines`, then gutter icons would be rendered for all problems. But line decorations (background, message) only for active line.|
|gutterIconSize|"100%"|Change gutter icon size. Examples: `auto`, `contain`, `cover`, `50%`, `150%`|
|gutterIconSet|"default"|Change gutter icon style.|
|errorGutterIconPath||Absolute path to error gutter icon.|
|warningGutterIconPath||Absolute path to warning gutter icon.|
|infoGutterIconPath||Absolute path to info gutter icon.|
|errorGutterIconColor|"#e45454"|Error color of `circle` gutter icon set.|
|warningGutterIconColor|"#ff942f"|Warning color of `circle` gutter icon set.|
|infoGutterIconColor|"#00b7e4"|Info color of `circle` gutter icon set.|
|removeLinebreaks|**false**|When enabled - replaces line breaks in inline diagnostic message with `⏎` sign.|
|scrollbarHackEnabled|**false**|When enabled - prevents showing horizontal scrollbar for decorations. (Might have a conflict with `errorLens.fontFamily` or `errorLens.padding` settings).|
<!-- SETTINGS_END -->
<!-- COLORS_START -->
## Colors (24)

|Color|Dark|Light|HC|Description|
|-|-|-|-|-|
|errorLens.errorBackground|`#e454541b`|`#e4545420`|`#e454541b`|Background color of the entire line containing error.|
|errorLens.errorMessageBackground|`#fff0`|`#fff0`|`#fff0`|Background color of the error message.|
|errorLens.errorBackgroundLight|`#e4545420`|`#e4545420`|`#e4545420`|Background color of the entire line containing error (Only in light themes).|
|errorLens.errorForeground|`#ff6464`|`#e45454`|`#ff6464`|Text color used to highlight lines containing errors.|
|errorLens.errorForegroundLight|`#e45454`|`#e45454`|`#e45454`|Text color used to highlight lines containing errors (Only in light themes).|
|errorLens.warningBackground|`#ff942f1b`|`#ff942f20`|`#ff942f1b`|Background color used to highlight lines containing warnings.|
|errorLens.warningMessageBackground|`#fff0`|`#fff0`|`#fff0`|Background color of the warning message.|
|errorLens.warningBackgroundLight|`#ff942f20`|`#ff942f20`|`#ff942f20`|Background color used to highlight lines containing warnings (Only in light themes).|
|errorLens.warningForeground|`#fa973a`|`#ff942f`|`#fa973a`|Text color used to highlight lines containing warnings.|
|errorLens.warningForegroundLight|`#ff942f`|`#ff942f`|`#ff942f`|Text color used to highlight lines containing warnings (Only in light themes).|
|errorLens.infoBackground|`#00b7e420`|`#00b7e420`|`#00b7e420`|Background color used to highlight lines containing info.|
|errorLens.infoMessageBackground|`#fff0`|`#fff0`|`#fff0`|Background color of the info message.|
|errorLens.infoBackgroundLight|`#00b7e420`|`#00b7e420`|`#00b7e420`|Background color used to highlight lines containing info (Only in light themes).|
|errorLens.infoForeground|`#00b7e4`|`#00b7e4`|`#00b7e4`|Text color used to highlight lines containing info.|
|errorLens.infoForegroundLight|`#00b7e4`|`#00b7e4`|`#00b7e4`|Text color used to highlight lines containing info (Only in light themes).|
|errorLens.hintBackground|`#17a2a220`|`#17a2a220`|`#17a2a220`|Background color used to highlight lines containing hints.|
|errorLens.hintMessageBackground|`#fff0`|`#fff0`|`#fff0`|Background color of the hint message.|
|errorLens.hintBackgroundLight|`#17a2a220`|`#17a2a220`|`#17a2a220`|Background color used to highlight lines containing hints (Only in light themes).|
|errorLens.hintForeground|`#2faf64`|`#2faf64`|`#2faf64`|Text color used to highlight lines containing hints.|
|errorLens.hintForegroundLight|`#2faf64`|`#2faf64`|`#2faf64`|Text color used to highlight lines containing hints (Only in light themes).|
|errorLens.statusBarErrorForeground|`#ff6464`|`#e45454`|`#ff6464`|Status bar item error color.|
|errorLens.statusBarWarningForeground|`#fa973a`|`#ff942f`|`#fa973a`|Status bar item warning color.|
|errorLens.statusBarInfoForeground|`#00b7e4`|`#00b7e4`|`#00b7e4`|Status bar item info color.|
|errorLens.statusBarHintForeground|`#2faf64`|`#2faf64`|`#2faf64`|Status bar item hint color.|
<!-- COLORS_END -->
<br>

> Colors can be configured in `settings.json` (**`workbench.colorCustomizations`** section)

> `#fff0` - is a completely transparent color.

## Upstream issues

Please upvote the following VS Code issues:

* [Api for editor insets](https://github.com/microsoft/vscode/issues/85682)
* [[theming] Access theme's colors programmatically](https://github.com/microsoft/vscode/issues/32813)
* [[theming] when completing color keys in settings, fill in current value](https://github.com/microsoft/vscode/issues/25633)
* [Inline text adornments break word wrapping](https://github.com/microsoft/vscode/issues/32856)
* [OnClick event on Gutter](https://github.com/microsoft/vscode/issues/5455)