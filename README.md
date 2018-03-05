**ArmorPaint / Manual**

# Intro

![](img/title.jpg)

*The following is an in-progress(!) quick start guide*

ArmorPaint is a stand-alone tool fully specialized in physically based texture painting of 3D models. Import desired geometry and start painting right away. A modern viewport provides instant visual feedback as you paint.

# Download

Runs on **Windows and Linux**.

- [Get ArmorPaint](http://armorpaint.org/download.html)

## Requirements

As of now ArmorPaint is known to work on Intel HD5100 graphics card. For 8K/16K texture painting, GTX 1060/6GB or better is recommended.

## Limitations

Only the absolute basics are working. There is no undo, masking or layers yet. As the time goes, these issues will get resolved.

# Get Started

<iframe width="560" height="315" src="https://www.youtube.com/embed/5YIvj3yIP00?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Controls

`Left mouse button` to paint. `Right mouse button` to rotate the mesh. `Mouse wheel` to zoom in and out.

# Assets

## Import Meshes

Drag and drop unwrapped `.obj`, `.fbx` or `.gltf` file into the viewport. This will replace the currently painted mesh. Importing `.blend` format is in progress but not yet supported. Use Blender to do the conversion in the meantime.

## Import Materials

Importing Cycles materials from `.blend` format is in progress but not yet supported. Assemble materials in the built-in node editor for now.

## Import Textures

Drag and drop `.jpg`, `.png`, `.tga` or `.hdr` images into the node editor. This will import the image and create a new Image node.

## Export Textures

Click `Project - Export Textures`. Format, resolution and channels to export can be configured in `Project - Properties`.

# Materials

Material nodes in ArmorPaint are based on Cycles nodes. When painting, brush applies a material onto the surface. To setup material, invoke node editor with `Project - Materials - Nodes`. Use toolbar at the top to add new nodes. Use `x`/`backspace` key do delete existing nodes.

# Painting

Configure brush parameters in `Project - Brushes`. `Left mouse button` to paint.

## Bake Ambient Occlusion

*Experimental:* Set `Brushes - Type` to `Bake AO` and click on the model in viewport to apply.

# UI

## Scaling

*Experimental:* It is possible to scale up the user interface by editing the `config.arm` file placed alongside ArmorPaint binary. Edit `window_scale` entry to `2.0` or higher. Once stable, this option will be exposed directly in ArmorPaint.

```
{
	...
    "window_scale": 2.0,
    ...
}
```