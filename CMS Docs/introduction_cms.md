# Introduction
This guide provides an overview of the basic skills and actions required to efficiently use our CMS Back Office. It is designed for content managers responsible for managing projects, libraries, and categories within the CMS.
* **Projects**: Represent brand website content consisting of elements from libraries and models.
![Projects](cms_projects.png)
* **Libraries**: Collections of elements that can be shared across multiple projects. For example, a game in the **Game** library can be configured and launched in different projects.
![Libraries](cms_libraries_2.png)

* **Models**: Collections of elements specifically for a single brand.
![Models](cms_introduction_models.png)

## Frequently used actions
**Changing visibility**
All items in the CMS have three types of **visibility** related to the corresponding site environment: **D**: Development, **R**: Release, and **P**: Production (Prod).
To change an item’s visibility, click the appropriate button (→D, →R, or →P) at the top of the list.

![Visibility](cms_visibility.png)

**Copying items**
> Note that copying items is only possible for items created within the project.

To copy an item, you should follow these steps:
1. Select an item and click the **Copy to project** button.
![Copy items](cms_copying.png)
2. In the **Copy to projects** dialog, select your project and click the **Apply** button.
![Apply dialog](cms_copying_2.png)

**Removing items**
The process of removing items is similar to copying. To remove an item (from a project), you should follow these steps:
1. Select an item and click the **Remove** button.
2. In the **Remove selected X-item?** dialog, click the **Apply** button.

To add (or remove) an item to (from) a category:
1. Select the item and click the **Add selected X-item to categories** button.
2. In the **Bulk add selected X-item to categories** dialog, select the necessary categories, and click the **Apply** button.

To use an item from a library in a project select it and click the **Add to project** button specifying the desired project.
![Adding X-item](cms_adding_x_items.png)
![Adding promo](cms_adding_promo.png)

>Removing a library element is only possible if it is not currently added to any projects. If you need to remove an item that is already used in projects:
> 1. Select the item and click the **Remove from project** button.
> 2. In the "Removing X-item from projects" tab, select the relevant projects and click the **Remove** button.

## Content synchronization
If you create an item, share it across multiple projects, and then make changes to it, you should use the synchronization process to update all the projects where it is used.

To synchronize an item with project(s) for specific fields or the entire content, follow these steps:
1. Select the item and click the **Synchronize from library** button.
2. In the **Synchronize X-item library from library** dialog, select the item that needs to be synchronized with the project item. 
3. On the same tab, select the project(s) for which the library item should be synchronized with the project item.

![Synchronization](cms_synchronization.png)

## Adding the content
The **Alias** field is present in almost every record in the CMS. It serves as an identifier for each record. When filling in the alias, avoid using special characters, spaces, or numbers at the beginning.
> It is not recommended to have items with identical aliases within the same CMS model.

Some items on the brand website can be recognized by their alias, which helps simplify the search for an item in the CMS. For example, promotions or tournaments can be identified by their alias.

![Promotions on the brand website](cms_brand_alias.png)

![Promotions in CMS](cms_promotion_in_cms.png)

## Countries to implement
The **Countries to Implement** field regulates an item's availability for specific countries. It allows you to either permit or restrict access to an item based on the selected countries.

>Keep in mind that restricting an item for a certain country means that players from allowed countries can still view the item in all language versions available on the site. Therefore, all language versions (e.g., EN, PL, HU) should be carefully maintained. Note that language versions are not tied to specific countries for a given item.

Filling out the **Countries to implement** field
* **Allow specific countries**: If certain countries need to be allowed (with all other countries restricted), select the Allowed button and enter the country or list of countries. 
* **Restrict specific countries**: If certain countries need to be restricted (with all other countries allowed), select the **Restricted** button and enter the country or list of countries. 
* **Allow all countries**: To allow all countries, select the **Restricted** button and leave the field empty. 
* **Restrict all countries**: To restrict all countries, select the Allowed button and leave the field empty.

## Content deployment
The content manager can deploy content only to the development and release site environments, with some exceptions for projects that are under development.

**Content deployment via Jenkins**
Using Jenkins, you can deploy content to V2 platform projects. Jenkins consists of projects called Jobs, and each job begins with either **CD**, **CR** or **CP**:
* **CD**: Deploys content to the development environment.
* **CR**: Deploys content to the release environment.
* **CP**: Deploys content to the production environment.

To deploy content:
1. Find and select the necessary project **Job**. 
2. Click the **Schedule a build for...** button.

![Content deployment](cms_jenkins.png)

