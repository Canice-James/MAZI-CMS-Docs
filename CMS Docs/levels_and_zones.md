# Levels and Zones
The **Level** model is used to add custom gamification elements.

The **Zones** model is used as an extension of the **Levels** model. It divides the levels into zones, providing a structured approach to gamification.

**Adding levels**
1. Go to the **Project Settings** > **Levels** model. 
2. In the Levels model, click the **Add new** button. 
3. Fill in all the necessary information to create a new level item:
   * **Level**: Select the required level from the dropdown that was added to NR1 by the backend team. 
   * **Level Images**: Add images if necessary. 
   * **Name**: Enter the name of the level and add translations for all language versions. 
   * **Text for Level**: Add the required number of text elements and fill them in, adding translations for all language versions. 
   * **Terms for Level**: Add any applicable T&C for the level. When adding T&C, use HTML tags if necessary.

**Adding Zones**
To create a zone, ensure that all necessary levels are already created.

The zone record should include the following fields:
* **Level From**: Select the level from which the current zone begins. 
* **Level To**: Select the level at which the current zone ends. 
* **Target Level**: Select the level from which users can view the next zone levels. 
* **Zone Images**: Add the required images. 
* **Name**: Enter the name of the zone. 
* **Text for Zone**: Add the required text and complete it. 
* **Description for Level**: Add a description of the zone.

Example of a filled **Zone**
![Adding zones](cms_zones.png)


