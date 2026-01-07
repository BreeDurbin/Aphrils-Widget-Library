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

### If you cannot see your plugin in the content drawer after enabling plugin visibility:

Your plugin is likely installed as an engine plugin. Enabling engine content will let 
you view the plugin from the content drawer. Content Drawer Settings → Check "Engine Content"
You should now see your plugin in the engine folder in your content drawer, but this isn't ideal
because there are a large number of engine plugins. 

### Recommended: Install the plugin in your project

This will give you easier access to your plugin based content.

To get your plugin from the engine installation:

1. In editor select Edit → Plugins 
2. Search "Aphrils Widget Library - Buttons"
3. Select package
4. Pick an output folder that is easy to get to.
5. Navigate to the packaged plugin output
6. Depending on how the output was packaged:
   - If it is packaged in a host project copy the plugin("AphrilsWidgetLibraryButtons" folder) from the plugins directory.
   - If it is just the plugin copy the plugin "AphrilsWidgetLibraryButtons" folder
   - You can know you have the right folder copied because inside it there will be a "AphrilsWidgetLibraryButtons.uplugin" file inside it.
7. Now that we have the plugin, we can install it in your project but copying the plugin folder into your "ProjectFolder/Plugins"
8. Build your project to ensure the plugin is built.
9. Enable the plugin in Edit → Plugins → Aphril's Widget Library - Buttons
10. You should now be able to see the plugin in your Content Drawer in the "Plugins" folder.

---

## Recommended: Project Setup

1. In `Project/Content`, create the following folders:
   - `WidgetLibrary`
   - `WidgetLibrary/Buttons`

2. Use these folders for:
   - User-owned Material Instances
   - Widget Blueprints
   - Common UI styles

This keeps project-specific customization cleanly separated from plugin content.

---

## Optional: Verification Steps

1. In the Content Drawer, right-click and select:  
   **User Interface → Widget Blueprint**

2. Open the newly created Widget Blueprint

3. In the Palette, locate **Aphril’s Widget Library**  
   *(Defaults to the upper center-left area of the palette)*

4. You should see **five buttons** available

5. Try out your new buttons.

6. You can also see all buttons at once though Plugins → "Aphril's Widget Library - Buttons" → Showcase
   - Right click WBP_Showcase → Preview

---

Now that you are all setup Installation-Wise our [Workflow Guide](https://breedurbin.github.io/Aphrils-Widget-Library/general-guides/workflow/) can help you get to know your new content.

If you are having technical issues with the installation you can create a [Support Ticket](https://github.com/BreeDurbin/Aphrils-Widget-Library/issues) for assistance.
