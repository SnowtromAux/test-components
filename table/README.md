# Customizable Table Component

## **Overview**
The **Customizable Table Component** is designed for dynamic data representation, providing flexibility in organizing, displaying, and managing information in a structured format. This component supports sortable columns, customizable buttons, pagination, and structured action controls.

---
## **Component Structure**
### **1. Table Layout**
A table is composed of the following sections:

- **`<thead>`**: Defines the column headers.
- **`<tbody>`**: Contains the dynamic row data.
- **Pagination Controls**: Allows users to navigate between pages of table data.

#### **Example Table Structure:**
```html
<table class="data-table">
    <thead>
        <tr>
            <th class="narrow-column">#</th>
            <th>Name</th>
            <th>Created Date</th>
            <th class="narrow-column">Actions</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="narrow-column number-cell" data-number="1"></td>
            <td>Admin</td>
            <td>01-05-2023 14:30</td>
            <td class="text-right">
                <div class="action-buttons">
                    <a href="#" class="btn btn-small btn-primary">Edit</a>
                    <a href="#" class="btn btn-small btn-info">Show</a>
                    <button class="btn btn-small btn-danger">Delete</button>
                </div>
            </td>
        </tr>
    </tbody>
</table>
```

---
## **Customization Options**
### **1. Adding More Columns**
To extend the table with additional columns:
- Modify the `<thead>` section to include new headers.
- Adjust the `<tbody>` rows to match the additional data fields.

#### **Example:**
```html
<thead>
    <tr>
        <th>#</th>
        <th>Name</th>
        <th>Email</th>
        <th>Created Date</th>
        <th>Actions</th>
    </tr>
</thead>
```

### **2. Adjusting Pagination**
Pagination helps users navigate through large datasets. To change the **number of pages, rows per page, or navigation controls**, modify the pagination section.

#### **Example Pagination Structure:**
```html
<div class="pagination-container">
    <div class="pagination-info">
        Showing <span class="highlight">1</span> to <span class="highlight">10</span> of <span class="highlight">1000</span> results
    </div>
    <ul class="pagination">
        <li class="pagination-item disabled"><span class="pagination-link">‹</span></li>
        <li class="pagination-item active"><a class="pagination-link" href="#">1</a></li>
        <li class="pagination-item"><a class="pagination-link" href="#">2</a></li>
        <li class="pagination-item ellipsis"><span class="pagination-link">...</span></li>
        <li class="pagination-item"><a class="pagination-link" href="#">100</a></li>
        <li class="pagination-item"><a class="pagination-link" href="#">›</a></li>
    </ul>
</div>
```

### **Modifying Pagination Settings:**
- **Change Rows per Page**: Adjust how many rows are displayed per page by modifying the backend logic or JavaScript.
- **Customize Page Numbers**: Modify the pagination items to show different page numbers dynamically.
- **Enable/Disable Navigation Controls**: Hide or disable "Previous" and "Next" buttons when applicable.

### **3. Disabling Buttons**
To disable a button, simply add `disabled` to the button tag.

#### **Example:**
```html
<button class="btn btn-small btn-danger" disabled>Delete</button>
```

### **4. Adding Icons to Buttons**
For enhanced user interaction, use icons in buttons. TailwindCSS or Font Awesome icons can be integrated.

---
## **Best Practices**
- **Follow Strict Class Naming:** Maintain the predefined class names for consistency.
- **Use Proper Data Formatting:** Ensure dates and numbers are formatted correctly for readability.