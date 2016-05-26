# Icons and tiles generator - Universal Windows Platform
The ambition is to follow [Microsofts guidelines for icons and tiles] (https://msdn.microsoft.com/en-us/windows/uwp/controls-and-patterns/tiles-and-notifications-app-assets). Microsoft already has a solution for [Photoshop users] (https://blogs.msdn.microsoft.com/madenwal/2015/11/24/generating-your-tileicon-image-assets-for-windows-10-uwp-using-photoshop-actions/) and this is basically a rip off of that :). 


## How to use it

Open the seven SVG-files in Inkscape and replace the existing logo with your apps logo. Each SVG-file has guides rules to show the margins from the guidelines. In most cases you should keep your logo in the center four boxes. If some part of your logo is outside these boxes, try to keep it inside the blue rectangles. 

If you are using a monochrome icon you can keep your logo black. This is changed to white when the actual bitmaps are generated.
The seven SVG-files are used like this:

*	**Logo-AppList** - Used for icons for the start menu/app list.
*	**Logo-NoMargins** - Used for icons for the task bar. By default the icons are "unplated". Read more about this below.
*	**Logo-TileLargeMedium** - Used for icons for medium and large tiles.
*	**Logo-TileSmall** - Used for icons for small tiles.
*	**Logo-TileWide** - Used for icons for wide tiles.
*	**SplashScreen** - Used for splash screen.
*	**StoreLogo** - Used for icons in the Windows Store.


Open `IconAndTileGenerator.ibp` in Inkscape batch. This is a basic script file and if you are lucky you don’t need to change anything. But there are a few things to be aware of:

* The script by default replaces black with white. If you don’t want this remove lines like this: `Replace fill:#000000;fill-opacity:1; fill:#FFFFFF;fill-opacity:1;`
* The script by default makes the guides transparent (the blue rectangles). This is done by making them transparent. If you have problems with this remove lines like this: `Replace fill:#1ba1e2;fill-opacity:1 fill:#FFFFFF;fill-opacity:0`
* The script generates some files with the suffix altform-unplated by default. Read more about plated and unplated icons in the [guide lines] (https://msdn.microsoft.com/en-us/windows/uwp/controls-and-patterns/tiles-and-notifications-app-assets#Target-based_assets).
* In many cases **Logo-TileWide** and **SplashScreen** will have the same image but with a different scaling. If that’s the case, you can remove one of these file and change in `IconAndTileGenerator.ibp` to use the file you kept. 

Press Start batch converter in Inkscape batch and wait a few seconds. Put the generated bitmaps in the assets folder of you project and you’re done. You may need to open `Package.appxmanifest` to ensure that all images are used.


## References
* [Guidelines for tile and icon assets] (https://msdn.microsoft.com/en-us/windows/uwp/controls-and-patterns/tiles-and-notifications-app-assets)
* [Generating your tile/icon image assets for Windows 10 UWP using Photoshop Actions] (https://blogs.msdn.microsoft.com/madenwal/2015/11/24/generating-your-tileicon-image-assets-for-windows-10-uwp-using-photoshop-actions/)

