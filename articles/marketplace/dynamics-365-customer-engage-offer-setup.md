---
title: Create a Dynamics 365 apps on Dataverse and Power Apps offer on Microsoft AppSource (Azure Marketplace).
description: Create a Dynamics 365 apps on Dataverse and Power Apps offer on Microsoft AppSource (Azure Marketplace).
ms.service: marketplace 
ms.subservice: partnercenter-marketplace-publisher
ms.topic: how-to
author: vamahtan
ms.author: vamahtan
ms.date: 05/25/2022
---

# Create a Dynamics 365 apps on Dataverse and Power Apps offer

This article describes how to create a _Dynamics 365 apps on Dataverse and Power Apps_ offer. Before you start, create a commercial marketplace account in [Partner Center](./create-account.md) and ensure it is enrolled in the commercial marketplace program.

## Before you begin

Review [Plan a Microsoft Dynamics 365 offer](marketplace-dynamics-365.md). It will explain the technical requirements for this offer and list the information and assets you’ll need when you create it.

## Create a new offer

1. Sign in to [Partner Center](https://partner.microsoft.com/dashboard/home).
1. On the Home page, select the **Marketplace offers** tile.

    [ ![Illustrates the Marketplace offers tile on the Partner Center Home page.](./media/workspaces/partner-center-home.png) ](./media/workspaces/partner-center-home.png#lightbox)

1. On the Marketplace offers page, select **+ New offer** > **Dynamics 365 apps on Dataverse and Power Apps**.

    [ ![Shows the 'New offer' button with the Customer Engagement & Power Apps offer type selected.](./media/dynamics-365/new-offer-dynamics-365-customer-engagement-workspaces.png) ](./media/dynamics-365/new-offer-dynamics-365-customer-engagement-workspaces.png#lightbox)

> [!IMPORTANT]
> After an offer is published, any edits you make to it in Partner Center appear on Microsoft AppSource only after you republish the offer. Be sure to always republish an offer after changing it.

## New offer

1. Enter an **Offer ID**. This is a unique identifier for each offer in your account.

    - This ID is visible to customers in the web address for the offer and in Azure Resource Manager templates, if applicable.
    - Use only lowercase letters and numbers. The ID can include hyphens and underscores, but no spaces. The combined sum of the Offer ID and Publisher ID is limited to 40 characters. For example, if your Publisher ID is `testpublisherid` and you enter **test-offer-1**, the offer web address will be `https://appsource.microsoft.com/product/dynamics-365/testpublisherid.test-offer-1`. In this case, the segment, “testpublisherid.test-offer-1” is 28 characters long, which is within the 40-character limit.
    - The Offer ID can't be changed after you select **Create**.

1. Enter an **Offer alias**. This is the name used for the offer in Partner Center.

    - This name isn't used on AppSource. It is different from the offer name and other values shown to customers.
    - This name can't be changed after you select **Create**.

1. Associate the new offer with a _publisher_. A publisher represents an account for your organization. You may have a need to create the offer under a particular publisher. If you don’t, you can simply accept the publisher account you’re signed in to.

    > [!NOTE]
    > The selected publisher must be enrolled in the [**Commercial Marketplace program**](marketplace-faq-publisher-guide.yml#how-do-i-sign-up-to-be-a-publisher-in-the-microsoft-commercial-marketplace-) and cannot be modified after the offer is created.

1. Select **Create** to generate the offer. Partner Center opens the **Offer setup** page.

## Alias

Enter a descriptive name that we'll use to refer to this offer solely within Partner Center. The offer alias (pre-populated with what you entered when you created the offer) won't be used in the marketplace and is different than the offer name shown to customers. If you want to update the offer name later, see the [Offer listing](dynamics-365-customer-engage-offer-listing.md) page.

## Setup details

1. On the _Offer setup_ page, choose one of the following options:

    - Select **Yes** to sell through Microsoft and have Microsoft host transactions on your behalf. 
    
        If you choose this option, the Enable app license management through Microsoft check box is enabled and cannot be changed.

        > [!NOTE]
        > This capability is currently in Public Preview.

    - Select **No**, if you prefer to only list your offer through the marketplace and process transactions independently.

        If you choose this option, you can use the **Enable app license management through Microsoft** check box to choose whether or not to enable app license management through Microsoft. For more information, see [ISV app license management](isv-app-license.md).

1. To let customers run your app’s base functionality without a license and run premium features after they’ve purchased a license, select the **Allow customers to install my app even if licenses are not assigned** box. If you select this second box, you need to configure your solution package to not require a license.

1. If you chose **No** in step 1 and chose not to enable app license management through Microsoft, then you can select one of the following:

    - **Get it now (free)** – List your offer to customers for free.
    - **Free trial (listing)** – List your offer to customers with a link to a free trial. The trial experience lets users deploy your solution to a live Dynamics 365 environment. Offer listing free trials are created, managed, and configured by your service and do not have subscriptions managed by Microsoft.

        > [!NOTE]
        > The tokens your application will receive through your trial link can only be used to obtain user information through Azure Active Directory (Azure AD) to automate account creation in your app. Microsoft accounts are not supported for authentication using this token.

    - **Contact me** – Collect customer contact information by connecting your Customer Relationship Management (CRM) system. The customer will be asked for permission to share their information. These customer details, along with the offer name, ID, and marketplace source where they found your offer, will be sent to the CRM system that you've configured. For more information about configuring your CRM, see [Customer leads](#customer-leads).

## Test drive

A test drive is a great way to showcase your offer to potential customers by giving them access to a preconfigured environment for a fixed number of hours. Offering a test drive results in an increased conversion rate and generates highly qualified leads. To learn more, start with [What is a test drive?](what-is-test-drive.md).

> [!TIP]
> A test drive is different from a free trial. You can offer either a test drive, free trial, or both. They both provide customers with your solution for a fixed period-of-time. But, a test drive also includes a hands-on, self-guided tour of your product’s key features and benefits being demonstrated in a real-world implementation scenario.

To enable a test drive, select the **Enable a test drive** check box and select the **Type of test drive**. You will configure the test drive later. With test drive, you must also configure your offer to a CRM system for customer leads (see next section). To remove test drive from your offer, clear this check box.

## Customer leads

[!INCLUDE [Connect lead management](includes/customer-leads.md)]

For more information, see [Customer leads from your commercial marketplace offer](partner-center-portal/commercial-marketplace-get-customer-leads.md).

Select **Save draft** before continuing to the next tab in the left-nav menu, **Properties**.

## Next steps

- [Configure offer properties](dynamics-365-customer-engage-properties.md)
- [Offer listing best practices](gtm-offer-listing-best-practices.md)
