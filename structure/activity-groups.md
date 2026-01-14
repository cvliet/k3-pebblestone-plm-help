# PLM Activity Groups

PLM Activity Groups allow you to bundle related tasks (activities) together to form logical building blocks. These groups simplify the creation of PLM Templates and PLM Plans by reducing repetitive work. Instead of adding each activity manually, you can add a complete group of related tasks in one step.

Activity Groups are typically linked to a specific PLM Phase, though this is not required. You can also add activity groups directly to a plan without assigning a phase. However, using phases improves the plan structure and visibility.

---

## Accessing PLM Activity Groups

Search for **PLM Activity Groups** in the *Tell Me* search bar.

![PLM Activity Group card](/assets/images/activitygroups_list.png)

---

## Field Overview

![PLM Activity Group card](/assets/images/activitygroups_card.png)

### Code / Description  
Defines the ID and name of the group, e.g. `DSN01 – Create initial sketch & mood board`.

### Activities  
Each group contains a list of PLM Activities. These are selected manually when you define the group. However, the activities within a group are automatically **sorted by Activity Code**, not in the order you add them.  
This sorting also applies when the group is used in a PLM Template or PLM Plan.

### Duration  
The default duration is inherited from the linked activity, but you can override it at group level.  
For example, if a "Fit Review" activity normally takes 3 days, you could change it to 1 day for a specific group.

### Use Color Level  
This setting is inherited from the individual activities when you add them to the group, but it can still be changed at the group level.

---

## How Activity Groups Are Used

Activity Groups are used to structure PLM Templates and PLM Plans by grouping related activities together under a single line.  
This improves readability, allows for easier setup, and provides control over shared attributes like color tracking, responsibility, and item phase.

When a group is added to a template or a plan:

• The system copies the group’s description and list of activities.  
• Activities are **sorted by Activity Code**, not by the order they were entered in the group.  
• The *Use Color Level* setting from each activity is also copied into the plan, but you can override it on the group line **before inserting** the group into the template/plan.  
• You can manually change the *Responsible Code* and *Item Phase Code* on the group line:  
  ○ These values will be inherited by all activities within that group when added to the plan.  
  ○ After insertion, individual activity lines can still be modified if needed.

This logic ensures a consistent structure while allowing flexibility during planning and execution.

---

## Best Practices

• **Use groups to structure the plan logically**  
 Group activities by purpose or department (Design, Sampling, Costing). This keeps plans readable and helps with communication.

• **Keep groups reusable**  
 Create generic activity groups that can be used across multiple templates. Don’t hardcode item-specific details.

• **Use the group to control tracking settings**  
 Set *Use Color Level*, *Responsible Code*, and *Item Phase* at group level if the same applies to all tasks. This saves time during plan setup.

• **Avoid unnecessary complexity**  
 Don’t overload a single group with too many unrelated tasks. Break it into multiple smaller groups if the scope becomes unclear.

• **Name clearly**  
 Use clear and consistent naming conventions for groups (e.g. “DES01 – Design Phase 1”).

• **Regularly review activity groups**  
 As your processes evolve, update your groups to stay aligned with how your team works.
