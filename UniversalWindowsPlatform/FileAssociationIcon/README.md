# File association icon generator - Universal Windows Platform
There doesn't seems to be any offication gudielines for icons used for file associations. The closest thing we found is on [How to handle file activation] (https://msdn.microsoft.com/en-us/library/windows/apps/xaml/hh779669(v=win.10).aspx):

*We recommend that you include the proper icons with your project so that your logo looks great in all of these places. For a Windows Store app, include in your image folder 16/32/48/256 pixel versions for the small logo and icon sizes. For a Windows Phone Store app, include 63/129/336 pixel versions instead. Match the look of the app tile logo with the color plate baked in and have the logo extend to the edge without padding it. Test your icons on white backgrounds.*

Also there doesn't seems be be any good templates to start with. So we created some templates that are extremly similar to the ones used in Office :-).


## How to use it

Open the SVG-files in Inkscape and replace the existing logo with your apps logo. Files with 16, 32, 48 and 256 pixels are used on Windows Desktop. Size 63, 129 and 339 is used on Windows Phone.

Open [FileAssociationIconGenerator.ibp] (Source/FileAssociationIconGenerator.ibp) in Inkscape batch. This is a basic script file and you shouldn't need to change anything.

Press Start batch converter in Inkscape batch and wait a few seconds. Put the generated bitmaps in the assets folder of you project and you are done.


## References
* [How to handle file activation] (https://msdn.microsoft.com/en-us/library/windows/apps/xaml/hh779669(v=win.10).aspx)

