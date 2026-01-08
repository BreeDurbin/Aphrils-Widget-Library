# Recommended Workflow

This workflow shows how to create custom-styled buttons using **Aphril’s Widget Library** while preserving built-in animations and default behavior.

---

## 1. Prepare a Material Instance

1. Duplicate a **Material Instance** from the plugin.
2. Move it into:

```
WidgetLibrary/Buttons
```

3. Adjust the material instance to match your preferred visual style.

---

## 2. Duplicate a Button Widget

1. Duplicate a **HexButton** (or any other button type) from the plugin.
2. Move the duplicated widget into:

```
WidgetLibrary/Buttons
```

---

## 3. Update Variable Default Values

1. Open your duplicated button in the **Widget Blueprint Editor**.
2. Switch to the **Event Graph** tab.
3. In the **Variables** panel (left side), expand the **Appearance** category.
4. Select the **Button Image** variable.

> **Tip:** If the **Details** panel is not visible, enable it via
> **Window → Details**

5. In the **Details** panel for `Button Image`:

    * Set **Default Value → Button Image**
    * Assign your configured **Material Instance** from
      `WidgetLibrary/Buttons`

6. Verify that your button now displays the new style.

Your newly themed button will appear under **Aphril’s Widget Library** in the **Widget Palette**.

---

## Optional: Add Your Button to the Common UI Category

By default, user-created widgets appear under **Common UI**. To place your button there:

1. Open your button widget.
2. From the top menu, select **File → Reparent Blueprint**
3. Choose `CommonButtonBase`

---

## Advanced: Create Your Own Palette Category

If you want full control over how widgets are grouped in the Widget Palette:

1. Use `UAwlMaterialButton` as the base for a new C++ class.
2. Give the class a unique name to avoid **One Definition Rule (ODR)** conflicts.
3. Override `GetPaletteCategory()` to return your desired category name.
4. Reparent any widgets you want in this category to your new class.

---

## Additional Notes

This duplication-based workflow provides a strong default setup that includes:

* Built-in animations
* All AWL default behavior
* Instance-editable and spawn-exposed properties

This allows you to:

* Customize styling, button images, text styling, and text per widget
* Adjust defaults by editing variable default values
* Modify buttons directly inside UMG Widget Blueprints (e.g., menus and UI screens)

---

### Why this works well

* You retain all plugin functionality without modifying plugin assets
* Updates to the plugin won’t overwrite your custom buttons
* Styling and behavior remain centralized and reusable
