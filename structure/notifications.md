# PLM Notification Recipients

PLM Notification Recipients define who should receive alerts when an activity is about to start, has started, is overdue, or needs attention. Recipients can represent internal users, departments, external vendor contacts, or groups of people. These recipients are added to activities in PLM Templates and Plans, and help ensure the right people are informed on time.

---

## Accessing Notification Recipients

Search for **PLM Notification Recipients** in the *Tell Me* search bar in Business Central.

---

## Recipient Types

Recipients are either:

• **Person**  
An individual contact, internal or external.

• **Group**  
A collection of people, such as a team or department. A Group must contain at least one Person to receive notification emails.

You can also assign external people, like vendor or manufacturer contacts, by adding them as a Person and filling their name and email address. They can also be included in Groups. As long as the email is filled, they will receive notifications and can be assigned to tasks just like internal users.

---

## Field Overview

![PLM Activity Group card](/assets/images/notification_recipients_list.png)

### Code  
This is the unique identifier for the recipient or group. It can be a short code like DESIGN, PURCHASE, or a person's name. This code is used throughout templates and plans when assigning responsibility or notifications.

### Description  
The name of the recipient or group. This could be a full name of the person, a team name like “Design Department,” or something more descriptive. It’s shown in the plan lines and helps make assignments more readable.

### Type  
Defines whether the recipient is a Person or a Group. Use Person for individuals, either internal users or external contacts, and Group for departments or teams. External people are also created as Person type.

### Email Address  
The email used to send notifications. This must be filled if you want the recipient to receive alerts. If left blank, the system won’t send emails. You can use any valid email address, including external ones.

### Manager Code  
Optional field for reporting or grouping in the PLM Worksheet. You can use it to group recipients under a team lead or manager. This gives more flexibility when filtering or summarizing responsibilities.

### No. of Members  
Only shown when the recipient type is Group. Indicates how many people are assigned to the group. You can click on this to drill down and manage group members. Each member will receive notifications when the group is assigned.

---

## Business Central User Setup

To connect PLM recipients to Business Central users, a new field has been added to the **User Setup** page.

![PLM Activity Group card](/assets/images/bc_user_setup.png)

### Responsible for PLM actions  
This field allows you to link a user to a PLM Notification Recipient Code. When filled, it ensures that:

• The user will only see their assigned tasks in the PLM Worksheet or related filtered pages.  
• The system knows which user is responsible for PLM related activities.

This setup supports task visibility and simplifies user specific filtering without needing extra configuration in the PLM recipient cards.

---

## Where Recipients Are Used

Recipients can be assigned at different levels within a PLM Template or Plan.

• **Phase**  
When a recipient is added at phase level, it is automatically copied to all activity groups and activities within that phase.

• **Activity Group**  
Recipients added here will be inherited by all activities within the group.

• **Activity**  
Recipients can be entered directly per activity, giving full flexibility.

When the Responsible code is filled on a template or plan line, the system will automatically assign the recipient or recipients linked to that person or group. This helps ensure that the right contacts are set up quickly.

Additional recipients can be added manually on any plan or template line by clicking on the **No. of Recipient Lines** field. This opens the full list of notification recipients for that task, allowing you to fine tune who gets notified and when. Each activity can have multiple recipients, each with their own notification triggers.

---

## PLM Notification Triggers

Triggers define when a recipient receives a notification. For each recipient, you can set:

• **Before Start**  
Alert sent a number of days before the planned start date.

• **After Start**  
Notification sent after the planned start date.

• **Before Deadline**  
Notification sent before the planned ending date.

• **After Deadline**  
Reminder sent a number of days after the planned ending date.

Each trigger can be set per recipient line. This allows flexibility in how and when each person is informed. Notifications are calculated based on the dates and calendar logic in the PLM Plan.

---

## Email Integration

Notification emails are sent via standard Business Central email setup. Recipients must have a valid email address on the recipient card. No additional configuration is needed beyond standard email setup in Business Central.

![PLM Activity Group card](/assets/images/setup_email.png)
---

## Best Practices

• Use generic codes for departments or teams, for example DESIGN or SOURCING.  
• Assign a Manager Code to group related recipients for reporting or filtering in the PLM Worksheet.  
• Make sure to link valid email addresses.  
• Keep recipient information updated to avoid sending emails to the wrong address.
