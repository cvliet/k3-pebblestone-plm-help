# PLM Templates

PLM Templates are predefined planning structures used to standardize the workflow of product development across collections and seasons. A template contains a full planning layout, including phases, activity groups, and activities, each with durations, optional color tracking, recipients, and item phases.

Once certified, a template can be used to create PLM Plans, which inherit the structure and allow you to execute the planning cycle. Templates are designed for reuse and consistency and support faster, standardized plan creation across departments and teams.

---

## Accessing PLM Templates

Open the **PLM Templates** page using the *Tell Me* search in Business Central. From here, you can create, edit, or certify templates.

---

## Understanding the PLM Template Header

This section explains the fields in the PLM Template header. These fields define the basic setup of a template and help control how new PLM Plans are created. They include general information like description and duration, as well as settings for calendar, plan numbering, and certification status.

![PLM Activity Group card](/assets/images/plm_template_header.png)

### No.  
This is the unique identifier for the PLM Template. The value is automatically assigned based on the Template No. Series defined in PLM Setup, unless entered manually when creating the template. It helps to follow a structured format (PLMT-0001) for consistency.

### Description  
A free text field to describe the purpose or contents of the template, such as “Women’s Tops AW26” or “Basic Product Flow.” This description helps users quickly identify the right template when creating new PLM Plans.

### Total Duration  
Shows the sum of all durations from activity lines in the template. This value is a simple total of the planned working-time units entered on each activity (for example 3D, 2W, 1M).  
It does not consider calendars, non-working days, or dependencies. Its purpose is to give a general indication of how long the full sequence of activities would take before real planning dates are calculated in a PLM Plan.

### Plan Number Series  
This optional field allows you to assign a specific number series that will be used when creating PLM Plans from this template. If filled, this overrides the default PLM Plan number series defined in the global PLM Setup. This helps separate plan numbers by product type or department if needed.

### Default Reminder Duration  
This field stores the default reminder settings for task-related notifications. These include when notifications should be sent relative to the planned starting or ending dates (2 days before start, on due date, 1 day after due).  
These values are inherited by recipients linked to the template but can still be changed per recipient or per plan line once the plan is created.

### Default Past Due Duration  
Defines the number of days after a task's planned end date when a recipient should be notified that it’s overdue. This value acts as a fallback setting for all activities in the template.  
When a recipient is added to a plan or template, this value is copied into their notification line but can be changed manually per task or recipient.

This field ensures timely follow-up on missed deadlines and supports automated alerts to keep plans on track.

### Base Calendar Code  
Defines which calendar is used to calculate working days for the PLM Template. This calendar controls which days are treated as non-working, such as weekends and public holidays.  
When you assign a calendar in the template header, that value is automatically applied to all phase, group, and activity lines within the template.  
However, it can be manually changed per line if needed, for example when a task depends on a vendor or manufacturer in a different country with a different working calendar.

> **Note:** If no calendar is filled manually, the value from *Company Information > Shipping tab* is used by default.

### Customized Calendar  
Shows whether the selected base calendar has been customized with manual changes, for example turning public holidays into working days or blocking specific dates for factory closures, local events, or seasonal shutdowns.

If you customize the calendar from the template header, all underlying template lines will also reflect this as a customized calendar.  
However, each individual template line can have its own customized calendar as well. This allows you to adjust working days on a more detailed level, useful when different tasks depend on vendors or teams in different regions.  
You can click into the calendar to view or edit these customizations directly.

### No. of Plans  
Displays the total number of PLM Plans created from this template. This gives an indication of how often the template is used in practice.

### Status  
The status determines how the template can be used:

- **Under Construction:** The template is being built or edited. All fields and structure can be modified.  
- **Certified:** The template is locked for editing and can now be used to generate PLM Plans.  
- **Closed:** The template is no longer in use. It cannot be modified or used to create new plans.

Only Certified templates can be selected during PLM Plan creation. You can switch back from Certified to Under Construction if changes are needed, but this should be done with care.

---

## Template Functions Overview

The PLM Template Card includes several actions across three tabs: **Home**, **Status**, and **Related**. These functions allow you to build, update, and manage your templates effectively.

### Home Tab

- **Increase / Decrease**  
Used to indent or outdent the Description of activities within the template. This is purely visual and helps create logical structure or hierarchy in the template layout. It does not impact planning logic or dependencies.

- **Copy from Template**  
Copies the full structure from another PLM Template, including phases, groups, activities, durations, and recipients. Useful for reusing proven setups across seasons or product categories.

- **Create Plan**  
Generates a new PLM Plan based on the current template. Only available when the template is Certified. The new plan will inherit all structure and settings from the template.

### Status Tab

- **Certify**  
Sets the template to a locked state, ready for use in creating PLM Plans. Once certified, structural edits are blocked.

- **Under Construction**  
Switches the template back to editable mode. Use this if updates are needed. Re-certify before using again.

- **Close**  
Marks the template as closed and read-only. Closed templates cannot be edited or used to create new plans.

### Related Tab

- **Recipients**  
Opens the list of assigned recipients at phase, group, or activity level. These are copied into plans created from this template.

- **Dependencies**  
View task dependencies (predecessors/successors).

- **Comment Sheet**  
Opens a simple notes page linked to the template header. It’s used for general instructions, remarks, or internal comments about the template as a whole.  
> Note: Individual template lines (like activities) have their own comment fields. Those are managed separately.

---

## Understanding PLM Template Lines

The template lines define the structure, duration, and logic of a PLM Template. These lines serve as the blueprint for future PLM Plans. Each line represents either a phase, group, activity, or buffer time.

Lines can be created manually or added in bulk using activity groups. When creating a plan from a template, these lines are copied into the new plan and used to calculate the timeline and structure.

---

### Field Overview (Template Lines)

![PLM Activity Group card](/assets/images/plm_template_lines.png)

**Type**  
Defines the kind of line: Phase, Group, Activity, or Buffer Time. The type controls how the line behaves and what can be linked below it.

**Code**  
The unique code for the line. For phases and groups this can be typed manually. For activity lines, selecting a code will also fill the description, default duration, and Use Color Level.

**Description**  
Describes the task or phase. For activity lines this is filled from the selected activity but can be changed. Use the Increase/Decrease functions to indent lines and bring visual structure.

**Use Color Level**  
Boolean that defines whether execution must happen per color. This is inherited from the activity but can be changed manually on the line. Enables color-level tracking when used in a plan.

**Base Calendar Code**  
Specifies which calendar to use for calculating working days. Inherits from the header by default but can be changed on each line, for example when a task uses a different supplier or country.

**Customized Calendar**  
True if manual changes were made to the base calendar on this line. You can drill down and customize the calendar per task, for example to block out factory closures or local events.

**Duration**  
Defines the number of working days or weeks needed to complete the activity. Default is taken from the activity but is editable. Drives the scheduling when used in a plan.

**Responsible**  
Defines the recipient (person or group) responsible for the task. When filled on a phase or group, this value is inherited by lines below. Can be changed per line if needed.

**Item Phase Code**  
Optional. Triggers a phase update on the linked item when this task is started. Can be set manually or inherited from the group or phase above. Used to move items through the lifecycle.

**No. of Recipient Lines**  
Shows how many recipients are assigned to this line. Inherited from higher levels if set. Click the value to view or change the assigned recipients and their notification settings.

**Dependencies**  
Shows which other activities this line depends on, meaning those must be completed before this task can start.  
Clicking the field opens the Dependency Setup page, where you can define or edit these links.

> Note: The **Related > Dependencies** option in the header only shows an overview of all dependencies in the template, and doesn’t allow editing. Changes must be made from the field on the line itself.

**Comment**  
Shows whether there’s a comment attached to this line. Comments are added per line and not inherited. Click to read or edit the text.
