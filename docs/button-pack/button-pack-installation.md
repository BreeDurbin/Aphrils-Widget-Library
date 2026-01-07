# Installation Guide

---

## Basic Installation

1. Unzip the downloaded archive into your project’s plugin directory:  
   `Project/Plugins/`

   After extraction, you should have:  
   `Project/Plugins/AphrilsWidgetLibrary_Buttons`

2. Enable the plugin:
  - Either add it directly to your `.uproject` file, **or**
  - Enable it through the editor:  
    **Edit → Plugins → Enable `AphrilsWidgetLibrary_Buttons`**

3. Install **UiMaterialLab**:
  - Download the UiMaterialLab project from Fab
  - Copy the `Content/UiMaterialLab` folder into your project’s `Content` directory

4. Enable plugin content visibility:
  - Open the Content Drawer
  - Click the **gear icon** (top-right)
  - Enable **Show Plugin Content**

---

## Optional Verification Steps

1. In the Content Drawer, right-click and select:  
   **User Interface → Widget Blueprint**

2. Open the newly created Widget Blueprint

3. In the Palette, locate **Aphril’s Widget Library**  
   *(Defaults to the upper center-left area of the palette)*

4. You should see **five buttons** available

---

## Recommended Project Setup

1. In `Project/Content`, create the following folders:
  - `WidgetLibrary`
  - `WidgetLibrary/Buttons`

2. Use these folders for:
  - User-owned Material Instances
  - Widget Blueprints
  - Common UI styles

This keeps project-specific customization cleanly separated from plugin content.

---

### Adding Your Button to the Common Category (Optional)

To place your button in the **Common** category (Common UI default for user-created widgets):

1. Open your button widget
2. Top menu → **File → Reparent Blueprint**
3. Select `CommonButtonBase`

---

### Creating Your Own Palette Category (Advanced)

1. Use the `UAwlMaterialButton` class as a baseline for a new C++ class
2. Use your own class name to avoid One Definition Rule (ODR) violations
3. Override `GetPaletteCategory()` to return your desired category name
4. Reparent the widgets you want in the new category to this new class.

