# LC_EZPalette
Raw files to make suit creation easier. **This is just raw files you'll be adding. This won't do anything in-game, so you'll want to use this with mods like MoreSuits to create more suits.**

Since the UVs for this model are scattered all over UV space, this makes simple things like doing a simple color palette swap very complicated. The files in this come to remedy that problem.

# Table of Contents
- [Pre-requisites](#pre-requisites)
- [How-to](#how-to)
  - [SuitPaletteEditor.psd](#suitpaletteeditorpsd)
  - [Player.blend](#playerblend)
  - [Abreviation Legend](#abreviation-legend)

# Pre-requisites
- Program that can edit `.psd` files (ex.: Photoshop or [Photopea](https://www.photopea.com/))
- For more complex suits, program that allows you to paint on 3D models (Substance Painter or Blender)
  - If you want to use my `Player.blend` file, you'll have to use blender

# How-to
## SuitPaletteEditor.psd

If you only want to do a color palette swap, you will only need to follow this section of the tutorial.

![image](https://github.com/RavingDead/LC_EZPalette/assets/154840527/b0cf4626-9b25-4a7d-9ec8-667900ba9706)

Everything you'll need is inside this file's layers.

1. Go to one of the folders you want to modify

![image](https://github.com/RavingDead/LC_EZPalette/assets/154840527/8f24c758-9d7d-44d9-a852-81870143b806)

2. Click on the layer (in image above, the white square)
3. Fill the layer with the desired color using the bucket tool
4. If you want more complex designs without going into a 3D texturing software (ex: have 2 different colors on the oxygen tanks above/below the metal line), you can use the magic wand to color pick what you want based on the default skin, which you can find inside of the *\_\_HELPERS\_\_* folder among other useful stuff. 

![image](https://github.com/RavingDead/LC_EZPalette/assets/154840527/805d1b1d-06a6-4f30-af79-4f5544a7cb6d)

5. If you don't want to use some or all of the layers in extras, disable them by clicking the little eye. Unlike other layers, theses ones will use whichever color is used by their parent components (HLM_Head for cheeks and OUT_Suit for LegEnds)

![image](https://github.com/RavingDead/LC_EZPalette/assets/154840527/74910e66-2bc0-4ee3-aa37-bfec0972eaf8)

6. Done! Export your file to a PNG, follow the instruction of your prefered suit mod to add new suits and get going!

## Player.blend
![image](https://github.com/RavingDead/LC_EZPalette/assets/154840527/bb327ae7-3b39-43c0-8aa8-c313fc353fc4)

Legend

1. (Yellow) 3D Viewport - Model
2. (Green) Toolbar
3. (Red) 2D Viewport - Texture
4. (Blue) Material Graph
5. (Purple) Details Panel

*Note: To hide the Toolbar in the active window, press N*

This is where we'll be adding stuff that is too complicated to do on photoshop. I won't be going into details as to how blender works, but here's the basic steps you might go through to edit your suit.

1. You'll want to drag up your **Material Graph** to plug in your suit texture if needed.

![image](https://github.com/RavingDead/LC_EZPalette/assets/154840527/5a28da56-af7f-434f-97f3-84b8b34f3b4a)

There's 2 ways to go about this:

You change the 'Texture' (1) using the little folder icon

The 'Reference' image (2) is the default skin. You can interpolate between the 2 by changing the value (3) on the lerp node. For example, 0.75 will mean the texture is 75% visible while the reference is 25% visible.

2. You can drag back down the **Material Graph** for now. You'll only need it again to if you want to change the reference image or change the lerp value.
3. Go into your **Details Panel** and click the tab with a small screwdriver/wrench icon ![image](https://github.com/RavingDead/LC_EZPalette/assets/154840527/93bf2b5c-70ea-4297-9d32-fc64dfd87c09)

![image](https://github.com/RavingDead/LC_EZPalette/assets/154840527/c5431e85-5960-4775-8afa-925494449b9d)

We just want to make sure we have the right image selected, otherwise we won't be painting the image we just added. In my case, I opened a file called *T_UV_Layout.png* so this is what we'll be selecting.

4. To see your image in the **2D Viewport**, click the image icon and select your image.

![image](https://github.com/RavingDead/LC_EZPalette/assets/154840527/31f2e129-5db5-4754-ae18-d1a716a8c14d)

5. If you plan on using stamp tool (copy images on your model), you'll want to do this step.

Go back to the **Details Panel** and select the *ref_img* material.

![image](https://github.com/RavingDead/LC_EZPalette/assets/154840527/d6643bcc-989c-4c02-b96d-de4584bc6285)

Like we did in step 1, go in your **Material Graph** again and open the desired image using the little folder icon.

***Note: Make sure you select the correct layer again after doing this!!! Once this step is done, repeat step 3.***

![image](https://github.com/RavingDead/LC_EZPalette/assets/154840527/4d4ed8fd-3e20-401d-804a-c0b5c7af843a)

6. Make sure you are in Texture Paint mode

![image](https://github.com/RavingDead/LC_EZPalette/assets/154840527/a156420c-37c3-45b0-95f5-02a1b078544e)

7. Now comes the fun part: Painting!

Tip: F = hotkey for brush size, shift+F = hotkey for brush strength

Paint your model as you wish, using either the **2D Viewport** or **3D Viewport**.

You can change the color using the color icon at the top or using the color palette in the **Toolbar**.

8. To mask certain parts of the mesh, switch to edit mode and go into your **Details Panel** in the green triangle icon tab ![image](https://github.com/RavingDead/LC_EZPalette/assets/154840527/6c6b1c80-3446-4a66-bdd6-699f10587b92)

![image](https://github.com/RavingDead/LC_EZPalette/assets/154840527/6dbceb23-11ae-43e4-ad52-f58be548382f)

This won't work unless you are in Edit mode. Don't forget to switch back to texture painting once you're done! (Tip: Press Tab to switch back and forth between texture paint and edit mode)

![image](https://github.com/RavingDead/LC_EZPalette/assets/154840527/bd1c7946-be88-4eb4-bcea-6859c671c005)

In the vertex groups (1) is a bunch of vertex groups you can use to quickly select geometry. Select one group and click the select or deselect button (2) to either add geometry to your selection or remove it. Do not touch assign or remove.

You can also press shift+left click on a face to add/remove it to the selection.

![image](https://github.com/RavingDead/LC_EZPalette/assets/154840527/ae040868-2fa3-42e3-9e7f-456be3e9b59a)

Going back to Texture Paint, if you click this cube icon, this will mask all the unselected faces.

9. If you want to use custom images, select the clone tool and left click where you want to apply it

![image](https://github.com/RavingDead/LC_EZPalette/assets/154840527/dc1a40fc-7e7d-4af8-b778-4c882699495c)

Note: The reference plane must be selected if you want to mask by geometry, otherwise it won't work.

To move where the cloning area will originate from, press shift + right click where needed (this will move the red-white circle).

10. Once you're done editing your image, you can go in your **2D Viewport**, go in the *Image* menu and click *save as*. (I recommend saving a new image to not lose your original!)
11. Done! Export your file to a PNG, follow the instruction of your prefered suit mod to add new suits and get going!

## Abreviation Legend
| **Abv** | **Definition**                 |
|---------|--------------------------------|
| BLT     | Belts                          |
| BTS     | Boots                          |
| GLV     | Gloves                         |
| HLM     | Helmet                         |
| OUT     | Outfit / Body                  |
| OXY     | Oxygen bottles / Back          |
| REF     | Reference plane (blender only) |
