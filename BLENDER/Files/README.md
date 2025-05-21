# 📂 Blender Assets — Files Folder

This subfolder includes all `.blend` project files, along with associated assets such as textures, renders, and animations. These are used in conjunction with the main Blender simulations found in the parent folder.

---

## 📁 Folder Contents

| File Type       | Description |
|------------------|-------------|
| `.blend`         | Blender project files (scenes, animation setups) |
| `.jpg/.png`      | Image textures used in rendering |
| `.mp4/.webm`     | Video exports of the simulation results |
| `.obj/.stl/.dae` | Imported/exported 3D models used in the scene |

---

## 🔧 Usage Instructions

1. Open `.blend` files in [Blender](https://www.blender.org/download/).
2. Check the **Shader Editor** or **UV/Image Editor** tab for associated textures.
3. To render:  
   - Go to **Render > Render Image/Animation**  
   - Make sure all linked files (images, textures) are loaded correctly.

---

## 💡 Tips

- If materials appear pink in Blender, the texture paths may be broken. Re-link via **File > External Data > Find Missing Files**.
- Exported renders can be reused in presentation decks or simulation demos.

---

## 🔗 Related Modules

- Refer to the main [BLENDER README](../README.md) for simulation workflow.
- Some assets may be derived from [CAD](../../CAD) models.

---
