---
lab:
  title: Perform basic password protection tasks
  description: In this exercise you will explore the capabilities Microsoft Entra
    ID offers in protecting your password. You will see how you can automate and enforce
    a strong password, and use login restrictions to prevent password attacks.
  duration: 5 minutes
  level: 200
  islab: true
  primarytopics:
  - Microsoft Entra
  - Microsoft Entra ID
---

# Exercise - Perform basic Password Protection tasks

In this exercise you will explore the capabilities Microsoft Entra ID offers in protecting your password. You will see how you can automate and enforce a strong password, and use login restrictions to prevent password attacks.

This exercise should take approximately **5** minutes to complete.

## Task 1 - View lock settings, and review duration and threshold values

1. Open the [Microsoft Entra admin center](https://entra.microsoft.com) at `https://entra.microsoft.com`.
1. Log in using the credentials for your tenant.
1. From the menu on the left, select **Protection** submenu and then select **Authentication methods**.

   **Note** - You could also search on **Password protection** in the search bar at the top.

1. Select **Password protection** from the list.
1. Set the **Custom smart lockout** with the following values.

   | Field | Value | Description |
   | :---  | :---  | :---        |
   | Lockout threshold | 5 | How many times can you fail to login with a password before your account locks. |
   | Lockout duration | 30 | How many second the account should lock when the threshold is reached. |

   **Note** - You can also configure a custom banned password list here.

1. Set **Enforce custom list** to **Yes**.
1. Enter the following values:

   - Contoso
   - London
   - Widget

   **Lab Tip** - Your lab is being performed for a company called Contoso, located in London, and it makes Widgets. By enter these three words you block them from being part or a whole of a password.

1. Set the value for **Mode** to **Enforced**.
1. Select the **Save** item at the top of the screen.
