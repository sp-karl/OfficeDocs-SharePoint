---
ms.date: 05/20/2024
title: "Restrict OneDrive access by security group"
ms.reviewer: nibandyo
ms.author: mactra
author: MachelleTranMSFT
manager: jtremper
audience: Admin
f1.keywords:
- CSH
ms.topic: how-to
ms.service: one-drive
ms.localizationpriority: medium
ms.collection: 
- Strat_OD_admin
- Highpri
- Tier2
- M365-sam
- M365-collaboration
- essentials-compliance
- essentials-security
search.appverid:
ms.assetid: 
ms.custom:
- admindeeplinkSPO
- onedrive-toc
description: "Learn how to allow only users in specified security groups to access OneDrive."
---

# Restrict OneDrive access by security group

[!INCLUDE[Advanced Management](includes/advanced-management.md)]

You can restrict access and sharing of OneDrive content to users in specified Microsoft Entra ID security groups. Even if other users outside of these security groups are licensed for OneDrive, they won’t have access to their own OneDrive or any shared OneDrive content when this policy is in effect. OneDrive access restriction at tenant level is applied when a user attempts to open a OneDrive or a file. 

You can use this to prevent new users from accessing any OneDrive content. For example, you can restrict OneDrive access and sharing to your new users, guest or frontline users. 

Note that users who are not members of the specified security group can still see files in organization-wide search and Copilot experiences if they have existing permissions to the file prior to the policy configuration. However they will not be able to open the file or OneDrive if they are not part of the specified security group. 

Note - If you want to prevent oversharing of OneDrive content also for users with existing permissions, we recommend you to enforce OneDrive site access restriction to inidividual user's OneDrive. For more information, see [Restrict access to a user's OneDrive content to people in a security group](onedrive-site-access-restriction.md).

## Requirements

To access and use this feature, your organization must have one of the following subscriptions:

- Microsoft SharePoint Premium - SharePoint Advanced Management
- Office 365 E5/A5
- Microsoft 365 E5/A5

## Specify security groups for OneDrive access

To enable this feature:

1. Go to <a href="https://go.microsoft.com/fwlink/?linkid=2185071" target="_blank">Access control in the SharePoint admin center</a>, and sign in with an account that has [admin permissions](sharepoint-admin-role.md) for your organization.

2. Select **Restrict OneDrive access**.

3. Select **Restrict OneDrive access to only users in specified security groups**.

    :::image type="content" source="media/restrictonedriveaccess.png" lightbox="media/restrictonedriveaccess.png" alt-text="Restrict OneDrive access on the Access control page in the SharePoint admin center":::

4. Add the security groups (maximum of 10) you want to be able to use OneDrive.

5. Select **Save**.

> [!IMPORTANT]
> Users who aren't members of the specified security groups will lose access to their own OneDrive and any shared OneDrive content. Sharing of content will be allowed only with the specified security group or members of the specified security group.

## Audit events

[Audit events](/microsoft-365/compliance/audit-log-activities) are available in Microsoft Purview compliance portal to help you monitor restricted access control activities. Audit events are logged for the following activities:

- Enabled Restricted OneDrive access and sharing
- Disabled Restricted OneDrive access and sharing

## Related topics

[Restrict access to a user's OneDrive content to people in a security group](onedrive-site-access-restriction.md).

[Restrict access control for SharePoint sites](restricted-access-control.md)

[Data access governance insights for SharePoint sites](data-access-governance-reports.md)
