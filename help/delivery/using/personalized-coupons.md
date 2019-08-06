---
title: Personalized coupons
seo-title: Personalized coupons
description: Personalized coupons
seo-description: 
page-status-flag: never-activated
uuid: 7fea5e87-1949-4166-8633-e6bf9bb20486
contentOwner: sauviat
products: SG_CAMPAIGN/CLASSIC
content-type: reference
discoiquuid: fd579c95-37f6-4a8a-8141-b61d1887fd6c
index: y
internal: n
snippet: y
---

# Personalized coupons{#personalized-coupons}

Adding coupons to your deliveries can give your recipients enhanced value for products and services. You can use the Campaign coupon module to create a set of coupons that you expect to add to upcoming marketing offers. When you are ready to create a delivery, assign the applicable coupons. Since coupons are valid for a select period, an assigned coupon is uniquely linked to its delivery message. Also, Campaign confirms that there are enough coupons for the number of messages before the delivery is sent.

>[!NOTE]
>
>Coupon management is a package that must be installed. To confirm that you have Coupon management, check** Administration > Configuration > Package management > Installed packages.** 
>Coupon data can be imported and exported using CSV and XML formats. For details regarding importing and exporting, refer to [this section](../../platform/using/generic-imports-and-exports.md).

## Creating a coupon {#creating-a-coupon}

The coupon module gives you two options when creating coupons:

* **Anonymous**: A generic coupon for select recipients or lists of recipients.
* **Individual**: A personalized coupon for select recipients.

Before following the steps below, make sure that you know the type of coupon you want to create.

1. In the Campaign tree, go to **Resources > Campaign management > Coupons**.

   ![](assets/deliv_coup_01.png)

1. Click the **New** button.
1. Enter the name of the coupon in **Label** field. A unique code has been automatically entered in **Coupon code**. You can keep the code or enter a new one.

   ![](assets/deliv_coup_02.png)

1. Choose **Start date** and **End date** to set the period in which the coupon is valid.
1. In **Coupon type**, choose Anonymous or Individual.

   **Anonymous coupons**: An anonymous coupon is identical for all recipients. Confirm that Anonymous is selected in the **Coupon type** menu and click **Save** to generate the coupon.

   **Individual coupons**: An individual coupon can be further personalized with additional coupon codes. For example, an individual coupon is created for a sale at a sports equipment store. However, the list of recipients is long and they do not share the same enthusiasm for a single sport. You can add code names for the individual coupon based upon a sport (e.g. soccer, football, baseball etc.) and send each code to the applicable recipients.

    1. When choosing Individual, a new tab, Coupons, appears on the lower left. Go to the **Coupons** tab and click **Add**.
    1. Enter a unique code for the individual coupon when prompted by the pop-up window.
    1. Click **Save** to generate the coupon.

   For more details about the Coupons tab, see [Configuring individual coupons](../../delivery/using/personalized-coupons.md#configuring-individual-coupons).

   >[!NOTE]
   >
   >Individual coupons can be imported in bulk. For details regarding importing and exporting, refer to [this section](../../platform/using/generic-imports-and-exports.md).

### Configuring individual coupons {#configuring-individual-coupons}

![](assets/deliv_coup_03.png)

The Coupons tab is only available with Individual coupons. After a coupon is associated with a delivery, the Coupons tab provides the following details:

* **Status**: Coupon availability.
* **Redeemed on**: The date the coupon is redeemed.
* **Channel**: The channel used to send the coupon.
* **Address**: The recipients' email addresses.

Values for **status**, **channel**, and **address** are automatically completed. However, the values for **redeemed on** are not recovered by Campaign. They can be completed by importing a file that has the details for coupon redemption.

## Inserting a coupon into an email delivery {#inserting-a-coupon-into-an-email-delivery}

In the example below, the delivery is created from the Home page. For detailed instructions on how to create a delivery, refer to [this section](../../delivery/using/about-email-channel.md). You can also add a coupon to a delivery in a workflow.

1. Go to **Campaigns** and choose **Deliveries**.
1. Click **Create**.

   ![](assets/deliv_coup_04.png)

1. Enter a name in **Label** and click **Continue**.
1. Click **To** to add recipients.
1. Click **Add** to choose recipients for the delivery. Once you have selected your recipients, click **Ok** to return to the delivery.

   ![](assets/deliv_coup_05.png)

1. Enter a subject and add content to the message.

   ![](assets/deliv_coup_06.png)

1. In the toolbar, click **Properties** and choose the **Advanced** tab.
1. Click the folder icon for **Coupon management**.

   ![](assets/deliv_coup_07.png)

1. Choose the coupon and click **Ok**. Click **Ok** again.

   ![](assets/deliv_coup_08.png)

1. Click on the message to choose where you want to place the coupon.

   ![](assets/deliv_coup_09.png)

1. Click the personalization icon to choose one of the following based upon the type of coupon:

    * Anonymous coupon: **Coupon > Coupon code**
    
      ![](assets/deliv_coup_10.png)

    * Individual coupon: **Coupon value > Coupon code**
    
      ![](assets/deliv_coup_11.png)

      The coupon is inserted into the message as code rather than the name you assigned. The code is used within the Campaign standard data model.

   ![](assets/deliv_coup_12.png)

1. Run a test to confirm the name you assigned to the coupon. Go to the **Preview** tab and click **Test personalization**. Choose a recipient for the test.

   ![](assets/deliv_coup_13.png)

   Following the test, the coupon should appear as the assigned name rather than the code.

   ![](assets/deliv_coup_14.png)

1. In the toolbar, click **Send** (upper left) and choose how you want to send the delivery.

   ![](assets/deliv_coup_15.png)

1. Click **Analyze**. If the analysis log confirms that there are enough coupons for all recipients, click **Confirm delivery** to send it.

   ![](assets/deliv_coup_16.png)

>[!NOTE]
>
>For instructions on how to manage insufficient coupons for a delivery, see [Managing insufficient coupons](../../delivery/using/personalized-coupons.md#managing-insufficient-coupons)

To confirm that the delivery was successful:

1. Go to **Explorer > Resources > Campaign management > Coupons**.
1. Click the **Deliveries** tab.

   ![](assets/deliv_coup_17.png)

   The status reads as **Finished** for a successful delivery.

>[!NOTE]
>
>By default, the coupon management module uses an **nms:recipient **table. For instructions on how to use other tables, see [Editing schemas](../../configuration/using/data-schemas.md).

## Managing insufficient coupons {#managing-insufficient-coupons}

The delivery analysis stops if there are fewer coupons than messages. In such a case, you can import more coupons or restrict the number of messages. Follow the instructions below if you want to limit the number of messages.

1. Go to the email delivery window.
1. Click **To**.
1. In **Select target**, go to the **Exclusions** tab.

   ![](assets/deliv_coup_18.png)

1. In the exclusion settings section, click **Edit**.
1. Enter the number of messages you want to send in **Limit delivery to...messages** and click **Ok**. You can send the delivery.

   ![](assets/deliv_coup_19.png)

>[!NOTE]
>
>When managing a limited number of coupons, a delivery workflow lets you split the delivery based upon your criteria. It is a good option if you want to send coupons to a select population without restricting the target.
