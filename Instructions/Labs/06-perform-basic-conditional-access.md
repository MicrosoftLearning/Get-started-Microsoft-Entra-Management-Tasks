---
lab:
  title: Perform basic Conditional Access policy tasks
  description: In this exercise you will learn to create and configure a Conditional
    Access policy and test its results with the What If analysis tool.
  duration: 10 minutes
  level: 200
  islab: true
---

# Exercise - Perform basic Conditional Access policy tasks

In this exercise you will learn to create and configure a Conditional Access policy and test its results with the What If analysis tool.

This exercise should take approximately **10** minutes to complete.

## Task 1 - Review a Conditional Access policy

1. Open the [Microsoft Entra admin center](https://entra.microsoft.com) at `https://entra.microsoft.com`.
1. Log in using the credentials for your tenant.
1. From the menu on the left, select **Protection** submenu and then select **Conditional access**.
1. Review the information provided on the **Conditional Access Overview** page.

   **Note** - You can see how many policies you have enabled, and how many users who have logged in recently that are not covered by a policy; along with other details.

1. Select the **+ Create new policy** from the top menu.
1. In the **Name** box enter **Block Bhogeswar from using Sway**.
1. In the **Assignments** section select **0 users and groups selected** text.

   - In the **Include** section mark the **Select users and groups** item.
   - Put a mark in the **Users and groups** box.
   - When the list of users and groups opens, select **Bhogeswar Kalita** from the list.
   - Use the **Select** button to add the user.
   - Select the word **Exclude** to switch tabs.
   - Put a mark in the **Users and groups** box.
   - When the list of users ang groups opens, select **the admin user you are using** from the list.
   - Use the **Select** button to exclude this user.

   **Lab tip** - We have added a user for this policy and we have added an exclude for our admin, to make sure they are not accidentally locked out by a policy change.

1. Find the section **Target resources** section.
1. Select the **No target resources selected** text from this section.

   - Make sure **Resources (formerly cloud apps)** is chosen in the dropdown.
   - Put a mark in the **Select resources** item.
   - In the section titled **Select** chose the word **None**.
   - When the resource selection dialog opens, enter **Sway** into the search bar.
   - Put a check in the box next to **Sway** then use the **Select** button to approve the choice.

   **Lab tip** - We have chosen the app Sway to be the resource this policy works on. You could choose multiple apps, or you could even choose to exclude apps.

1. Open and review the **Network** section, but we are not going to use that for this lab.
1. Open and review the **Conditions** section, but we are not using it for this lab.

   **Lab tip** - Network and Conditions are powerful options in the Conditional Access policy, but they are not required for this simple policy to block access to an app.  You would use them if you wanted to do things like restrict access for user working from a specific location, or block access if a user has show risky behavior.  There are many granular options that you can choose from, or even combine together.

1. Find the section titled **Access controls**.
1. Under the word **Grant** select the text **0 controls selected**.
1. When the Grant dialog opens, select the **Block access** item.
1. Use the **Select** button to accept the change.

   **Lab tip** - You have not set the values needed to create a simple block access policy to the Sway app for Bhogeswar.  In the Access controls section, we could have allowed access with specific conditions like MFA or a domain joined device.

1. At the bottom of the **Conditional Access** interface, find the **Enable policy** item.
1. Set the value to **On**.
1. Select the **Create** button.

   **Lab tip** - You have three options to pick from, and you can change value at any time, without having to change the policy.
   - On = enables the policy to run
   - Off = turn the policy off in case you need to modify it.
   - Report-only = use this option to review the outcome of the policy before you fully turn it on.

## Task 2 - Perform a What If analysis for a conditional access policy

1. Open the [Microsoft Entra admin center](https://entra.microsoft.com) at `https://entra.microsoft.com`.
1. Log in using the credentials for your tenant.
1. From the menu on the left, select **Protection** submenu and then select **Conditional access**.
1. From the Conditional access screen select the **What if** option from the top menu.
1. In the section **User or Workload identity** select the text **No user or service principal selected**.
1. Make sure the circle next to **User** is marked.
1. Select the text **No user selected**.
1. From the Users list, put a mark next to **Bhogeswar Kalita**, then use the **Select** button.
1. In the **Cloud apps, actions, or authentication context**, select the text **Any cloud app**.
1. When the **Select target type** dialog opens, confirm that **Cloud apps** is chosen in the dropdown.
1. Mark the **Select apps** circle.
1. Use the search to find the **Sway** app, then use the **Select** botton to finalize.
1. Scroll down to the bottom of the What If tool.
1. Select the button **What If**.

   **Note** - the results appear off the bottom of the screen, so you will need to scroll down again.

1. You should see the **Block Bhogeswar from using Sway** policy listed, and it is blocking access.

### Subtask 1 - Try a different app in the What If analysis

1. Scroll back to the top of the **What If** tool.
1. In the **Cloud apps, actions, or authentication context**, select the text **1 app selected**.
1. Select the elipsis `...` next to **Sway** and choose **Remove**.
1. Select the text **None** to pick a new app.
1. Search for **Office 365** and choose it from the list, then use the **Select** button.
1. Scroll down to the bottom again.
1. Select the **What If** button.
1. You should see that the **Block Bhoseswar from using Sway** policy did not apply.

