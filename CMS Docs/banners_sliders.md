# Banners and Sliders
This section provides instructions for creating banners and sliders in the CMS. To begin, you need to create a category that serves as the placement location for banners and sliders. The frontend team uses this placement to position the banners or sliders at specific locations on the website.

**Creating a Category**

1. Open the CMS system and select the specific project in the **Projects Dashboard**.  
2. Go to the **Project** tab and open the **Banners & Sliders** model.  
3. Add a new category by clicking the **+Add new category** button.  

![Adding a new category](cms_banners.png)

4. In the **Add bannerCategory** dialog that opens, fill in the following fields:  
   ***Alias**: It is recommended to use a key value of the future banner and/or its location as an alias. Do not use spaces or special characters when creating the alias.  
   * **Name**: Enter the category name.  
   * **Screenshots**: Add a screenshot from a project where this banner is used.  
   * **Description**: Provide a description of where the category can be found in the project.
   ![Adding a banner category](cms_banner_category.png)

**Creating Banners & Sliders**

To add a new banner or slider:
1. Click the **+Add new** button.  
2. In the **Add banner** dialog that opens, fill in the following fields:
   - **Content type**: This dropdown has options such as *banner*, *slider*, and *SpecialPromo*. Select the required category for the current item.
   - **Countries to implement**: Add the required countries.
   - **Categories**: Enter the required previously created placement category.
   - **Platform**: Choose from the options: all, desktop, or mobile, to specify the devices for which the item will be available.
   - **Showing to users**: Use the checkboxes to select the user groups for which the item will be available: all users, logged users, or unlogged users.
   - **Terms and Conditions**: Select the applicable T&C from the dropdown list, which includes various terms added to the "Terms and Conditions" model.
   - **Title**: Enter the name of the current item.

![Adding a slider](cms_slider_item.png)

**Fields for Button Text**:  
   - **Logged user**: Enter the button text for logged users.  
   - **Unlogged user**: Enter the button text for unlogged users. The text for logged and unlogged users may be the same. When adding button text, follow the layout or project requirements.
   - **URL**:  
     - **Logged user**: Enter the alias value for the link. The required alias must be requested from the frontend team.  
     - **Unlogged user**: Enter the alias value for the link.
   - **Slide text**: Add the required number of slide text items. You can import text using the **Import slide text by XLSX** field.
   - **Images for banner**: Add images if required. Use the **Replace image** button to add different images for each language version. After adding an image for EN localization, switch to the required localization and upload the corresponding image by clicking the **Replace image** button.
   - **Video Desktop and Video Mobile**: Add videos if required.

![Adding a slider item](cms_slider_fields.png)

**Sorting Items within a Category**

If you have more than one item within a category, you can sort them accordingly to determine their order of appearance.