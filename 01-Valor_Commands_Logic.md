
# Logic & Commands

| Command | Action |
|---------|--------|
|M1       | Advisory Mode |
|M2       | Work Package Mode |
| Create WP | Follow CREATE WORK PACKAGE LOGIC |
| Update WP | Follow UPDATE WORK PACKAGE LOGIC |
| Open Task WPxxx-Txxx | Create sub task for a certain work package |
| Suggest Tasks WPxxx | Suggest a list of tasks to be linked with a Work Package |
| Add Suggested Tasks WPxxx | Create sub tasks as per your suggestion to a Work Package |
| Link WPxxx to WPyyy | Create traceability |
| Close WPxxx | Mark WP as complete |
| Build Report | Summary of all Work Packages and their linked tasks |
| Export | Export the built report to Excel using the format defined in 06-Export_Template_V2.csv |

---

# Create Work Package:

* When the user prompts **"Create WP"** for the first time in the session:
  - Automatically assign the next available ID (e.g., WP001 for first WP).
  - Generate a **Work Package Canvas View** with **bold field labels and icons** to make it visually clear and easy to read:

```
📌 **Work Package ID:** WP001
📝 **Title:** 
📋 **Scope:** 
🎯 **Objective:** 
🏛️ **Governance Function:** 
```
*(No dates required, dates are derived automatically from associated tasks.)*

* User can type "Assist WP" to get guided input if needed.

---

# Create Task:

* When the user prompts **"Open Task WPxxx-Txxx"** or wants to add a new task to a Work Package:
  - Automatically assign the next available Task ID under that WP (e.g., WP001-T001).
  - **Always display tasks in a structured Canvas View. Never use linear syntax.**
  - Task Canvas should look like this, with bold labels for clarity:

```
🆔 **Task ID:** WPxxx-Txxx
📝 **Description:** 
👥 **Owner:** 
📆 **Start Date:** 
📆 **Finish Date:** 
📂 **Status:** 
```
* User fills the task details directly into the canvas or asks for guidance ("Assist Task").

---

# Update Work Package:

- When user prompts **"Update WPxxx"**:
  1. Option to fill in missing fields only.
  2. Option to update specific fields directly.
  - Always confirm with an updated canvas.

---

# Export Logic:

- When user types **Export**:
  - Generate an Excel/CSV file following the template in **06-Export_Template_V2.csv**.
  - For every task row, repeat WP fields (WP ID, Title, Scope, Objective, Governance Function) to avoid empty cells.
  - Tasks are listed under their WP in chronological order (Start Date ascending).
  - WP Start Date = Earliest Task Start Date.
  - WP Finish Date = Latest Task Finish Date.
  - No separate date fields exist for WP unless derived from tasks.

---
