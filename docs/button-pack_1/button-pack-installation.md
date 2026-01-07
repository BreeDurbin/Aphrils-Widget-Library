# Install guide:

1. Unzip the zip into your plugins folder(Project/Plugins/), you should get: Project/Plugins/AphrilsWidgetLibrary_Buttons
2. Add plugin to uproject directly or add using editor(Edit -> Plugins -> Enable AphrilsWidgetLibrary_Buttons)
3. Install UiMaterialLab. Download the project from fab, Copy the Content/UiMaterialLab folder into you Project/Content
4. Enable plugins view in your content drawer(content Drawer settings(Gear at top right of content drawer) -> Check Plugin Content)

# Additional Optional Steps
1. Verify installation: Right click content drawer -> User Interface -> Widget Blueprint
2. Open the new Widget Blueprint
3. Check for Aphril's Widget Library in your palette (Defaults to Upper center Left)
4. You should have 5 buttons there

# Recommended Additional setup:
1. In Project/Content Create a WidgetLibrary and then Buttons folder
2. This is for user owned Material Instances, Widget Blueprints, Common Ui Styles etc

# Your first Awl Button:
1. Duplicate a Material Instance from the Plugin -> Move it into WidgetLibrary/Buttons
2. Dial in the material instance to your preferred style
3. Duplicate a HexButton from the Plugin -> Move it into your WidgetLibrary/Buttons
4. Update your Duplicated button *Variable Defaults* (In event Graph)
- From Widget Bluepring Editor Click Event Graph in the top right
- Variables on the Left Side
- Appearance Category
- Button Image variable
- If a details panel doesnt pop up for the Button Image variable then
    - Top Bar -> Window -> Details Panel
- Now in the Details Panel of your Button Image variable
    - Default Value -> Button Image: Assign your configured Material Instance from the Content Drawer WidgetLibrary/Buttons
5. You should now have your newly themed button available in the Aphrils Widget Library Category in the Palette of your Widget Editor
- How to your button to Common Category (Common Ui Default for User Create WBPs):
- Open your Button, Top Bar -> File -> Reparent Blueprint -> CommonButtonBase
  6, Your own category:
- Use the UAwlMaterialButton Class as a baseline for a new class in your own cpp code
- Use your own class name to avoid One Definition Rule (ODR) violations from teh compiler
- Change the GetPaletteCategory() Funtion to return the Desired name of your Category
# Additional Notes:
This duplicate strategy for making your own buttons and themeing them as you like is nice as if gives you a solid default button setup which includes Animations, All Awl Defaults, and Instance Editable properties for your button
- This means: You can Edit styling, Button Image, Text Styling, Text etc per widget when you add the button within a UMG WBP such as a Menu Widget
- Change Defaults for your Button by editing the variable defaults in the Event Graph of your widget

