# mw-extension-DisplayTitle
Mediawiki Extension fork of DisplayTitle

## About
See [Mediawiki Extension:DisplayTitle](https://www.mediawiki.org/wiki/Extension:Display_Title)

## Installation

## Configuration

## Usage

## Credits

## Version History and Release Notes
### DisplayTitle v1.37.0
Fork from Display Title version 3.1.  (Our number starts with the version that the extension was last tested for, which is 1.37.x for this extension).

* Removed the changing of the display title for redirects.  If a redirect (old article) has DISPLAYTITLE set, that will be displayed.  But the extension will no longer display to the redirected title.  The reason for this change is that this version of the extension was written for a project where a whole family of articles all redirect to a main article, but we want to be able to display different DISPLAYTITLE's for each redirected article.  Running and ran both redirect to run, but we are working with Hebrew where we want to display vowels, but not have vowels in the official article title.


