# glumo
WIP : toy text editor, with the aim of being built with as few libraries as possible in Rust. This will take a long time to make, but the time will pass anyways.  
Inspired by Sokol, embedded-display, vim and Godot.  
The objective of this text editor project is to have a very decoupled architecture, with the window handling software distinct from the text editor. That way, it could be possible to add things beyond a text editor to glumo, and that requires having a Tab object which would have the same API as a window in other libraries, granting access to drawing primitives, inputs and other things.  
It might be a good idea at some point to split glumo into multiple libaries. It might be necessary to change the name at that point, but we'll see then.  

## MVP
The first version of the editor will have the following features, in the order they are going to be added :
- x11 backend
- Variable window size
- Input processing
- Bitmap text and sprite rendering
- Triangle drawing and color rendering
- Simple text buffer editing with vim bindings
- Efficient file saving
- Use of swapfiles

## First order extensions
After that MVP is done, it should be expanded with the following features, still in chronological order :
- Editor tabs
- Editor split screen
- NerdTree-like interface for navigating files
- Mouse support
- Non-Vim edition mode

## TTF support
Absolutely needed features for efficient rendering and text scalability
- ttf file loader
- VkSurface/GLSurface support
- Vulkan/GL backend to render ttf files (extremely complex)
- Upgradd Text Buffer rendering

## Customization options
These features need to be added for more ricing options (which are the most important in a text editor anyway)
- Loading of a configuration file
- Ability to change font
- Ability to change editor colors
- Ability to add transparency

## IDE stuff
In order to make this editor more usable for code editing, a few things are needed, in order :
- Automatic downloading of configured LSP files
- Syntax highlighting tied to languages
- Diagnostics in editor
- Auto-complete like VSCode
- Access to a shell inside the interface

## Cross-platform
To make the editor cross-platform, a few things are needed. First, I will need a normalised UI system, which will be provided by these two features :
- Normalised Graphic tablet support
- Normalised Controller support
- Expand the UI system to encompass all of the Godot Engine UI elements
- Allow to use Godot UI config resources to change the look of the UI 
Afterwards, support should be rolled out for the following windowing systems :
- Wayland
- Whatever Windows uses
- Whatever MacOS uses

## Other useful addons for the text editor
- man support
- org files support
- pdf support (might be horrifyingly difficult)
- git support
- merge editor

## Final extensions
Once the rest is done, I'd like to expand this project with a few more windows and a few more functionality, so :
- Allow to create a text editor tab with potentially 0..* buffers and a basic svg editor in the other tab
- Add new tab : basic pixel by pixel drawing program
- Add new tab : 3D Triangle editor (likely a vulkan backend, likely...)
- Add new tab : 3D engine editor (an entirely different project, but I'm going to try to make that in parallel in order to have code that can be used not atrociously)

