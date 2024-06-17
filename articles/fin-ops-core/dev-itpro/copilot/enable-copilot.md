---
title: Copilot prerequisites
description: Learn about instructions for administrators on how to enable basic Copilot capabilities in finance and operations apps.
author: cabeln
ms.author: cabeln
ms.topic: how-to
ms.date: 02/16/2024
ms.custom:
 - bap-template
ms.reviewer: johnmichalak
ms.collection:
  - bap-ai-copilot
audience: Application User
ms.search.region: Global
ms.search.form:
---

# Copilot prerequisites

[!include [banner](../includes/banner.md)]

Copilot brings features that help users complete their tasks more efficiently. For example, one feature uses the power of generative AI to provide in-app help guidance.

This article describes how to enable basic Copilot capabilities in finance and operations apps. Most Copilot features in finance and operations apps require this basic foundation. For some features, this foundation is all that's needed, but other features may require additional installations and/or feature management (see also [Overview of enabling Copilot capabilities and features](enable-copilot-overview.md)).

## Country/region and language availability

For information about which countries/regions and languages the Copilot capability in Microsoft Dynamics 365 Supply Chain Management becomes available in, see the [Copilot international availability guide](https://dynamics.microsoft.com/availability-reports/copilotreport/).

## Environment requirements

Your environment must be a cloud-deployed environment. Copilot in finance and operations apps isn't supported in cloud-hosted development environments.

## Enable Power Platform integration

You must have enabled the [Power Platform integration](../power-platform/enable-power-platform-integration.md) in Microsoft Dynamics Lifecycle Services. (However, you don't have to enable dual-write for this feature.)

> [!IMPORTANT]
> Depending on the availability of Copilot and generative AI back-office services in your region, your Dataverse environment might also have to be set up to support cross-region calls. For more information, see [Enable copilots and generative AI features](/power-platform/admin/geographical-availability-copilot).
>
> You don't have to set up support for cross-region calls if the required AI services are already available in your Dataverse environment.
>
> For information about the capabilities and limitations of AI-powered Copilot features in Microsoft finance and operations apps, see [Responsible AI FAQs for the Microsoft Dynamics 365 finance and operations platform](../responsible-ai/responsible-ai-overview.md).

## <a name="enable-sql-key"></a>Enable the Sql row version change tracking license key

Follow these steps to check the status of the **Sql row version change tracking (Preview)** license key and enable it as required. If the key isn't enabled, you receive an error when you try to install the Copilot application in Power Platform admin center.

1. Go to **System administration \> Setup \> License configuration**.
1. On the **Configuration keys** tab, scroll down to the **Sql row version change tracking (Preview)** key. If the key is already enabled, skip the rest of this procedure. If it isn't enabled, move on to the next step.
1. Put your system into maintenance mode as described in [Maintenance mode](../sysadmin/maintenance-mode.md).
1. Return to the **License configuration** page, and enable the **Sql row version change tracking (Preview)** key.
1. Turn off maintenance mode as described in [Maintenance mode](../sysadmin/maintenance-mode.md).

## Enable Power Platform to publish bots with AI features

To enable Power Platform to publish bots with AI features, follow these steps.

1. Open [Power Platform admin center](https://admin.powerplatform.microsoft.com/).
1. In the navigation pane, select **Settings**.
1. In the list, select the row where the **Name** is *Publish bots with AI features*.
1. The **Publish bots with AI features** dialog opens. Set the slider to **Enabled**.
1. Select **Save**.

## <a name="install-copilot-app"></a>Install the Copilot application in your finance and operations apps environment

Follow these steps to install the Copilot application in your finance and operations apps environment.

1. Open the [Copilot in Microsoft Dynamics 365 Supply Chain Management](https://aka.ms/dynamicsfnocopilot_scmaiapp) page in the Microsoft commercial marketplace.
1. Select **Get it now**.
1. The deployment process opens [Power Platform admin center](https://admin.powerplatform.microsoft.com/). Select the Dataverse environment connected to your finance and operations apps environment to install the Copilot application.

    > [!IMPORTANT]
    > **Troubleshooting:** You might receive the following error message while you install the Copilot application in Power Platform admin center: "Unable to complete updates to the Track changes option for table: 'EcoResProductTranslationAIEntity'. Exception details: This functionality requires enabling sql row version change tracking feature. Please enable SQL Row version configuration key." If you receive this error, follow the instructions in the [Enable the Sql row version change tracking license key](#enable-sql-key) section.

1. You can follow the status of the installation by opening the detail view of the environment. In the **Resources** field, select **Dynamics 365 apps**. During installation, the status of the Copilot application is *Installing*. After installation is completed, the status changes to *Installed*. If an error occurs, the status changes to *Failed*. In this case, you can find details about the error in the **Notifications** field.

## Enable the required security roles

Users who should have access to the functionality must be assigned the *AIB Roles* and *Finance and Operations AI* security roles in Dataverse.

1. In the detail view of the environment, in the **Access** field, select *Users* or *Teams*.
2. Select the users or teams that should have access, and assign the *AIB Roles* and *Finance and Operations AI* security roles to them.
