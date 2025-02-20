---
title: Journey Optimizer Create your email message
description: Journey Optimizer Create your email message
kt: 5342
audience: developer
doc-type: tutorial
activity: develop
exl-id: 2b7333c3-5b6a-41c5-a7a7-b048d1579ddd
---
# 7.2 Create your email message

In this exercise, you'll configure the journey that needs to be triggered when someone creates an account on the demo website.

Login to Adobe Journey Optimizer by going to [Adobe Experience Cloud](https://experience.adobe.com). Click **Journey Optimizer**.

![ACOP](./images/acophome.png)

You'll be redirected to the **Home**  view in Journey Optimizer. First, make sure you're using the correct sandbox. The sandbox to use is called `--aepSandboxId--`. To change from one sandbox to another, click on **PRODUCTION Prod (VA7)** and select the sandbox from the list. In this example, the sandbox is named **AEP Enablement FY22**. You'll then be in the **Home** view of your sandbox `--aepSandboxId--`.

![ACOP](./images/acoptriglp.png)

In the left menu, click **Messages**. 

On the Messages screen, you’ll see a view similar to this. Click **Create Message**.

![Journey Optimizer](./images/msg1.png)

Give your Message a title following this naming convention `--demoProfileLdap-- - Registration Email` and select the **Email Preset** and enable the **Email** channel. Click on the **Create** button to create your Registration Email message.

![Journey Optimizer](./images/msg2.png)

The next screen is the message dashboard, from there you will be able to see the email thumbnail when the content will be provided.

![Journey Optimizer](./images/msg3.png)

On the right-hand side are the Email properties:

- **From email**: the email address from whom the recipient will receive email message. Note that this value is specified by the **preset** given in the previous step and is read-only.
- **From name**: the sender name  from whom the recipient will receive email message. Note that this value is specified by the **preset** given in the previous step and is read-only.
- **Subject line**: the mandatory subject of the message which will be edited in the next step. 
- **Body**: a button brings you to the Email Designer to create and edit the email content.
- **Optional features**: these two checkboxes allow to disable the tracking of the email's opens and email's clicks and therefore, prevent the message from measuring metrics like open rate, click-through rate,...

First, make sure that the 2 checkboxes under **Optional features** are checked. If not, please **make sure they are both activated**. 

![Journey Optimizer](./images/msg4.png)

Click the **Subject line** text field.

![Journey Optimizer](./images/msg5.png)

In the text area start writing **Hi**

![Journey Optimizer](./images/msg6.png)

The subject line is not done yet. Next you need to bring in the personalization token for the field **First name** which is stored under `profile.person.name.firstName`. In the left menu, scroll down to find the **Person** element and click on the arrow to go a level deeper.

![Journey Optimizer](./images/msg7.png)

Now find the **Full name** element and click on the arrow to go a level deeper.

![Journey Optimizer](./images/msg8.png)

Finally, find the **First name** field and click on the **+** sign next to it. You'll then see the personalization token appear in the text field.

![Journey Optimizer](./images/msg9.png)

Next, add the text **, thank you for signing up!**. Click **Save**.

![Journey Optimizer](./images/msg10.png)

You'll then be back here. Click **Email Designer** to create the email's content. 

![Journey Optimizer](./images/msg11.png)

In the next screen you will be prompted with 3 different methods to provide the email's content:

- **Design from scratch**: Start with a blank canvas and use the WYSIWYG-editor to drag and drop structure and content components to visually build up the email's content.
- **Code your own**: Create your own email template by coding it using HTML
- **Import HTML**: Import an existing HTML template, which you'll be able to edit.

Click **Design from scratch**.

![Journey Optimizer](./images/msg12.png)

In the left menu, you'll find the structure components that you can use to define the structure of the email (rows and columns).

![Journey Optimizer](./images/msg13.png)

Drag and drop a **1:2 column Left** from the menu into the canvas. This will be the placeholder for the logo image.

![Journey Optimizer](./images/msg14.png)

Drag and drop a **1:1 column** underneath the previous component. This will be the banner block.

![Journey Optimizer](./images/msg15.png)

Drag and drop a **1:2 column Left** underneath the previous component. This will be the actual content with an image on the left side and text on the right side.

![Journey Optimizer](./images/msg16.png)

Next, drag and drop a **1:1 column** underneath the previous component. This will be email's footer. Your canvas should now look like this:

![Journey Optimizer](./images/msg17.png)

Next, let's use Content Components to add content inside these blocks. Click on the **Content Components** menu item

![Journey Optimizer](./images/msg18.png)

Drag and drop an **Image** component in the first cell on the first row. Click **Browse**.

![Journey Optimizer](./images/msg19.png)

You'll then see this. Navigate to the folder **enablement-assets** and select the file **luma-logo.png**. Click **Select**.

![Journey Optimizer](./images/msg21.png)

You're now back here:

![Journey Optimizer](./images/msg25.png)

Go to **Content Components** and drag and drop an **Image** component in the first cell on the first row. Click **Browse**.

![Journey Optimizer](./images/msg26.png)

In the **Assets** pop-up, go to the **enablement-assets** folder. In this folder, you'll find all assets previously prepared and uploaded by the creative team. Select **module23-thankyou-new.png** and click **Select**. 

![Journey Optimizer](./images/msg28.png)

You'll then have this:

![Journey Optimizer](./images/msg30.png)

Select your image and in the right menu, scroll down until you see the **Size** width slider component. Use the slider to change the width to f.i. **60%**.

![Journey Optimizer](./images/msg31.png)

Next, go to **Content Components** and drag and drop a **Text** component in the structure component on the fourth row. 

![Journey Optimizer](./images/msg33.png)

Select the default text **Please type your text here.** as you would do with any text editor. Write **Dear** instead. Notice the text toolbar displayed when you are in text mode.

![Journey Optimizer](./images/msg34.png)

In the toolbar click the **Add personalization** icon.

![Journey Optimizer](./images/msg35.png)

Next, you need to bring the **First name** personalization token which is stored under `profile.person.name.firstName`. In the menu, find the **Person** element, drill down to the **Full Name** element, and then click the **+** icon to add the First Name field onto to expression editor.

Click **Save**.

![Journey Optimizer](./images/msg36.png)

You'll now notice how the personalization field has been added to your text. 

![Journey Optimizer](./images/msg37.png)

In the same text field, hit **Enter** twice to add two lines and write **Thank you for creating your account with Luma!**.

![Journey Optimizer](./images/msg38.png)

The final check to perform to ensure your email is ready is to preview it, click on the **Preview** button.

![Journey Optimizer](./images/msg50.png)

Start by identifying which profile you want to use for the preview. Select the **email** namespace by clicking on the icon next to **Enter identity namespace** field.

In the list of identity namespaces, select the **Email** namespace.

In the **Identity value** field, enter the email address of a previous demo profile that is already stored in the Real-time Customer Profile. For example **woutervangeluwe+06022022-01@gmail.com** and click on the **Find Test Profile** button

![Journey Optimizer](./images/msg53.png)

Once your profile shows up in the table, click on the **Preview** tab to access the preview screen.

When the preview is ready, validate that the personalization is correct in the subject line, the body text as well as the unsubscription link is highlighted as an hyperlink.

Click **Close** to close the preview.

![Journey Optimizer](./images/msg54.png)

Click **Save** to save your message.

![Journey Optimizer](./images/msg55.png)

Go back to the message dashboard by clicking the **arrow** next to the subject line text in the top-left corner.

![Journey Optimizer](./images/msg56.png)

You've now completed the draft version of your registration email. Click **Publish** to publish your message so you can use it in a journey.

![Journey Optimizer](./images/msg57.png)

Click **Publish** again.

![Journey Optimizer](./images/msg58.png)

Wait until you see a green confirmation pop-up at the bottom of the screen indicating that the message is published. 

![Journey Optimizer](./images/msg59.png)

You have finished this exercise.

Next Step: [7.3 Journey Optimizer: Setup Journey](./ex3.md)

[Go Back to Module 7](./journey-orchestration-create-account.md)

[Go Back to All Modules](../../overview.md)
