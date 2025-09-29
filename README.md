# live-tool-inspection

Room Inspection Application

This document provides a comprehensive overview of the Room Inspection Application, a web-based tool designed to streamline and enhance various types of room and code inspections. The application offers three distinct inspection modes: EA - Inspection (room-by-room), ECS Inspection (room codes with detailed checks), and Room Inspection SE/ST/SV (room numbers with specific SE/ST/SV entries). It features a user-friendly interface, data persistence through local storage, and robust export/import functionalities for inspection data.

Features

The Room Inspection Application is equipped with a suite of features designed to facilitate various inspection processes, ensuring data integrity, ease of use, and comprehensive reporting. The core functionalities are categorized by the three primary inspection types:

1. EA - Inspection (Room-by-Room)

This mode is tailored for general room inspections, allowing users to systematically go through a list of rooms and record observations based on predefined checks. Key features include:

•
Room List Input: Users can input a list of room names or numbers, one per line, into a dedicated text area. This supports manual entry or pasting from external sources.

•
Sequential Navigation: The application guides users through each room in the provided list, allowing them to move to the previous or next room effortlessly.

•
Configurable Checks: For each room, a set of grouped questions and labels are presented. These checks cover various aspects such as personnel working in the room (Bylor, MEH, Other), installed equipment (Walled in eqpt, Other eqpt, SSW, Supports, Pipes, Clumps, Cable trays, Cables, CBS, HVAC/Ducting), support installation status (Not started, Partially installed, Mostly installed, Fully installed), obstructions to MEH work (Hydrodem, Access egress routes, Stored eqpt), and coating status (Floor, Walls, In progress).

•
Binary and Text Input: Most checks are binary (Yes/No), allowing for quick selection. A dedicated 'Comments' section provides a free-form text area for detailed notes.

•
Progress Tracking: A progress bar and numerical indicator show the user's advancement through the list of rooms.

•
Data Export: Inspection results can be exported to a CSV file, with each row representing a room and columns detailing the status of each check and any comments.

2. ECS Inspection (Room Codes with Detailed Checks)

This mode is designed for more granular inspections involving specific room codes and associated detailed checks. It provides an Excel-like interface for managing codes and their statuses.

•
Room Code Input: Users can input room codes, optionally associated with a room name, in a structured format. The application parses these inputs to create a comprehensive list of codes to be inspected.

•
Code-Specific Statuses: Each code can be assigned a status from a predefined list, including options like 'Available', 'No Access', 'Protective Covering', 'Installed', 'PIA Required', 'TCO', 'CBS blocking Installation', 'Equipment Blocking Install', 'Not Verified', 'Material Blocking', 'Not Installed', 'Material Blocking Plate', and 'Unavailable'.

•
Comment Fields: Alongside each code and its status, users can add specific comments in a dedicated text area, allowing for detailed explanations or observations.

•
Excel-like Grid Interface: The inspection interface presents codes, their statuses, and comments in a clear, tabular format, enhancing readability and data entry efficiency.

•
Progress Tracking: Similar to the EA Inspection, this mode also includes progress indicators to show the user's advancement through the list of room codes.

•
Data Export: The results, including room name, code, selected status, and comments, can be exported to a CSV file for further analysis or record-keeping.

3. Room Inspection SE/ST/SV

This specialized mode focuses on capturing specific SE, ST, and SV entries associated with room numbers, particularly useful for detailed inventory or compliance checks.

•
Room Number Input: Users provide a list of room numbers. The application uses the first 6 characters of each room number as a prefix for generating SE/ST/SV codes.

•
Categorized Text Areas: For each room, separate text areas are provided for SE, ST, and SV entries. Users can input multiple codes for each category, one per line.

•
ST Code with Clamp Quantities: The ST entry field supports a specific format where users can enter ST codes along with associated clamp quantities (e.g., STCode-ClampQty). The application intelligently parses and stores these two pieces of information separately.

•
Dynamic Entry Management: The text areas allow for flexible input, and the application dynamically updates the internal state as users type, ensuring real-time data capture.

•
Progress Tracking: Users can navigate through the list of rooms, with progress indicated by a title and progress bar.

•
Data Export: The collected SE, ST, SV codes, along with clamp quantities, are exported to a CSV file. The export format intelligently groups entries by room number and includes the generated prefixes, making it suitable for structured data analysis.

General Features (Applicable to All Modes)

•
Intuitive User Interface: The application boasts a clean, modern, and responsive design, ensuring a consistent experience across various devices (desktops, tablets, and mobile phones).

•
Data Persistence: All inspection data is automatically saved to the browser's local storage, ensuring that progress is not lost even if the user closes the application or their browser.

•
Data Import/Export (JSON): Users can export the entire application state (including all inspection data) as a JSON file. This allows for easy backup, sharing, or transfer of data between different instances of the application. Conversely, users can import JSON files to restore previous inspection states.

•
Reset Functionality: A clear reset option is available to wipe all stored data and return the application to its initial state, useful for starting new projects or clearing sensitive information.

•
Dynamic UI Updates: The user interface dynamically updates based on user interactions, such as navigating between rooms, selecting check statuses, or inputting data, providing immediate feedback.

•
Modals for User Feedback: Informative modal dialogs are used to provide feedback on actions like successful exports, import errors, or confirmation for resetting the application.

Technologies Used

The Room Inspection Application is built entirely using standard web technologies, making it highly portable and accessible through any modern web browser. It leverages a client-side architecture, ensuring quick response times and offline capabilities (once loaded).

•
HTML5: Provides the fundamental structure and content of the web pages.

•
CSS3: Styles the application, implementing a clean, responsive, and visually appealing design. It utilizes modern CSS features like Flexbox and Grid for layout, and gradients for aesthetic enhancements.

•
JavaScript (ES6+): Powers the entire interactive functionality of the application, including:

•
DOM Manipulation: Dynamically creates and updates UI elements based on user input and application state.

•
Event Handling: Manages user interactions such as button clicks, text input, and file operations.

•
Local Storage API: Persists application data across browser sessions.

•
File API: Handles the reading and writing of JSON and CSV files for import and export functionalities.

•
Data Structures: Manages complex inspection data using JavaScript objects and arrays.



How to Use

This section provides detailed instructions on how to navigate and utilize the Room Inspection Application for each of its inspection modes.

Getting Started

1.
Open the Application: Simply open the room_app.html file in any modern web browser. The application will load, and you will be presented with the Main Menu.

2.
Main Menu: The Main Menu allows you to select the type of inspection you wish to perform:

•
EA - Inspection: For general room-by-room inspections.

•
ECS Inspection: For detailed inspections of specific room codes.

•
Room Inspection SE/ST/SV: For entering and managing SE, ST, and SV codes for rooms.



EA - Inspection (Room-by-Room)

1.
Select "EA - Inspection": Click the "EA - Inspection" button on the Main Menu.

2.
Enter Room Names/Numbers: On the "Room Input Page", enter the names or numbers of the rooms you wish to inspect. Each room name/number should be on a new line. You can type them manually or paste a list from another source.

3.
Start Inspection: Click the "Start Inspection" button. This will take you to the "Check Page".

4.
Perform Checks: For each room:

•
The current room name will be displayed at the top.

•
A series of questions and checks will be presented.

•
For binary (Yes/No) questions, click the "Yes" or "No" button as appropriate. The selected button will highlight, and the item will be marked as checked.

•
For the "Comments" section, type your observations into the text area.

•
Your progress through the rooms will be shown by the progress bar and "Room X of Y" indicator.



5.
Navigate Rooms: Use the "Previous Room" and "Next Room" buttons to move between rooms. When you are on the last room, the "Next Room" button will change to "Complete Inspection".

6.
Complete Inspection: Once all rooms are inspected, click "Complete Inspection" to go to the "Completion Page".

7.
Export Data: On the "Check Page" or "Completion Page", click "Export to CSV" to download your inspection data as a CSV file. This file can be opened in spreadsheet software like Microsoft Excel.

8.
Return to Input: Click "Back to Input" to return to the room input page, where you can modify the room list or perform other data management actions.

ECS Inspection (Room Codes with Detailed Checks)

1.
Select "ECS Inspection": Click the "ECS Inspection" button on the Main Menu.

2.
Enter Room Codes: On the "Code Input Page", enter your room codes. The expected format is:

3.
Start Inspection: Click the "Start Inspection" button. This will take you to the "Code Check Page".

4.
Perform Code Checks: For each room and its associated codes:

•
The page displays an Excel-like grid with columns for "Code", "Status", and "Comment".

•
Status: Click the "Select Status" button next to a code. A dropdown list of predefined statuses will appear. Select the appropriate status (e.g., "Available", "Installed", "No Access"). The button text will update to reflect your selection.

•
Comment: Type any relevant comments or observations into the "Comment" text area next to each code.

•
Use the room selector dropdown at the top to quickly jump between different rooms.



5.
Navigate Rooms: Use the "Previous Room" and "Next Room" buttons to move between different sets of room codes. The "Next Room" button will change to "Complete Inspection" on the last set of codes.

6.
Complete Inspection: Click "Complete Inspection" to proceed to the "Completion Page".

7.
Export Data: On the "Code Check Page" or "Completion Page", click "Export to CSV" to download your code inspection data. The CSV will include the room name, code, selected status, and any comments.

8.
Return to Input: Click "Back to Input" to modify the code list or manage data.

Room Inspection SE/ST/SV

1.
Select "Room Inspection SE/ST/SV": Click this button on the Main Menu.

2.
Enter Room Numbers: On the "Room SE/ST/SV Input Page", enter the room numbers you want to inspect, one per line. The application will use the first 6 characters of each room number as a prefix for generating SE/ST/SV codes during export.

3.
Start SE/ST/SV Inspection: Click the "Start SE/ST/SV Inspection" button. This will lead you to the "Room SE/ST/SV Check Page".

4.
Enter SE/ST/SV Data: For each room:

•
You will see three separate text areas labeled "SE", "ST", and "SV".

•
Enter the relevant codes for each category, one per line.

•
For "ST" codes, you can optionally include clamp quantities using the format STCode-ClampQty (e.g., 12345-2).

•
The data you enter is automatically saved as you type.



5.
Navigate Rooms: Use the "Previous Room" and "Next Room" buttons to move between rooms. You can also use the room selector dropdown.

6.
Export Data: Click "Export to CSV" to download a CSV file containing all the SE, ST, and SV codes, including parsed clamp quantities and the generated room prefixes.

7.
Return to Input: Click "Back to Input" to go back to the room number input page.

Data Management

The application provides robust features for managing your inspection data:

•
Save Data: All your inspection progress and entered data are automatically saved to your browser's local storage. This means you can close the browser and reopen the application later, and your data will still be there.

•
Load Saved Data: On any input page (Room, Code, or SE/ST/SV), clicking "Load Saved Data" will retrieve the last saved state from local storage and populate the input fields and inspection data accordingly.

•
Download Data (JSON): Click "Download Data (JSON)" on any input page to export the entire application state as a JSON file. This is useful for backing up your data or transferring it to another device.

•
Upload Data (JSON): Click "Upload Data (JSON)" on any input page to import a previously saved JSON file. You can either click the file input label to browse for a file or drag and drop a JSON file onto the designated area. This will restore the application to the state contained within the JSON file.

•
Reset Application: Clicking "Reset Application" (available on all input pages) will clear all saved data from local storage and reset the application to its initial state. A confirmation modal will appear to prevent accidental data loss.

Responsive Design

The application is designed to be fully responsive, adapting its layout and elements to provide an optimal viewing and interaction experience across a wide range of devices, from large desktop monitors to tablets and mobile phones. This ensures that inspectors can use the tool effectively in various field conditions.

