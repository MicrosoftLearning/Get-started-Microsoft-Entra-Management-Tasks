---
lab:
  title: Perform basic Mulitfactor Authentication tasks
  description: In this exercise you will explore the MFA setup process and configure
    a basic MFA deployment.
  duration: 10 minutes
  level: 200
  islab: true
---

# Exercise - Perform basic Multifactor Authentication tasks

In this exercise you will explore the MFA setup process and configure a basic MFA deployment.

This exercise should take approximately **10** minutes to complete.

## Task 1 - Enable / Disable Per-user MFA settings

1. Open the [Microsoft Entra admin center](https://entra.microsoft.com) at `https://entra.microsoft.com`.
1. Log in using the credentials for your tenant.
1. From the menu on the left, open the **Identity** submenu
1. Select **Users** and then select **All users**.
1. Look at the menu on the top of the new screen and find **Per-user MFA**.
1. Select **Per-user MFA**.
1. Put a mark in the box next to **Bhogeswar Kalita**.
1. Select **Enable MFA** from the top of the list.
1. Read the message box that pops up.

   **Note** - This is a manual URL that you can email to the user, if you want to let them know to set up MFA.

1. Select **Enable** button.
1. Note that after a few seconds **enforced** shows up next to Bhogeswar's name.

## Task 2 - Review the Service settings for MFA

1. Open the [Microsoft Entra admin center](https://entra.microsoft.com) at `https://entra.microsoft.com`.
1. Log in using the credentials for your tenant.
1. From the menu on the left, open the **Identity** submenu.
1. Select **Users** and then select **All users**.
1. Select **Per-user MFA** item.
1. Select **Service settings**.
1. Review the settings you can configure:

   | Setting | What is it for |
   | :--- | :--- |
   | App passwords | There are some legacy apps that won't work with MFA, use this setting to allow a user to keep using them. |
   | Trusted IPs | If your company has a specifc set of IP-address ranges that are always known safe, you can allow users to by-pass MFA the logging in. |
   | Verification options | Select the methods you are willing to allow users to use for their second factor of authentication. |
   | Remember multifactor authentication on trusted device | If your users are using a device that you trust, like a company managed laptop; you can allow them to retain thier MFA approved status for a specified number of days. |

1. Select the **Discard** button if you made any changes.
1. This is one method of configuring MFA for your users.

## Task 3 - View MFA account lockout settings

1. Open the [Microsoft Entra admin center](https://entra.microsoft.com) at `https://entra.microsoft.com`.
1. Log in using the credentials for your tenant.
1. From the menu on the left, open the **Protection** submenu.
1. Scroll to the bottom of the list and select **Show more**.
1. Select **Multifactor authentication** from the menu.
1. Select **Account lockout** from the menu.
1. Set the following lockout values:

   | Field | Value |
   | :---  | :---  |
   | Number of MFA denials to trigger account lockout | 3 |
   | Minutes until account lockout counter is reset | 180 |
   | Minutes until account is automatically unblocked | 15 |

1. Select the **Save** option at the top of your screen.
1. Review some of the other configuration options you have on MFA like:

   - Fraud alert
   - Block / unblock users
   - Notifications
