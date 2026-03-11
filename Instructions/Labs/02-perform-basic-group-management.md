---
lab:
  title: Perform basic Group Management tasks
  description: In this exercise you will explore the beginner level tasks associated with creating and using groups. You make a new group and assign members and set some basic access levels.
  duration: 15 minutes
  level: 100
  islab: true
---

# Exercise - Perform basic Group Management tasks

In this exercise you will explore the beginner level tasks associated with creating and using groups. You make a new group and assign members and set some basic access levels.

This exercise should take approximately **15** minutes to complete.

## Task 1 - Create a Microsoft 365 group

1. Open the [Microsoft Entra admin center](https://entra.microsoft.com) at `https://entra.microsoft.com`.
1. Log in using the credentials for your tenant.
1. From the menu on the left, select **Groups** and then **All groups**.
1. Select **New group** option.
1. Enter the requested information:

   | Field | Value |
   | :---  | :---  |
   | Group type | Microsoft 365 |
   | Group name | Project23 |
   | Group description | This group consists of members of the new AI Simulation software with codename Project23 |
   | Membership type | Assigned |

1. Under the **Members** heading, select **No member selected**.
1. Add **Bhogeswar Kalita**, by marking the box and choosing the **Select** button.
1. Select the **Create** button.

## Task 2 - Create a Security group

1. Open the [Microsoft Entra admin center](https://entra.microsoft.com) at `https://entra.microsoft.com`.
1. Log in using the credentials for your tenant.
1. From the menu on the left, select **Groups** and then **All groups**.
1. Select **New group** option.
1. Enter the requested information:

   | Field | Value |
   | :---  | :---  |
   | Group type | Security |
   | Group name | Guest Users |
   | Group description | This group has all the Guest users currently in the tenant. |
   | Membership type | Dynamic User |

1. Under the **Dynamic user members** heading, select **Add dynamic query**.
1. Create a dynamic query with the following values:

   | Field | Value |
   | :---  | :---  |
   | Property | userType |
   | Operator | Equals |
   | Value | Guest |

1. Select the **Save** item from the top of the page.
1. Select the **Create** button.

   **Note** - It will take up to 2 minutes for the group to be populate.

1. From the **Groups** select the **Refresh** item.
1. Select the **Guest Users** group we just created.
1. Select **Members**.

## Task 3 - Add an existing user to a new group

1. Open the [Microsoft Entra admin center](https://entra.microsoft.com) at `https://entra.microsoft.com`.
1. Log in using the credentials for your tenant.
1. From the menu on the left, select **Groups** and then **All groups**.
1. Select the **Project23** group we created in Task 1.
1. Select the **Members** option from the menu.
1. Select **+ Add members** from the menu near the top.
1. Mark the box next to **External User** and use the **Select** button.

### Subtask 1 - Alternative method to add an existing user to a new group

1. Open the **Users** menu, then select **All users**.
1. Find and select **External User** from the list.
1. Select the **Groups** item from the menu.
1. Select the option to **+ Add memberships**.
1. Mark an existing group and use the **Select** button to add them.

## Task 4 - Add licenses and owners to a group

1. Open the [Microsoft Entra admin center](https://entra.microsoft.com) at `https://entra.microsoft.com`.
1. Log in using the credentials for your tenant.
1. From the menu on the left, select **Groups** and then **All groups**.
1. Select the **Project23** group we created in Task 1.
1. Choose the **Owners** option from the menu.

   **Note** - Your tenant administrator will automatically be added as the owner of a group, if no owner is specified.

1. Select the **+ Add owners** menu item.
1. Mark the box next to **Bhogeswar** and use the **Select** button.
1. Notice the new owner has been added to the group.

### Subtask 1 - Adding a license to a group

1. Open a new tab in your browser.
1. Connect to [Microsoft 365 admin cetner](https://admin.microsoft.com) at `https://admin.microsoft.com`.
1. From the menu on the left, open the **Billing** section and select **Licenses**.
1. Select the **Microsoft Power Automate Free** license.
1. Choose the **Groups** tab from the newly opened screen.
1. Select the **+ Assign licenses** item.
1. Use the dropdown on the right side of the screen to select the **Project23** group created earlier.
1. Use the **Assign** button at the bottom of the screen.
1. Close the **You assigned licenses...** notification.
1. Use the **Refresh** button to see the added group licenses.
