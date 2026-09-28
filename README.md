# fitness-tracker-design
Fitness Tracker Pseudocode and Flowchart and IPO Chart

**Course:** ITP 100 Software Design and Logic  
**Author:** Raheem Reid  
**Deliverable:** Algorithm Design (IPO, Flowchart, Pseudocode)  

## 1. Problem Description and Scope  
* **Problem:** Students need a command-line interface to track daily cardiovascular and strength exercise durations, validate that inputs are realistic, and review their progress toward a weekly target of 120 minutes.  
* **Scope:**  
  * Features a continuous main loop with 2 hierarchical submenus (Cardio and Strength).  
  * Validates menu bounds (rejects values outside menu options) and duration inputs (rejects negative numbers).  
  * Aggregates total minutes in memory during execution and outputs a progress summary on demand.  
  * Terminates cleanly when the user selects the Exit option.
## 2. IPO Chart (Input - Process - Output)  
| Input | Processing | Output |
| :--- | :--- | :--- |
| `main_choice` (Integer: 1–4)<br>`sub_choice` (Integer: 1–3)<br>`duration` (Real/Integer: ≥ 0) | 1. Initialize `total_cardio = 0` and `total_strength = 0`.<br>2. Display the main menu in a loop until the user enters `4`.<br>3. Validate that `main_choice` is between 1 and 4.<br>4. If `main_choice` is `1` (Cardio) or `2` (Strength):<br>&emsp;a. Display the appropriate submenu.<br>&emsp;b. Validate that `sub_choice` is between 1 and 3.<br>&emsp;c. Prompt for `duration` and loop until `duration >= 0`.<br>&emsp;d. Map the selected choice to an activity name.<br>&emsp;e. Add `duration` to the appropriate running total.<br>5. If `main_choice` is `3` (Summary):<br>&emsp;a. Calculate `total_active = total_cardio + total_strength`.<br>&emsp;b. Determine goal achievement status (`>= 120` minutes).<br>&emsp;c. Display the formatted summary report.<br>6. If `main_choice` is `4` (Exit), display the farewell message and terminate the program. | Invalid input warning messages<br>Success confirmation showing the logged activity and minutes<br>Formatted Activity Summary:<br>&emsp;• Total Cardio Minutes<br>&emsp;• Total Strength Minutes<br>&emsp;• Total Active Minutes<br>&emsp;• Weekly Goal Status Message<br>Exit Farewell Message |
