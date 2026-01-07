# Recommended Workflow

---

1. Duplicate a **Material Instance** from the plugin
- Move it into `WidgetLibrary/Buttons`

2. Adjust the material instance to your preferred style

3. Duplicate a **HexButton** from the plugin
- Move it into `WidgetLibrary/Buttons`

4. Update your duplicated button’s **Variable Defaults**:
- Open the widget in the Widget Blueprint Editor
- Click **Event Graph** (top-right)
- Locate the **Variables** panel on the left
- Expand the **Appearance** category
- Select the **Button Image** variable

If the Details panel does not appear:
- Top menu → **Window → Details**

In the **Details** panel for `Button Image`:
- Set **Default Value → Button Image**
- Assign your configured Material Instance from  
  `WidgetLibrary/Buttons`

5. Your newly themed button should now appear in the  
   **Aphril’s Widget Library** category in the Widget Palette

---

## Additional Notes

This duplication-based workflow provides a strong default setup that includes:
- Built-in animations
- All AWL default behavior
- Instance-editable properties

This allows you to:
- Edit styling, button images, text styling, and text per widget
- Adjust defaults by editing variable default values in the Event Graph
- Customize buttons directly inside UMG Widget Blueprints (e.g., menus)

