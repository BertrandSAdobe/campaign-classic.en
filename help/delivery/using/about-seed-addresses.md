---
title: About seed addresses
seo-title: About seed addresses
description: About seed addresses
seo-description: 
page-status-flag: never-activated
uuid: e27ba49c-252f-4e05-b387-34b778487c82
contentOwner: sauviat
products: SG_CAMPAIGN/CLASSIC
content-type: reference
discoiquuid: 6682fbe2-786a-43e7-88d9-86c31418e632
index: y
internal: n
snippet: y
---

# About seed addresses{#about-seed-addresses}

Seed addresses are used to target recipients who do not match the defined target criteria. This way, recipients who are out of the delivery scope can receive the delivery, as any other target recipient would.

Once of the main reason for using them is **your mailing list protection**. Inserting seed addresses into your mailing list lets you be noticed if it is being used by a third-party, as the seed addresses it contains will receive the deliveries sent to your mailing list.

Moreover, seed addresses let you **preview and test the deliveries personalization and rendering** before their sending, by sending them proofs (see [Using seed addresses as proof](../../delivery/using/about-seed-addresses.md#using-seed-addresses-as-proof)).

The seed addresses feature has the following benefits:

* Random substitution of fields with data taken from recipient profiles: this lets you enter only the email address, for instance in the seed address section, and let Campaign automatically fill in the other fields form the profile (see [Use case: configuring the field substitution](../../delivery/using/use-case--configuring-the-field-substitution.md)).
* When using a workflow with Datamanagement functionalities, the additional data processed in deliveries can be entered at seed address level to force values: this sidesteps random value substitution.
* Seed addresses are automatically excluded from reports on the following delivery statistics: **Clicks**, **Opens**, **Unsubscriptions**.

Seed addresses are added to the target of deliveries by being imported or by being created directly in the delivery or the campaign.

>[!NOTE]
>
>Seed addresses do not belong to the recipients table,they are created in a separate table. If you extend the recipients table with new data, you have to extend the seed addresses table as well with the same data. Otherwise, they extended fields will not be taken into account for seed addresses.   
>An example of how to extend the seed addresses table is presented in this section: [Use case: selecting seed addresses on criteria](../../delivery/using/use-case--selecting-seed-addresses-on-criteria.md)

For direct mail deliveries, seed addresses are added during extraction and mixed in the output document.

>[!CAUTION]
>
>For direct mail deliveries, the extraction file format must comply with the following limitations:  
>
>* It must not use the option **Handle groupings (GROUP BY+HAVING)**.
>* If element collections are extracted, these fields will have an empty value for the seed addresses, unless the **Single row (expert user)** option is selected. For more on this, refer to [this section](../../platform/using/exporting-data.md#step-7---data-formatting).
>
