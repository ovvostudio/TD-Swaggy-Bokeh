# TD-Swaggy-Bokeh

> Physically accurate deep GLSL implementation of DoF in Touch Designer.
**Universal component TD088/TD099**.

 
 





In an effort to create a truely hi-quality set of post-processing tools for Touch Designer, I'm starting a serie of components that are real-time, simples but not simplistic and can rival their off-line counterparts in the standard post-processing/motion design software like Nuke, Fusion or Adobe After Effects to name a few.

So, this is the first of those components that accurately mimics the **Depth of Field**. 

This is a 1:1 GLSL implementation of an amazing work by [**Martin Upitis**](http://devlog-martinsh.blogspot.fr/2011/12/glsl-depth-of-field-with-bokeh-v24.html). The code is so clean that demanded really no effort to port it to Touch Designer.

To bring it into the world of Touch Designer, I decided to integrate it more deeply than I initially thought. That is, you don't even have to match the camera, it is done just by dragging your scene camera into the the corresponding component field.

But you can also use it to composite your 3d renders with a depth pass. I've always been a fan of [Frischluft Lenscare](http://www.frischluft.com/lenscare/) which is imho the best depth of field generator around.

One of the best features of Lenscare is to visualize the focus and the sharp zone. The same functionnality available in **Swaggy Bokeh** by toggling the 'Show Focus' switch. Red line is the focus, white - sharp zone. You can dial as much or as little of the bokeh swag as you wish whether you use 3d camera or bringing it from a 3d software package as pass.

One of the amazing feature, always thanks to Martin's work, is Autofocus. Basically, you're giving the screen coordinates in normalized format (as UV) and whatever depth is registered at this location would become your focus. Note that the coordinates goes from LEFT (0) to RIGHT (1) for U and from BOTTOM (0) to TOP (1) for V. Be careful though with moving objects, you depth in this location can jump wildly.

Everything else is self-explanatory. I only warped Martin's pixel shader in an interactive GUI that reacts and activates necessary parts when needed.

Bring on some swag! You have no excuses anymore.

Best
Shandor
