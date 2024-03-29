# mw--DisplayTitle
The Display Title extension allows a page's display title to be used as the default link text in links to the page - both links from other pages as well as self-links on the page. Display Title also uses the display title of a page as part of the title of its talk page. It optionally displays the original page title as a subtitle on the page. And, it provides a parser function to query a page's display title.

This extension builds on functionality in MediaWiki core that supports setting a page's display title using the DISPLAYTITLE magic word. Placing {{DISPLAYTITLE:My Display Title}} on a page stores the value of the display title (My Display Title in this case) in the displaytitle page property of the MediaWiki page_props table and, if configured appropriately, displays that value on the page as the title in the title bar. The Display Title extension queries the displaytitle value in the page_props table to provide its features. 

Url: https://www.mediawiki.org/wiki/Extension:Display_Title

There are no changes from the official DisplayTitle 3.2, because our changes were incorporated into the most recent version.  
## Installation
- Download and place the file(s) in a directory called DisplayTitle in your extensions/ folder.
- Add the following code at the bottom of your LocalSettings.php:

    wfLoadExtension( 'DisplayTitle' );

- Configure as required
- Yes Done – Navigate to Special:Version on your wiki to verify that the extension is successfully installed.

## Configuration

Configuration flag 	Default value 	Description
- $wgDisplayTitleHideSubtitle -	false - If false, display the page's original title as a subtitle below the title bar.
- $wgDisplayTitleExcludes[] - An array of names of pages that should not have their page names replaced with their display title in links to the page. 
- wgDisplayTitleFollowRedirects - true - 

In order for DisplayTitles to function correctly, the following configurations need to be set.

    $wgAllowDisplayTitle = true; // defaults to true
    $wgRestrictDisplayTitle = false; // defaults to true
    
There are also some installation configurations you need to set.  See the DisplayTitle offical documentation for details.

## Usage
    {{DISPLAYTITLE:...}}

    {{#getdisplaytitle:Book:42}}
    {{#getdisplaytitle:{{FULLPAGENAME}}}}
    
    mw.ext.displaytitle.get()
    mw.ext.displaytitle.set()
    
    {{#invoke:DisplayTitle|set|My Display Title}}
    {{#invoke:DisplayTitle|get|My Page}} 
    
## Version History

### Version 3.2
- Added Hebrew translation
- Added option wgDisplayTitleFollowRedirects 

### Version 3.1
- Fix incompatibility with the Cite extension

### Version 3.0
- Compatibility dropped with MW 1.34 and lower
- Updates due to code deprecations in MediaWiki
- Several fixes to anchor/fragment behavior

### Version 2.0
- Compatibility dropped with MW 1.28 and lower

### Version 1.0 
- Initial release.
