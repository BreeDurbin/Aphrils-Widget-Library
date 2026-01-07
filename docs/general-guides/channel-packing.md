# Channel Packing in Krita

---

### Shape textures in Awl follow the following format:

**Red: Border**

**Green: Body**

**Blue : Opacity Mask**

---

In Krita you can easily pack a layered image into the appropriate R,G,B channels

Setup your image with the following layers for packing:
  - Border
  - Body
  - Opacity

**Warning** : Copy Red, Copy Green, Copy Blue filters are often used for channel packing in Krita,
but they can be a bit finicky, luckily Krita offers us a better way to pack our textures.

**For each layer:**

1. In the layers docker (Default Center-Right of your screen in Krita 5) 
  - Right-Click the layer you would like to assign to be packed into a channel.
  - Select Properties
  - In the active channels deselect the channels you do not want to pack from the layer.
  - E.g. For packing the Border layer into the red channel only red should be selected.
2. Repeat this for all layers you wish to pack. You can also pack multiple layers into the same channel.
3. Disable visibility on all layers you do not want to pack, ensure visibility on all layers you want to pack. (Eye icon for each layer)
4. Export your texture:
   - File → Export → File Type: Png → Save
   - When selecting compression and save file settings, uncheck "Store Alpha Channel" this will premultiply the alpha to our R,G, B channels and save us space
   - If you do not uncheck the "Store Alpha Channel" your image may have blocky-ness when you import it into ue. 
     This is because we do not use the Alpha channel and if the alpha isn't premultiplied in if the RGB Channels are spotless when you export they will come out
     jagged because the alpha hasn't cleaned them up.
