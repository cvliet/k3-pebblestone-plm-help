# PLM Activities

PLM Activities represent the lowest level in the structure of the PLM module. Activities are the actual tasks that need to be performed, for example: create a tech pack, request a sample or approve a sample. The activities also carry the logic to change the phase of an item, to send notifications, and to track progress of a product.

## Tell Me

To open the list of PLM Activities, use the *Tell Me* function and search for “PLM Activities”.

## Activity List Page

On the activity list page, you can define your available activities. Once an activity is used in a template or plan, it will copy certain values from this list, but not all.

## Fields

**Code**  
The unique identifier for the activity. This can be a short code like DEV01 or FIT02.

**Description**  
The name of the activity.

**Default Duration**  
The number of working days this task is expected to take. This is the suggested duration that will be copied when using this activity in a template or plan. You can override the copied value if needed.

**Use Color Level**  
If enabled, this setting means that the activity needs to be tracked per color. All the available tracking levels are activated: the activity line, item level, and color level. This is useful for activities like approving a sample per color. If disabled, the activity can be marked as completed for all colors at once.

## Behavior

When an activity is inserted into a template or a plan, the following values are copied:

• Code  
• Description  
• Default Duration  
• Use Color Level  

These values can be overwritten, as long as the plan is still in status “New” or “Under Construction”.

The following values are **not** copied when inserting an activity into a template or plan:

• Responsible Code  
• Item Phase Code  
• Notification Recipients  

These fields must be manually entered per template line or plan line.

## Use Color Level

When *Use Color Level* is enabled, the activity needs to be completed for all item colors individually. The status of the activity line, item, and color will be updated as follows:

• When the first color of an item is marked as started, the item and activity line will also be marked as started.  
• When all colors of an item are marked as completed, the item will be marked as completed.  
• When all items and all colors are completed, the activity line will be marked as completed.

This setting is ideal for tasks like sample approvals, where each color might progress at a different pace.

## Best Practices

• Use a short and clear name for the activity.  
• Use color-level tracking only when it adds value.  
• Be consistent in naming and durations to help with planning and reporting.  
• If multiple tasks share similar names or purposes, use consistent coding for easy grouping and filtering.
