---
lab:
  title: Perform basic User Management tasks
  description: In this exercise you will explore the beginner tasks of an Identity and Access administrator by creating and managing a user in Microsoft Entra ID. There are five common activities you will perform in your lab from creating a new user to assigning them roles and licenses.
  duration: 10 minutes
  level: 100
  islab: true
  primarytopics:
    - Microsoft Entra
    - Microsoft Entra ID
---

# Exercise - Perform basic User Management tasks

In this exercise you will explore the beginner tasks of an Identity and Access administrator by creating and managing a user in Microsoft Entra ID.  There are five common activities you will perform in your lab from creating a new user to assigning them roles and licenses.

This exercise should take approximately **10** minutes to complete.

## Task 1 - Create a new user

1. Open the [Microsoft Entra admin center](https://entra.microsoft.com) at `https://entra.microsoft.com`.
1. Log in using the credentials for your tenant.
1. From the menu on the left, select **User** and then **All users**.
1. Select **+ New user** and then pick the **Create new user** option.
1. Enter the requested information:

   | Field | Value |
   | :---  | :---  |
   | User principal name | BhogeswarK |
   | Display name | Bhogeswar Kalita |

1. Leave the **Mail nickname** as is.
1. Make a copy of the **Password** (auto-generated) and store it in **Notepad**.  You will need it later.
1. Leave Accounted enabled checked.
1. Select the Properties tab.
1. Set the values for first and last name:

   | Field | Value |
   | :---  | :---  |
   | First name | Bhogeswar |
   | Last name | Kalita |

1. Note that you can set the **User type** to **Member**. If you pick Guest, it will restrict the users capabilities.
1. Scroll down to the bottom of the page.
1. Set the **Usage location** to **United States** or to whatever region you are in.
1. Select the **Review + create** button.
1. Select **Create**.

### Subtask 1 - Log in to confirm user

1. Open an InPrivate browsing window.
1. Connect to the [Microsoft Entra admin center](https://entra.microsoft.com) at the link `https://entra.microsoft.com`.
1. Enter the username and password you just created.

   | Field | Value |
   | :---  | :---  |
   | Username | BhogeswarK@`your tenant name`.onmicrosoft.com |
   | Password | `Auto generated password you saved` |

1. If prompted follow the on-screen instructions to complete MFA setup.
1. Feel free to explore the Microsoft Entra admin center for a minute.
1. Close the InPrivate browsing window.

## Task 2 - Add a license to the user

1. Open a new tab in your browser.
1. Connect to the [Microsoft 365 admin center](https://admin.microsoft.com) at `https://admin.microsoft.com`.
1. If prompted, log in using the credentials for your tenant.
1. Find the menu on the left side of the screen.
1. Open the **Billing** item in the menu.
1. Select **Licenses** from the list.
1. When the list of licenses appears, select **Microsoft Power Automate Free**.
1. Select the **+ Assign licenses** item.
1. Choose **Brogeswar** from the list (user created in previous task).
1. Select the **Assign** button at the bottom of the page.
1. Notice the message that you have successfully assigned a license.
1. Close the tab with **Microsoft 365 admin center**.

## Task 3 - Invite an external user to your tenant

1. If not already open - Open a browser and connect to the [Microsoft Entra admin center](https://entra.microsoft.com) at `https://entra.microsoft.com`.
1. If prompted, log in using the credentials for your tenant.
1. From the menu on the left, open the **Identity** menu.
1. Select **Users** then select **All users**.
1. At the top of the page select **+ New User**.
1. Choose the option to **Invite external user** from the dropdown.
1. Enter the information for your new external user:

   | Field | Value |
   | :---  | :---  |
   | Email | ExtUser@testemail.com |
   | Display name | External User |
   | Message | Thank you for joining the company for this short work project. We look forward to building this project together. |

1. Select the **Review + Create** button.
1. Select **Create**.

## Task 4 - Assign a role to a user

1. If not already open - Open a browser and connect to the [Microsoft Entra admin center](https://entra.microsoft.com) at `https://entra.microsoft.com`.
1. If prompted, log in using the credentials for your tenant.
1. In the left menu find the **Identity** section. Open it if not already opened.
1. Select **Users** then select **All users**.
1. Choose the user **Bhogeswar Kalita** create in the earlier task.
1. From the newly opened menu select **Assigned roles**.
1. At the top of the screen select **+ Add assignment**.
1. From the **Select role** dropdown menu chose the role **Attribute Definition Reader**.
1. Select the **Next** button when it becomes available.
1. Choose the option **Eligible** for **Assignment type**.
1. Select **Assign**.

### Subtask 1 - Alternate method to assign a role to a user

1. Look at the Identity menu section on the left side of the screen.
1. Select the **Show more** option to see the full **Identity** menu.
1. From the list of items in the **Identity** menu, expand the **Roles & admins** section.
1. Select **Roles & admins**.
1. Select **Attribute Log Reader** from the list of roles.
1. From the top of the screen select **+ Add assignment**.
1. From the **Select member(s)** select the **No member selected** text.
1. From the list of user choose **Bhogeswar Kalita**.
1. Choose the **Select** button at the bottom.
1. Select the **Next** button.
1. On the Add assignments page choose **Active** for the **Assignment type**.
1. Note that you have to enter a justification for this role / user assignment.
1. Enter the justification **User will be working as an Attribute log reader as their primary job.** into the box.
1. Select **Assign**.

## Task 5 - Bulk import users
1. If not already open - Open a browser and connect to the [Microsoft Entra admin center](https://entra.microsoft.com) at `https://entra.microsoft.com`.
1. If prompted, log in using the credentials for your tenant.
1. From the **Identity** menu, select **Users** and then select **All users**.
1. From the top of the page, select the **Bulk operations** drop-down arrow and then select **Bulk create**.

   **Note** - Selecting Bulk create will open a new tile. This tile provides a Download link to a template file that you will edit to populate with your user information and upload to add the bulk creation of users.

1. Select **Download** to see a sample bulk user CSV file.

   **Note** - The .csv template provides you with the fields included with the user profile. This includes the required username, display name, and initial password. You can also complete optional fields, such as Department and Usage location, at this time.  You do not need to fill out all the fields.

   **Lab Tip** - A sample CSV has been provided in the Allfiles/Lab1 folder -- APL0501-BulkUser.csv.

1. Open Notepad.
1. Open the SC300BulkUser.csv file.
1. Search and replace the existing value **<<<enter your domain name>>>** with **Your actual domain name**.
1. Save the file.
1. On the Bulk create users dialog, select the file folder icon on step 3.
1. Path to the Allfiles/Lab1 folder and select **APL0501-BulkUser.csv** file.
1. Select **Open**.
1. Wait for the notification that the file uploaded successfully.  Select the **Submit** button to add the users.

   **Note** - After the users have been created, you will be prompted that the creation has succeeded.

1. **Close** the **Bulk create users** dialog.
1. Check the list of users to see your bulk created users.
