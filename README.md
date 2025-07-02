# Translation Memory Tools

---

| Function                | Description                               |
|------------------------|-------------------------------------------|
| `list_memories`       | List saved translation memories           |
| `create_memory`       | Create a new translation memory           |
| `update_memory`       | Update a memory’s name                    |
| `delete_memory`       | Delete a translation memory               |
| `add_translation`     | Add a translation unit to a memory        |
| `delete_translation`  | Remove a translation unit from a memory   |
| `import_tmx`          | Import a TMX file into a memory           |
| `check_import_status` | Check TMX import status                   |

---













# Salesforce Integration Functions

---

| Function                         | Description                                                                                                             |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| `salesforce_search_objects`      | Search for standard and custom objects using partial name matches. Finds both standard and custom objects. <br>**Example**: “Find objects related to Account” will find `Account`, `AccountHistory`, etc. |
| `salesforce_describe_object`     | Get detailed object schema information including field definitions, relationship details, and picklist values. <br>**Example**: “Show me all fields in the Account object” |
| `salesforce_query_records`       | Query records with support for parent-to-child and child-to-parent relationships. Supports complex WHERE conditions. <br>**Note**: For GROUP BY or aggregate queries, use `salesforce_aggregate_query`. <br>**Example**: “Get all Accounts with their related Contacts” |
| `salesforce_aggregate_query`     | Execute aggregate queries with `GROUP BY`, `HAVING`, and functions such as `COUNT`, `COUNT_DISTINCT`, `SUM`, `AVG`, `MIN`, `MAX`. Supports date/time grouping. <br>**Example**: “Count opportunities by stage” or “Find accounts with more than 10 opportunities” |
| `salesforce_dml_records`         | Perform data operations like inserting new records, updating existing ones, deleting records, or upserting using external IDs. <br>**Example**: “Update status of multiple accounts” |
| `salesforce_manage_object`       | Create and modify custom objects. Includes creating objects, updating object properties, and configuring sharing settings. <br>**Example**: “Create a Customer Feedback object” |
| `salesforce_manage_field`        | Manage object fields: add new custom fields, modify properties, and define relationships. Automatically grants Field Level Security to System Administrator unless specified via `grantAccessTo`. <br>**Example**: “Add a Rating picklist field to Account” |
| `salesforce_manage_field_permissions` | Manage Field Level Security (FLS): grant or revoke read/edit access for specific profiles, view current permissions, and bulk update permissions. <br>**Example**: “Grant System Administrator access to Custom_Field__c on Account” |
| `salesforce_search_all`          | Search across multiple objects using SOSL. Supports multiple object types and provides field-level snippets in the results. <br>**Example**: “Search for 'cloud' across Accounts and Opportunities” |
| `salesforce_read_apex`           | Read Apex classes: view full source code, list classes by name patterns, and get metadata such as API version and status. Supports wildcards (`*` and `?`). <br>**Example**: “Show me the AccountController class” or “Find all classes matching AccountCont” |
| `salesforce_write_apex`          | Create or update Apex classes, specify API versions, and manage class implementations for business logic. <br>**Example**: “Create a new Apex class for handling account operations” |
| `salesforce_read_apex_trigger`   | Read Apex triggers: get source code, list triggers by name, and view metadata including object, status, and API version. Wildcard search supported. <br>**Example**: “Show me the AccountTrigger” or “Find all triggers for Contact object” |
| `salesforce_write_apex_trigger`  | Create or update Apex triggers for specific objects. Define trigger events and specify API versions. <br>**Example**: “Create a new trigger for the Account object” or “Update the Lead trigger” |
| `salesforce_execute_anonymous`   | Run anonymous Apex code without saving it as a class. Useful for ad-hoc operations or script-based updates. Includes execution result and debug logs. <br>**Example**: “Execute Apex code to calculate account metrics” or “Run a script to update related records” |
| `salesforce_manage_debug_logs`   | Manage debug logs: enable or disable logs for specific users, configure log levels (NONE, ERROR, WARN, INFO, DEBUG, FINE, FINER, FINEST), and retrieve logs. <br>**Example**: “Enable debug logs for user@example.com” or “Retrieve recent logs for an admin user” |

---
