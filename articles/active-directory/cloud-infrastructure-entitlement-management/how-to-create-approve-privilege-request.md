---
title: Create or approve a request for permissions in the Remediation dashboard in Permissions Management
description: How to create or approve a request for permissions in the Remediation dashboard.
services: active-directory
author: kenwith
manager: rkarlin
ms.service: ciem
ms.workload: identity
ms.topic: how-to
ms.date: 02/23/2022
ms.author: kenwith
---

# Create or approve a request for permissions

> [!IMPORTANT]
> Microsoft Entra Permissions Management is currently in PREVIEW.
> Some information relates to a prerelease product that may be substantially modified before it's released. Microsoft makes no warranties, express or implied, with respect to the information provided here.

This article describes how to create or approve a request for permissions in the **Remediation** dashboard in Permissions Management. You can create and approve requests for the Amazon Web Services (AWS), Microsoft Azure, or Google Cloud Platform (GCP) authorization systems.

The **Remediation** dashboard has two privilege-on-demand (POD) workflows you can use:
- **New Request**: The workflow used by a user to create a request for permissions for a specified duration.
- **Approver**: The workflow used by an approver to review and approve or reject a user's request for permissions.


> [!NOTE]
> To view the **Remediation** dashboard, you must have **Viewer**, **Controller**, or **Administrator** permissions. To make changes on this tab, you must have **Controller** or **Administrator** permissions. If you don't have these permissions, contact your system administrator.

## Create a request for permissions

1. On the Permissions Management home page, select the **Remediation** tab, and then select the **My Requests** subtab.

    The **My Requests** subtab displays the following options:
    - **Pending**: A list of requests you've made but haven't yet been reviewed.
    - **Approved**: A list of requests that have been reviewed and approved by the approver. These requests have either already been activated or are in the process of being activated.
    - **Processed**: A summary of the requests you've created that have been approved (**Done**), **Rejected**, and requests that have been **Canceled**.

1. To create a request for permissions, select **New Request**.
1. In the **Roles/Tasks** page:
    1. From the **Authorization System Type** dropdown, select the authorization system type you want to access: **AWS**, **Azure** or **GCP**.
    1. From the **Authorization System** dropdown, select the accounts you want to access.
    1. From the **Identity** dropdown, select the identity on whose behalf you're requesting access.

        - If the identity you select is a Security Assertions Markup Language (SAML) user, and since a SAML user accesses the system through assumption of a role, select the user's role in **Role**.

        - If the identity you select is a local user, to select the policies you want:
            1. Select **Request Policy(s)**.
            1. In **Available Policies**, select the policies you want.
            1. To select a specific policy, select the plus sign, and then find and select the policy you want.

            The policies you've selected appear in the **Selected policies** box.

        - If the identity you select is a local user, to select the tasks you want:
            1. Select **Request Task(s)**.
            1. In **Available Tasks**, select the tasks you want.
            1. To select a specific task, select the plus sign, and then select the task you want.

            The tasks you've selected appear in the **Selected Tasks** box.

    If the user already has existing policies, they're displayed in **Existing Policies**.
1. Select **Next**.

1. If you selected **AWS**, the **Scope** page appears.

    1. In **Select Scope**, select:
        - **All Resources**
        - **Specific Resources**, and then select the resources you want.
        - **No Resources**
    1. In **Request Conditions**:
        1. Select **JSON** to add a JSON block of code.
        1. Select **Done** to accept the code you've entered, or **Clear** to delete what you've entered and start again.
    1. In **Effect**, select **Allow** or **Deny.**
    1. Select **Next**.

1. The **Confirmation** page appears.
1. In **Request Summary**, enter a summary for your request.
1. Optional: In **Note**, enter a note for the approver.
1. In **Schedule**, select when (how quickly) you want your request to be processed:
    - **ASAP**
    - **Once**
        - In **Create Schedule**, select the **Frequency**, **Date**, **Time**, and **For** the required duration, then select **Schedule**.
    - **Daily**
    - **Weekly**
    - **Monthly**
1. Select **Submit**.

    The following message appears: **Your Request Has Been Successfully Submitted.**

    The request you submitted is now listed in **Pending Requests**.

## Approve or reject a request for permissions

1. On the Permissions Management home page, select the **Remediation** tab, and then select the **My requests** subtab.
1. To view a list of requests that haven't yet been reviewed, select **Pending Requests**.
1. In the **Request Summary** list, select the ellipses **(…)** menu on the right of a request, and then select:

    - **Details** to view the details of the request.
    - **Approve** to approve the request.
    - **Reject** to reject the request.

1. (Optional) add a note to the requestor, and then select **Confirm.**

    The **Approved** subtab displays a list of requests that have been reviewed and approved by the approver. These requests have either already been activated or are in the process of being activated.
    The **Processed** subtab displays a summary of the requests that have been approved or rejected, and requests that have been canceled.


## Next steps


- For information on how to view existing roles/policies, requests, and permissions, see [View roles/policies, requests, and permission in the Remediation dashboard](ui-remediation.md).
- For information on how to create a role/policy, see [Create a role/policy](how-to-create-role-policy.md).
- For information on how to clone a role/policy, see [Clone a role/policy](how-to-clone-role-policy.md).
- For information on how to delete a role/policy, see [Delete a role/policy](how-to-delete-role-policy.md).
- For information on how to modify a role/policy, see Modify a role/policy](how-to-modify-role-policy.md).
- To view information about roles/policies, see [View information about roles/policies](how-to-view-role-policy.md).
- For information on how to attach and detach permissions for Amazon Web Services (AWS) identities, see [Attach and detach policies for AWS identities](how-to-attach-detach-permissions.md).
- For information on how to add and remove roles and tasks for Microsoft Azure and Google Cloud Platform (GCP) identities, see [Add and remove roles and tasks for Azure and GCP identities](how-to-attach-detach-permissions.md).
- For information on how to revoke high-risk and unused tasks or assign read-only status for Microsoft Azure and Google Cloud Platform (GCP) identities, see [Revoke high-risk and unused tasks or assign read-only status for Azure and GCP identities](how-to-revoke-task-readonly-status.md)
