# Achievements in CMS
Achievements’ content should be provided in the CMS system.

1. To view current achievements, go to **Project Dashboard** and find your project.
2. On your project’s page, find the **Gamification** tab and click **Achievements**.

On the **Achievements** page, you can view all current project achievements. If you click an achievement name, its content will appear in the **Edit achievement** dialog.

![Achievements_tab](achievement_cms.png) 

To add a new achievement, click the **Add new** button. In the dialog, specify the achievement’s content and settings.

![Achievements_dialog](achiev_cms.png ':size=500') 

* **Categories**: Select a category to group achievements (if necessary). For example, casino weekly challenges.
  * **All**: Select this checkbox to add an achievement to all achievement categories.
* **Button alias**: Button alias for redirecting to the specific page. For example, for sports achievement, use specific sports alias (may be found in the URL on the Sports page), or for casino achievement, specific game alias (may be found in CMS > Game library tab).
* **Button guest alias**: Button alias for non-logged-in players iif there is a difference in the redirect behavior for unlogged-in and logged-in users.
* **Achievements**: Achievement ID + Name from NR1.
* **Provider**: Game provider.
* **Game**: Game of the selected game provider.
* **Countries to implement**: Required countries.
  * **Allowed** and **Restricted**: Buttons defining which countries are allowed or restricted.
  * Checkbox **All** for all countries.
* **Championships**: Sport championships.  
* **Is virtual sport event?**: Toggle determines whether this achievement features virtual sports.
* **Product images**: Images for this achievement.
* **Translatable fields**: All fields under languages must be translated to all localizations.
* **Name**: Name of an achievement. This content will appear on the player’s interface.
* **Button name**
* **Button guest name**: Button name if there is a difference in the redirecting behavior for unlogged-in and logged-in users.
* **Tooltip** and **Description**: Descriptive information for completing the specific achievement. For example, “To unlock this achievement, you should make 150 spins”. This content will appear on the player’s interface.
* **Achievement text**: Additional information for achievements.

An example of a casino weekly achievement:

![Achievements_dialog](example_casino.png ':size=500') 

