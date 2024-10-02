# Chemical Supplies Management System

## Project Overview

This project is a chemical supplies management system that allows users to add, edit, delete, and paginate data about chemical supplies. It offers a user-friendly interface for managing chemical inventory, including vendor information, chemical properties like density and viscosity, and packaging details.

The data is stored in a table format and provides options to save the table, edit entries directly, and delete selected rows. 

---

## Design Approach

The project is designed with a focus on **simplicity**, **modularity**, and **usability**. The following key design principles were considered:

### 1. **Modularity**
   - The core features (add, edit, delete) are handled through separate event listeners and functions to make the code easier to understand and maintain.
   - The logic for editing and deleting rows is encapsulated in functions that handle specific actions based on user interaction with the table.

### 2. **Simplicity**
   - The table data is stored in a JavaScript array (`tableData`), making it easy to manipulate and update.
   - Form inputs for adding or editing data correspond directly to table columns, making it intuitive for users to modify the table.

### 3. **Performance**
   - DOM manipulations are kept to a minimum. When a row is added, edited, or deleted, only the necessary parts of the DOM are updated rather than redrawing the entire table.
---

## Technology Stack

- **HTML5:** Used for the table structure and form elements.
- **CSS3:** Styling the table, form, and buttons.
- **JavaScript:** Handles the core functionalities like saving, editing, deleting, and paginating the data.

---

## Key Features

### 1. **Data Storage**

The data about each chemical supply is stored in an array (`tableData`), where each row represents an object with properties such as Chemical Name, Vendor, Density, Viscosity, Packaging, etc. This array serves as a model for the table displayed in the DOM.

Example of how data is structured in `tableData`:

### 2. Save Feature

When a user adds data through the input fields, it is pushed to tableData and displayed in the table. The save-data event listener triggers the process of saving the table data, converting the input fields into a row in the table, and refreshing the table view.

### 3. Delete Feature

Users can select multiple rows using checkboxes and delete them. This ensures batch deletion is possible without unnecessary complexity.
