---
title: Optimizing Images for the Web
graded: 'n'
published: true
---

Images need to be saved appropriately for the Web. Details such as what image format (jpg, png, gif), image size, image quality, etc. all need to be considered.

## Before you Save

### Get prepped!

Before you can Save for Web in Photoshop, you need to get your image ready. Make sure the image is RGB and sized to be pixel-perfect. Resolution is irrelevant, we only truly care about the number of pixels!

### Save it already!

Choose `File > Save for Web` or the super-simple-and-totally-easy-to-remember shortcut `Command + Option + Shift + S` and switch the Original view to 2-Up or 4-Up so you can compare image format and compression options

[![]({{site.github.url}}/images/save4web01.jpg)]({{site.github.url}}/images/save4web01.jpg)

Select a Slice (one of the versions of your image) and apply a preset from the right side of the dialog box. Presets select a file format, compression algorithm, colors, etc. as a starting point for you to tweak and adjust.

Try adjusting the file format, compression quality, etc. and compare against other slices until you find the best overall compromise of image quality vs file size.

[![]({{site.github.url}}/images/save4web02.jpg)]({{site.github.url}}/images/save4web02.jpg)

Once you've found the imperfect balance between size and quality, you can actually click `Save`. The best part about Save for Web is that you can keep your source files (PSDs, etc.) in one folder, and save them all to your Images folder and Photoshop never forgets where you want to save to!

## Considerations

### Embed ICC Profile

"Embedding ICC profiles shows a "true" copy of the original colors, but only in profile-aware apps like Safari and FF 3.5. … [T]his shift won't apply to any CSS-set backgrounds or borders around the image. In a lot of cases, this doesn't matter, but when it matters it's a huge pain to work around. This is the main reason web designers might want to leave profiles out of images that need to match browser colors." (source: [Viget Inspire](http://www.viget.com/inspire/save-for-web-simply/))

Basically, don't apply `Embed ICC Profiles` unless it is a standalone photograph. Any site elements (buttons, backgrounds, icons, etc.) should be saved with the option unchecked.

### sRGB

The best practice is to create/edit your images for web graphics in sRGB from the get-go to avoid any nasty colour shifts if you create an image in another Colour Space, such as Adobe RGB (1998). The Adobe RGB (1998) Colour Space covers a larger amount of the colour spectrum than sRGB and is a common default for a lot of Photoshop users. To ensure you are working in the right Colour Space go to `Edit > Color Settings` and select the `Web/Internet` preset. Remember to switch it back for Print editing, etc.! Worst case, your images will be edited in Adobe RGB (1998), or some other Colour Space, and converted on-the-fly by the Web browser (as virtually all browsers do this) to sRGB, potentially creating an undesirable colour shift.

#### Mac vs PC

*Note: This only applies to Macs using OSX 10.5 and lower.* Gamma settings are different for Mac ( Pre-Snow Leopard 1.8) and PC (2.2). Essentially, this means that monitor colours are darker on a PC than a Mac, and therefore all your images will be darker on a PC than how you see it on your home Mac. You can view your image on a Mac as though it were a PC. Simply go to `View > Proof Setup` and select `Windows RGB`. You can toggle the preview on/off with `Command + Y`

### Optimization options

Not sure what all those setting mean? Adobe has a handy guide to help you out.

-   [JPEG optimization options](http://help.adobe.com/en_US/Photoshop/11.0/WS29D0201B-A3E2-4339-9747-8FB540762EE3.html)
-   [GIF optimization options](http://help.adobe.com/en_US/Photoshop/11.0/WSE07483CE-5D9F-4764-AA48-9DF708AD8479.html)
-   [PNG optimization options](http://help.adobe.com/en_US/Photoshop/11.0/WSEA01D274-9690-488f-8CF0-0133E171BD4A.html)
