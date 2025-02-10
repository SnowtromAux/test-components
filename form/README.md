# Customizable Form Component

## **Overview**
The **Customizable Form Component** allows users to create and manage entries with different attributes and permissions. The form supports various input types, including text fields, checkboxes, and select dropdowns. Additionally, it provides flexibility in adding buttons at the bottom, which can be enabled or disabled as needed.

---
## **Component Structure**
### **1. Form Container**
The entire form is enclosed within a **form-container**, which consists of:
- **Header Section:** Displays the title (`Create New Entry`) and a **Back** button.
- **Content Section:** Contains the form fields and submission controls.

### **2. Form Elements**
The form consists of three types of elements:

#### **A. Text Fields**
- Used for entering details, such as **entry name**.
- Example:
  ```html
  <input id="name" class="input-field input-field-solid input-field-compact" name="name" type="text" required placeholder="Enter name">
  ```

#### **B. Select Dropdowns**
- Allows users to select predefined options (e.g., color selection).
- Example:
  ```html
  <select id="color" name="color" class="input-field input-field-solid input-field-standard" required>
      <option value="" selected>Select</option>
      <option value="primary">Primary</option>
      <option value="success">Success</option>
  </select>
  ```

#### **C. Checkboxes**
- Used to assign specific permissions.
- Organized into multiple **permission categories**.
- Example:
  ```html
  <label class="permission-option">
      <input type="checkbox" name="permission[1]" value="1"> view-list
  </label>
  ```

---
## **Customization Options**
### **1. Adding More Fields**
- To add more text fields, checkboxes, or select dropdowns, simply copy existing elements and modify their attributes accordingly.

### **2. Adjusting Buttons**
- Buttons at the bottom can be customized:
  - Add **multiple buttons** if needed.
  - Enable or disable buttons dynamically.
  - Example:
    ```html
    <button type="submit" class="button button-primary">Submit</button>
    <button type="button" class="button button-secondary">Cancel</button>
    ```

### **3. Styling**
- The form uses CSS variables for **color**, **spacing**, and **typography**, making it easy to customize.
- Modify `:root` variables to change the look and feel.

---
## **Best Practices**
- **Follow Strict Class Naming:** Maintain the existing class names to ensure consistent styling and functionality.
- **Use Proper Form Validation:** Ensure required fields are properly validated before submission.
- **Keep Permissions Well-Organized:** Use section dividers and logical groupings for checkbox permissions.
