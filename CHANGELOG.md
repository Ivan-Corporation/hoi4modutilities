# Change Log

All notable changes to the "hoi4modutilities" extension will be documented in this file.

Check [Keep a Changelog](http://keepachangelog.com/) for recommendations on how to structure this file.

## [0.5.1] - 2021/12/15 - Latest

### Fixed
* Support negative value of country colour.

## [0.5.0] - 2021/12/13

### Added
* Preview new supply system based on railway.
* New setting `hoi4ModUtilities.enableSupplyArea` to switch to old version development.

## [0.4.8] - 2021/10/15

### Fixed
* Remove context menu from preview panels.

## [0.4.7] - 2021/10/09

### Fixed
* `meta_effect` can't be parsed.

## [0.4.6] - 2021/05/22

### Added
* Support preview of `frameanimatedspritetype` and `textspritetype`.
* Support trusted workspaces feature in VSCode.

## [0.4.5] - 2020/12/08

### Changed
* Items in world map preview can be opened by double click instead of clicking button on toolbar.

### Fixed
* Show error message when size of map image is not multiply of 256.

## [0.4.4] - 2020/11/11

### Added
* `Display` option in world map preview, which can show or hide map components.
* `Export as image` button to export whole world map to an image.

### Fixed
* An issue that not all terrain definitions are read.
* An issue that connection between provinces are not visible when one of the province is out of view.

## [0.4.3] - 2020/10/07

### Added
* Show event picture in event tree.
* Partially supported Korean translation (Contributor: [gyhs(NIKA)](https://github.com/gyhs)).

### Fixed
* An issue that preview window closes even when text editor exists.

## [0.4.2] - 2020/08/23

### Added
* Focus tree preview supports multiple trees in one file now.

### Changed
* Changed preview `.tga` editor name.
* This extension will automatically activate when there're previewable files in workspace.

### Fixed
* Improve performace of edge rendering in world map preview.

## [0.4.1] - 2020/08/11

### Added
* Support `.tga` format image in all previews.

### Changed
* Event preview will show delay time of each event if not happen immediately.

### Fixed
* Preview doesn't properly update when document has circular dependencies.

## [0.4.0] - 2020/07/29

### Added
* Event tree preview
  * Show relationship of events.
  * Easily navigate from preview to event definition.
  * Resolve and show event target scope and other informations.
  * Localization support.
  * Zoom event tree using wheel.
* Command
  * `HOI4 Mod Utilities: Scan References` to automatically discover references of current script.

## [0.3.7] - 2020/07/25

### Fixed
* Add check before all usage of fsPath to make sure error message popup.
* An issue that D01 not treated as country scope.
* An issue that `dynamic_tags` is treated as a country in country tags files.
* An issue that world map still loading even preview page closed.

## [0.3.6] - 2020/07/17

### Changed
* Add telemetry to record usage and exceptions to provide better experience. It can be disabled with VSCode telemetry settings.

### Fixed
* Localization now can fallback to lang code when country code not present. For example, `en-us` will fallback to `en`.

## [0.3.5] - 2020/07/11

### Changed
* Update parser.
  * Strings without quote will be treated as string now.
  * Variables can be parsed now. The default value will be used.
* Focus tree preview will show warnings for invalid code.

### Fixed
* An issue that preview button shows incorrect type of preview.
* An issue that in some case focus tree preview shows nothing.

## [0.3.4] - 2020/06/23

### Added
* Focus tree
  * Focus can reference shared focuses now.

### Changed
* Focus tree
  * Change allow branches to condition, offset will also be calculated. This can be disabled by specifying feature flag `!useConditionInFocus`.

### Fixed
* Position of continuous focuses.
* Position of focus icons and titles in focus tree.
* An issue that preview will refresh twice.

## [0.3.3] - 2020/06/21

### Added
* Focus tree
  * Zoom focus tree using wheel.
  * Search item in focus tree by ID.

### Changed
* Change allow branches from checkboxes to multi-selection combobox.

### Fixed
* Update missing Chinese localization.

## [0.3.2] - 2020/06/06

### Added
* View mode `warnings` in world map.
* Warning filter in world map.

### Changed
* Align style of checkbox and combobox with VSCode.
* Click item in GFX file preview will navigate to name of sprite instead of type.
* Placeholder of search box in world map.

### Fixed
* Performance issue when opening world map preview.

## [0.3.1] - 2020/05/28

### Added
* World map preview
  * New view modes: strategic region and supply area.
  * New color sets: supply value.

### Changed
* Refine map loading and auto reload.
* Changed scale level to show edges and labels for different view modes.

### Fixed
* Fixed bug that can't copy file if parent folder not exist.
* Fixed bug that sometimes world map not properly reloaded.

## [0.3.0] - 2020/05/24

### Added
* Command
  * `HOI4 Mod Utilities: Preview World Map` to open world map preview window.
* World map preview
  * Possible view modes: province and state.
  * Copy (if not in mod) and open state file from world map.
  * Show warnings and informations about provinces and states.
  * Various of color sets.
  * Search province or state by ID.
  * Auto reload world map when related file updates.
  * Force reload world map from tool bar.

### Changed
* Update UI in preview page to match VSCode style.

### Fixed
* Fixed parsing rules of HOI4 file parser.

## [0.2.1] - 2020/05/02

### Added
* Reads `replace_path` of `.mod` file.
  * New setting `hoi4ModUtilities.modFile` to set working mod definition.
  * Read `replace_path` from working mod when loading files.
  * Show and change selected mod file from status bar.
* Focus tree preview
  * Show continuous focuses zone in focus tree preview.
* Add ability to reference more `.gfx` file in previewed file (focus tree, technology tree, gui, etc.).

### Changed
* Refine error message generated by HOI file parser.
* Added "Loading..." text to focus tree preview.
* Support more dds format so that they can be shown now.
* Changed icon of preview window.

### Fixed
* Fixed bug that sometimes icon in technology view not shown.
* Update strings in Chinese simplified localization.

## [0.2.0] - 2020/04/25

### Added
* Technology tree preview
  * Render technology tree as GUI defined in `interface\countrytechtreeview.gui` (icons, texts defined in this file will also be rendered).
  * Navigate to related technology tag by clicking technology or subtechnology.
  * Auto update preview when technology file changed.
  * Switch technology folder if a technology tree contains technology from different folder.
  * Can be dragged to scroll.
* GFX file preview
  * Support `corneredTileSpriteType` tags.

### Changed
* GFX file preview
  * Show image size on tooltip.
* Focus tree preview
  * Can be dragged to scroll.

### Fixed
* Fix 1 pixel offset of read `.dds` file.

## [0.1.1] - 2020/04/19

### Fixed
* Fix bug that the tokenizer will read `={` as one token.

## [0.1.0] - 2020/04/18

### Added
* Focus tree preview
  * Render focus tree as graph.
  * Navigate to `focus` tag in document by clicking a focus in graph.
  * Show/hide focus branches (available for focuses has `allow_branch` tag).
  * Auto update preview when document updates.
  * Preview focus tree file that contains `shared_focus` tree.
* GFX file preview
  * Preview all `spritetype` tags in `.gfx` files.
  * Filter sprites by name.
  * Navigate to `spritetype` tag in document by clicking a sprite in list.
* DDS preview
  * Supports RGB and RGBA format.
