**Please take into consideration the guidelines on the wiki. There is a specific section about icons on this page:**  
https://sky-children-of-the-light.fandom.com/wiki/Help:Wiki_Guidelines_for_Editing



# Inkscape

## Download

https://inkscape.org/release

## Palette

For quick access to the palette, go to `Edit > Preferences > System` and open the folder for `User palettes`.

Add the [skygame.gpl](https://github.com/Silverfeelin/SkyGame-Icons/blob/main/gimp/palettes/skygame.gpl) file to this folder.

You should now see a new palette with the name "Sky icons". If you don't see it, restart Inkscape.

![](https://i.imgur.com/02O1s5w.png)

The colors in the palette are used as follows:

- **Beige**: Main color of the icons.
- **Pink**: Accent color of the icons.
- **Stroke**: Color of the stroke around the icons.
- **Extra** (1): Tertiary color used in some icons.
- **Extra** (2): Quaternary color used in some icons.
- **SpellBeige**: Main color of spell icons.
- **SpellPink**: Accent color of spell icons.

## Document

> The easiest way to get the right document settings is to open an existing image. For example, by using the [blank.png](https://github.com/Silverfeelin/SkyGame-Icons/blob/main/templates/blank.png) template or by opening your [Reference image](#reference-image) directly.

To modify the document properties, go to `File > Document Properties`.

Icons should be created in a document with the following settings:

- **Format**: px (pixels)
- **Width**: 300
- **Height**: 300
- **Scale**: 1
- **Display units**: px (pixels)

![](https://i.imgur.com/fwXGtqo.png)

## Reference image

To create a good vector icon, a high quality reference image is recommended. The better the reference image, the less work you have to do to clean up edges and details.

> It is important for a later step that your reference image matches the canvas size of 300x300px. If you don't do this it will be more difficult to apply the correct stroke later on.

> If your image is low resolution, it's generally better to trace it at that resolution and upscale the vector image later. If you upscale the reference image, the trace might have a lot of jagged edges that are hard to clean up.

Example image (in-game screenshot, fitted into a 300x300px canvas with a dark background):  
![](https://i.imgur.com/nTdwSuX.png)

## Trace Bitmap

The Trace Bitmap feature can be used to automatically convert the reference image into a vector image. You can find this feature in `Path > Trace Bitmap`.

For light icons on dark backgrounds, enable `Invert image`. The preview will show the result of the trace in black.

You can play around with the settings until you get a good result. In general you want to change the `Theshold` as low as possible while still having visible separation between the different parts of the image.

In the below examples you can see how changing the threshold affects the result. The first result is not viable. The second and third are both viable, though the second will likely require less cleanup.

![](https://i.imgur.com/V3EJZtk.png)
![](https://i.imgur.com/0cRRDHW.png)
![](https://i.imgur.com/r5FVpyS.png)

At any point you can press `Apply` to create the vector image. If you're not happy with the result, you can delete the layer and try again. Click on the vector and press Delete on your keyboard, or use the layers menu.  
You can view your layers in `Layer > Layers and Objects...`.

Changing the name of a layer can be done by double-clicking on the name in the layers menu. This is useful to keep track of your layers.

Sometimes it's easier to trace multiple times for different parts of the image. In this example, both the beige and pink part of the icon are traced in one step. We'll separate the parts of the vector in a later step to color them differently.

![](https://i.imgur.com/54d5uAh.png)

## Splitting the vector

> This step is not always necessary as many icons only use one color.

Now that you have a decent vector image, it's time to split it into separate parts. 

You can change the color of the icon at this point to make it easier to see the details. Select the path and then click on a color from the palette at the bottom of the screen.

To split separate parts of the vector, you can use `Path > Break Apart`. Because this vector has two distinct parts, you'll now have two separate paths. At this point we can apply the correct colors to the two parts.

![](https://i.imgur.com/J8ujD0f.png)

> Changing the Alpha  value and color of the path will make it easier to compare the vector to the reference image. You can manually change the colors in the `Object > Fill and Stroke` menu. Just make sure to change the Alpha and color back before saving the icon.

## Cleaning up the vector

> Keep in mind that the vector does not have to be **perfect**. A good approximation is usually more than enough for a good icon.

If you're not happy with the result of the trace, you can clean up the vector by hand by changing the nodes of the path. Select the path and press `N` to use the node tool. You can also press this icon in the toolbar:

![](https://i.imgur.com/u6FdfC4.png)

You will now see all the nodes of the path, represented by small squares. To modify a node, select it by clicking on it. There are now several options available:

* Drag the node to move it around.
* Press Delete on your keyboard to delete the node.
* Ctrl + Alt + Click between two nodes to add a new node.
* Ctrl + Click on a node to change the curve type of the node.
* Drag the handles of a node to change the curve.

Example before and after cleaning up the back side of the basket:

![](https://i.imgur.com/0uKnycB.png)
![](https://i.imgur.com/XviPla3.png)

## Adding a stroke

For most icons, a single stroke is added around the entire icon. Here's the easiest wayt to apply the stroke:

* Select **all** the paths (hold `Ctrl` of `Shift` while clicking on the paths in the layer menu).
* Duplicate the paths (`Ctrl + D` or `Right click > Duplicate`).
* Combine the duplicated paths together (`Ctrl + Shift + Plus` or `Path > Combine`)
* Move the new 'stroke layer' to the back of the other layers.

![](https://i.imgur.com/HJeTbMc.png)

* Change the **Stroke** color of the stroke layer to the stroke color from the palette.
  * Hold `Shift` while clicking on the color in the palette to change the stroke color.
  * You can verify the stroke color in `Object > Fill and Stroke > Stroke`.
* Select both the stroke layer and the reference image layer (Ctrl click on the layers)
* Go to `Object > Fill and Stroke > Stroke style` and apply these settings:
  * Width: `12.3px`
  * Blur: `11.4%` (at the very bottom of the menu).
  * If your stroke looks completely different from the below example, you likely did not select both the stroke and reference layer, or the reference layer is not 300x300px. You can either try again or manually change the blur percentage.

![](https://i.imgur.com/D0n4ErV.png)

## Scaling the icon

* Select all the path layers in the layers menu
* Press `S` to use the selector tool.
* Press `Ctrl + Shift + A` or `Object > Align and Distribute` to open the align menu.
* Align the icon by pressing the align center buttons after making sure `Move/align selection as group` is enabled.

![](https://i.imgur.com/dkZiDIk.png)

* Hold `Ctrl` and `Shift` while dragging the corner of the icon to scale it to the desired size. The wiki recommends leaving roughly 25-50 pixels of space around the icon. Use the guide lines as an indicator if needed.

![](https://i.imgur.com/HbiqKVy.png)

## Saving the icon

> Before saving the icon, make sure you remove or hide the reference layer from the layers menu.

When saving the icon, it is highly recommended to always keep a copy of the icon in the Inkscape SVG format. This makes it easy to edit the icon in the future.

* Press `Ctrl + S` or go to `File > Save As...` to save the icon SVG file.
* Press `Ctrl + Shift + E` or go to `File > Export PNG Image...` to export the icon as a PNG file.
  * Make sure the settings are 300x300px with a DPI of 96.

That's it! You now have an icon ready to be used on the wiki.

![](https://i.imgur.com/V3ZB6kg.png)