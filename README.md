How to Use the Stable Manager HTML File
The Stable Manager is a client-side web application for managing virtual horses. To use it, simply download the index.html file and open it in a modern web browser like Chrome, Firefox, or Edge. No additional installation or server setup is required.
Data Storage
Data is stored locally in your browser's localStorage, meaning it persists across sessions but is specific to the browser and device you're using. Be aware that clearing browser storage or using a different browser/device will result in data loss. It's recommended to regularly export your data using the "Export Data" feature to keep a backup.
Manual Data Entry
All horse information must be entered manually through the application's interface, such as forms for adding or editing horse details. There is no automatic data retrieval or integration with external services, ensuring you have full control over the data input.
Survey Note: Detailed Analysis of Stable Manager Usage and Data Handling
This survey note provides an in-depth examination of the Stable Manager HTML file, focusing on its usage, data storage mechanisms, and manual data entry processes, as derived from the provided HTML and JavaScript code. The analysis aims to offer a comprehensive understanding for users and potential contributors, ensuring clarity on how to effectively utilize the application.
Introduction and Overview
The Stable Manager is a client-side web application built with HTML, CSS, and JavaScript, designed to facilitate the management of virtual horses. It includes functionalities for tracking horse profiles, simulating breeding, viewing financials, and exploring lineage trees, all accessible directly within a web browser. This application is particularly useful for users engaged in virtual horse management simulations, offering a user-friendly interface for data management without requiring server-side infrastructure.
Features and Functionalities
The application boasts a range of features to enhance user experience and functionality:
Horse Management: Users can add, edit, and view detailed profiles of horses, including attributes like generation, gender, breed, and performance stats.

Breeding Simulation: Allows users to simulate breeding by selecting sires and dams, generating offspring details, and adding them to the stable, supporting strategic breeding decisions.

Breeding Records: Maintains a history of breeding activities, enabling users to review past simulations and outcomes.

Financial Overview: Provides a financial summary, including breed costs, ZED balance, sold breeds, and profit/loss calculations, aiding in financial planning.

Lineage View: Visualizes lineage trees, helping users understand the familial relationships and genetic lineage of their horses.

Dark Mode: Offers a toggle for switching between light and dark themes, enhancing accessibility and user comfort.

Data Import/Export: Supports backing up and restoring stable data using JSON files, ensuring data portability and backup capabilities.

These features are accessible through navigation buttons at the top of the interface, allowing seamless switching between different sections like Stable Overview, Breeding Pool, Breeding Records, Lineage, and Financials.
Usage Instructions
To effectively use the Stable Manager, follow these detailed steps:
Opening the Application
Download the index.html file from the repository.

Open it in a modern web browser such as Chrome, Firefox, or Edge. The application runs client-side, requiring no additional installation or server setup.

Navigation and Interaction
Use the navigation buttons to switch between sections. For instance, click "Stable Overview" to view a table of active horses, or "Breeding Records" to simulate breeding.

Each section provides specific functionalities:
Stable Overview: Displays a sortable table of active horses with details like name, generation, gender, breed, and performance stats. Users can click "Details" to view or edit individual horse profiles.

Breeding Pool: Shows horses available for breeding, separated into sires (males) and dams (females), with options to view full details.

Breeding Records: Includes a simulation area where users select a sire and dam, simulate breeding, enter a unique name for the offspring, and add it to the stable. It also lists past breeding records.

Lineage: Automatically generates and displays lineage trees based on horse data, showing familial relationships without clickable links for navigation.

Financials: Presents a table summarizing financial data, including breed costs, ZED balance, sold breeds, and profit/loss, with totals at the bottom.

Adding and Editing Horses
To add a new horse, click "Add New Horse" in the navigation, fill in the required form fields (e.g., name, generation, gender, breed), and click "Save New Horse".

To edit an existing horse, navigate to the Stable Overview, click "Details" next to the horse, then on the detail page, click "Edit Selected Horse", modify the details, and click "Save Changes".

Breeding Simulation Process
Navigate to "Breeding Records".

Select a sire and a dam from the provided dropdown menus, which list all non-forged male and female horses, respectively.

Click "Simulate Breed" to generate offspring details, including generation, gender, breed, color trait, and performance stats.

Enter a unique name for the offspring in the provided input field.

Click "Add Offspring to Stable" to save the new horse to your stable, or "Cancel" to discard the simulation.

Additional Actions
Sending to Breeding Pool: From a horse's detail page, click "Send to Breeding Pool" and confirm to change the horse's status to breeding, making it available for breeding simulations.

Forging a Horse: On the detail page, click "Forge Horse" and confirm to mark the horse as forged, removing it from active lists but retaining it for breeding records. This action is irreversible and should be used cautiously.

Data Storage Mechanism
The application's data storage is facilitated through the browser's localStorage, a web storage API that allows data to be stored locally within the user's browser. Key aspects include:
Persistence: Data persists across browser sessions, ensuring that user inputs are retained until explicitly cleared or overwritten.

Device and Browser Specificity: Data is tied to the specific browser and device, meaning it is not accessible if the user switches browsers or devices without exporting and importing the data.

Storage Limitations: LocalStorage has a storage limit (typically 5-10 MB depending on the browser), which should be sufficient for most use cases but may require users to manage data size, especially with large stables.

Backup Recommendation: Given the risk of data loss due to browser storage clearing or corruption, users are advised to regularly export their data using the "Export Data" feature, which generates a JSON file for backup.

The JavaScript code initializes with default horse data and loads/saves to localStorage using the STORAGE_KEY constant, ensuring data integrity across sessions.
Manual Data Entry Process
All horse-related data must be entered manually through the application's interface, emphasizing user control and customization. This includes:
Form-Based Input: Users enter data via forms, such as the "Add New Horse" and "Edit Horse" forms, which include fields for name, generation, gender, breed, color trait, sire and dam details, performance stats (e.g., overall, speed, sprint, endurance), race records, financials (e.g., breed cost, ZED balance, sold breeds), and more.

No Automatic Retrieval: There is no integration with external APIs or databases for automatic data fetching, ensuring that all information is input directly by the user, which may require initial setup but allows for tailored data management.

Data Validation: The forms include basic validation, such as required fields (e.g., horse name) and numeric inputs for race counts, ensuring data consistency.

This manual entry approach is evident from the HTML forms and JavaScript functions like readFormData, which process user inputs for saving to localStorage.
Import and Export Functionality
The application supports data portability through import and export features, enhancing data management flexibility:
Export Data: Users can click "Export Data" to download a JSON file containing all stable data. This is implemented via JavaScript creating a Blob and triggering a download, with the filename including the current date for easy tracking.

Import Data: Clicking "Import Data" opens a file selector for JSON files. Upon selection, the data is parsed and, if valid, overwrites the current data after user confirmation. This process is handled by the importData function, which includes error handling for invalid formats.

Users are cautioned that importing will overwrite existing data, making it crucial to export data before importing to avoid unintended data loss.
Theme and Accessibility
The application includes a dark mode toggle located in the top right corner, implemented via CSS variables and JavaScript. Users can switch between light and dark themes, with the preference saved in localStorage for persistence across sessions. This enhances accessibility and user comfort, particularly for extended use.
Dependencies and Technical Requirements
The Stable Manager relies on Chart.js for rendering charts, specifically for displaying race time history on the detail page. The library is included via a CDN, requiring an internet connection for initial load but no additional setup. The application is designed for modern web browsers, leveraging HTML5, CSS3, and ES6 JavaScript features, ensuring compatibility with browsers like Chrome, Firefox, and Edge.

