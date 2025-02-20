---
title: Add a tag library
description: Learn how to create a tag library in Data Collection. This lesson is part of the Implement the Experience Cloud in Mobile iOS Objective-C Applications tutorial.
exl-id: b073937a-c4af-4753-8ff7-dedda9c6769e
---
# Add a library

In this lesson, you will create a library for your new tag property. A library packages together all of the desired tags settings and generates the specific implementation instructions required to install the library in your mobile app.

>[!NOTE]
>
>Adobe Experience Platform Launch is being integrated into Adobe Experience Platform as a suite of data collection technologies. Several terminology changes have rolled out in the interface which you should be aware of while using this content:
>
> * Platform Launch (Client Side) is now **[[!DNL tags]](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html)** 
> * Platform Launch Server Side is now **[[!DNL event forwarding]](https://experienceleague.adobe.com/docs/experience-platform/tags/event-forwarding/overview.html)** 
> * Edge configurations  are now **[[!DNL datastreams]](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/datastreams.html)**

## Learning Objectives

At the end of this lesson, you will be able to:

* Create a library
* Add changes to a library
* Build a library

## Save Your Changes to a Library

After configuring your extensions, you need to package them into a library that you can deploy in your app so you can use your solutions.

**To add and build a library**

1. Go to the **[!UICONTROL Publishing]** tab

1. Click **[!UICONTROL Add New Library]**

   ![Add New Library](images/mobile-launch-addNewLibrary.png)

1. Name the Library `Initial Setup`

1. Select **[!UICONTROL Environment > Development]**

1. Click **[!UICONTROL Add All Changed Resources]**

   ![Add All Changed Resources](images/mobile-launch-addAllChangedResources.png)

1. Note that after clicking **[!UICONTROL Add All Changed Resources]** tags summarizes the changes you just made when adding extensions.

1. Click **[!UICONTROL Save & Build for Development]**

   ![Save and Build for Development](images/mobile-launch-saveAndBuild.png)

1. After a few moments, the status dot will turn green indicating the library built successfully.

    ![Library Built](images/mobile-launch-libraryBuilt.png)

[Next "Install the tag property and the SDK" >](install-the-mobile-sdk.md)
