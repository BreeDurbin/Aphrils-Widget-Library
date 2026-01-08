# Recommended Workflow

---

```mermaid

flowchart TD
%% Core workflow steps (blue)
    A[Start] --> B[Duplicate Material Instance from plugin]
    B --> C[Move Material Instance → WidgetLibrary/Buttons]
C --> D[Edit Material Instance to preferred style]
D --> E[Duplicate HexButton (or desired button) from plugin]
E --> F[Move Button → WidgetLibrary/Buttons]
F --> G[Open Button in Widget Blueprint Editor]
G --> H[Event Graph → Variables Panel → Appearance → Button Image]
H --> I[Details Panel: assign Default Value → configured Material Instance]
I --> J[Verify button appears in Aphril's Widget Library]

%% Optional steps (green)
J --> K{Optional: Add to Common UI?}
K -- Yes --> L[File → Reparent Blueprint → CommonButtonBase]
K -- No --> M[Skip]

%% Advanced steps (orange)
L --> N{Advanced: Create Custom Palette Category?}
M --> N
N -- Yes --> O[Create new C++ class from UAwlMaterialButton]
O --> P[Override GetPaletteCategory()]
P --> Q[Reparent widgets → new class]
N -- No --> R[End]

Q --> R
M --> R

%% Coloring nodes (v11-compatible)
style A fill:#cce5ff
style B fill:#cce5ff
style C fill:#cce5ff
style D fill:#cce5ff
style E fill:#cce5ff
style F fill:#cce5ff
style G fill:#cce5ff
style H fill:#cce5ff
style I fill:#cce5ff
style J fill:#cce5ff

style K fill:#d4edda
style L fill:#d4edda
style M fill:#d4edda

style N fill:#ffe5b4
style O fill:#ffe5b4
style P fill:#ffe5b4
style Q fill:#ffe5b4



```


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

### Adding Your Button to the Common UI Category (Optional)

To place your button in the **Common UI** category (Common UI default for user-created widgets):

1. Open your button widget
2. Top menu → **File → Reparent Blueprint**
3. Select `CommonButtonBase`

---

### Creating Your Own Palette Category (Advanced)

1. Use the `UAwlMaterialButton` class as a baseline for a new C++ class
2. Use your own class name to avoid One Definition Rule (ODR) violations
3. Override `GetPaletteCategory()` to return your desired category name
4. Reparent the widgets you want in the new category to this new class.


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


