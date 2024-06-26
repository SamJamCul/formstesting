#   Group Admin journey

## Status

- Date created: *2024-05-03*
- Developed 

## Contents
- [As is](#as-is)
- [To be](#to-be)
- [Key decisions](#key-decisions)
- [Designs](#designs)

## As is 
- Currently, any user with a trial account can create a form
- Once a user's trial account is ugraded to an editors account, they can make the form live
- Departments don't have a way to control who creates and makes forms live
- When upgrading a trial account, a member of the GOV.UK Forms adoption team manually adds the user's name and organisation details and changes their role from trial to editor.

## To-be
Group admin journey enables group admins to: 
- Create groups
- Request groups to be made active
- Make forms live after a group is upgraded to an active active
- Add editors to their group

## Key decisions
- We decided to make the MVP version of this journey so we enable departments have control over their forms and learn more from the users.

**Select an organisation**
- Created an extra html page and  made it necessary for all users to select their organization after they logged in the Forms service. This helps the adoption team see if their department has an MOU. This process is only done once when the users signs in for the first time.
- We are using autofill feature with the search functionality. 
- Dev & Design team decided not to validate email addresses against name and organisation for this mvp.
- Added a details component to explain users what to expect if their organisation is not listed on the org list. This was done to help reduce support tickets.
- We decided to ask for the organisation first to avoid users who can't use Forms yet. 

**Enter your full name**
- Created an extra a page and made it necessary for all users to fill in their name, so that we update our records about the user and the adoption team can check if an MOU is in palce.

**Groups landing page**
- Create an page for users to see groups they are part of while allowing them to create their own groups. We decided that whoever creates a group becomes a group admin and can only publish forms if they have their form upgraded by an organisation admin.

**Groups landing page with an upgrade request**
- Added an extra line for upgrade request so the users can see which groups have requested to upgrade.

 **Create a new group**
- Added a HTML page for users to create their group.

 **Group landing page with a form** 
- Added a HTML page to display forms in a group.
- Added a link to change the name of this group
- Added a link to edit members of this group

 **View or edit members of this group**
- Added a HTML page to show a list of users.
- Added a green primary button to add an editor
- Added a gray secondary button to remove editors
- Added a details component to explain the difference between 'editor' and 'group admin' roles. 

 **Request to upgrade a group**
- Added a HTML page to show how users can upgrade their group.

 **What happens next page**
- Added a HTML page with a success banner to show that users have requested to ugprade their group.

 **Group page for active group**
- Changing "trial" caption to "active".

 **Add an editor or group admin**
- Added a HTML page for group admins to add other members to their group.

 **Task list page-trial group**
- Using the same task list page and only changing the content for Make your form live.

 **Task list page-active group**
- Using the same task list page and only changing the back link to "back to <name of group> ".

  
## Designs
- [Figma files for designs can be found here](https://www.figma.com/file/D2DtaS68qRvVZgtxaBQNjd/User-management---moving-to-a-'group'-model-for-public-beta?type=design&node-id=124%3A7025&mode=design&t=oXGvFNLZw5ETbTzV-1")
- [Protoype can be found here](https://forms-prototypes-pr-201.herokuapp.com/product-pages)
<br>

### Select an organisation 
![Select an organisation](/design/features/user-management/screenshots-v1/group-admin-screenshots/001-selectorganisation.png)
*This shows the ‘Select an organisation’ page with the new guidance section that says "Currently, GOV.UK Forms is only available for central government organisations that publish content on the GOV.UK website." It then asks user to select the organisation they work in, this is followed by a green, primary “Save and continue” button. Underneath the primary button there's a details component with a title "if your organisation is not listed" and a body text "If you’re from a central government organisation that publishes content on the GOV.UK website but your organisation is not listed, please contact the GOV.UK Forms team.If you’re from a public sector organisation that does not publish content on GOV.UK you cannot use GOV.UK Forms yet. You can read about our forthcoming features and sign up to our mailing list for updates.*

Once users select the organisation they are in, they are taken to Enter your full name page. 

If users don't select an organisation, we prevent them from moving forward and show the following error messaging: "There's a problem, select your organisation"

### Enter your full name
![Enter your full name](/design/features/user-management/screenshots-v1/group-admin-screenshots/002-enteryourfullname.png)
*This shows the ‘Enter your full name’ page and asks user to input their name and surname. It's then followed by green, primary button that says "Save and Continue"* 

Once user clicks "Save and continue" they are taken to groups landing page. 

### Groups landing page
![Your group](/design/features/user-management/screenshots-v1/group-admin-screenshots/003-yourgroup.png)
An example of a your group page. It shows:
- Active groups
- Trial groups
- Create a group primary button
- What is a 'group' detailed component with a text that says:

*Each form is created inside a group. People can be added to a group to create and edit forms in it. If you need access to an existing form or group, ask someone who has access to that group to add you. When a group is first created it will be a ‘trial’ group. That means you cannot make any forms in the group live. You can request for a group to be upgraded to an ‘active’ group if you need to make forms live. If you’re not sure if you should make a new group, speak with your organisation’s GOV.UK publishing team.*

Once 'create a group' is selected, a user is taken to create a new group page. 

### Groups landing page (with request)
![Your group (with request)](/design/features/user-management/screenshots-v1/group-admin-screenshots/003-yourgroupswithrequests.png)
An example of your group page with a request. 

### Create a new group
![Create a new group](/design/features/user-management/screenshots-v1/group-admin-screenshots/004-createanewgroup.png)
*This shows the ‘Create a new group’ page. It asks users to enter a name for their group. It is then followed by primary button that says "Save and continue".*

Once a user clicks the button they are taken to group page. 

### Group page
![Group landing page](/design/features/user-management/screenshots-v1/group-admin-screenshots/005-grouplandingpagefortrialgroup2.png)
This shows the forms landing page where a group admin can see all the forms inside this group.  

### Members of this group
![Members of this page](/design/features/user-management/screenshots-v1/group-admin-screenshots/006-membersofthisgroup.png)
This shows the a list of members in a group with a functionality of removing or adding members to this group. 

Once a user clicks 'add an editor'. They are taken to add another member page. 

### Add another member to the group
![Add another member to the group](/design/features/user-management/screenshots-v1/group-admin-screenshots/009-addaneditororgroupadmin.png)
This shows the ‘Add another member to the group’ page and asks user to input email of the user they want to add to this group.

### Request to upgrade
![Upgrade request](/design/features/user-management/screenshots-v1/group-admin-screenshots/007-upgraderequest1.png) 
This shows the request to upgrade page where group admin can request to make their from live. 

Once they click 'send request to upgrade' button they are taken to what happens next page. 

### What happens next page
![Upgrade request](/design/features/user-management/screenshots-v1/group-admin-screenshots/007-Upgraderequest.png) 
This shows the 'what happens next page' where user is informed about the next steps and are given the option to go back to forms landing page. 

### Active group
![Active group](/design/features/user-management/screenshots-v1/group-admin-screenshots/008-activegroup.png)
An example of an active group. 

### Task list page - trial
![Task list page](/design/features/user-management/screenshots-v1/group-admin-screenshots/010-tasklistpage-trial.png)
*Example of a task list page for a trial group with content changed for "Make your form live" section. Changed content is as follows "You cannot make this form live because it’s in a ‘trial’ group. Find out how to upgrade the group so you can make forms live.*

### Task list page - active
![Task list page](/design/features/user-management/screenshots-v1/group-admin-screenshots/010-tasklistpage-active.png)
Example of a task list page for an active group.
