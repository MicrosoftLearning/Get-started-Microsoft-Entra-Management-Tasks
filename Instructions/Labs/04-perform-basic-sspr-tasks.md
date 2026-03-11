---
lab:
  title: Perform basic Self-Service Password Rest (SSPR) tasks
  description: In this exercise you will learn where the self-service password reset feature is located in Microsoft Entra and explore the process to configure it.
  duration: 15 minutes
  level: 200
  islab: true
  primarytopics:
    - Microsoft Entra
---

# Exercise - Perform basic Self-Service Password Rest (SSPR) tasks

In this exercise you will learn where the self-service password reset feature is located in Microsoft Entra and explore the process to configure it.

This exercise should take approximately **15** minutes to complete. <!-- update with estimated duration -->

## Task 1 - View the SSPR properties for a specific group

1. Open the [Microsoft Entra admin center](https://entra.microsoft.com) at `https://entra.microsoft.com`.
1. Log in using the credentials for your tenant.
1. From the menu on the left, open **Protection** submenu and then select **Password reset**.
1. Find the **Self service password enabled** bar.

   | Value | What it means |
   | :---  | :--- |
   | None | No users can use the SSPR feature |
   | Selected | Only members of the selected group(s) can use SSPR |
   | All | All users can use the SSPR feature |

1. Set the value to **Selected**.
1. Select the text **No groups selected**.
1. Mark the **Project23** group we created previously.
1. Use the **Select** button to complete your choice.
1. **Save** your configuration.

### Subtask 1 - View SSPR authentication methods

1. Select **Authentication methods** from the menu within **Password reset**.
1. Select **1** as the value for **Number of methods required to reset**.

   **Note** - this value represents how many different ways the user is required to sign-in to the password reset tool, before they are allowed to reset their password. Note that using a password is not an option.

1. Select **Email**, **Mobile phone**, and **Mobile app code** for **Methods available to user**.

   **Note** - if you use Security Questions you have to specific the number of questions the user is required to create and answer.

1. Use the button at the top to **Save** your choices.
1. You have added an Authentication method to your self-service password reset.

### Subtask 2 - View SSPR registration

1. Select **Registration** from the menu within **Password reset**.
1. Make sure the **Require users to register when signing in?** value is set to **Yes**.
1. Set the **Number of days before users are asked to re-confirm...** to **90** days.
1. Select **Save** to save your changes.

### Subtask 3 - View SSPR reset notifications

1. Select **Notifications** from the menu withing **Password reset**.
1. Leave the **Notify users on password reset?** at the default of **Yes**.
1. Change the **Notify all admins when other admins reset their password?** value to **Yes**.
1. Use the **Save** option to save your changes.
