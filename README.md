# College Lost & Found Portal

## Project Title
**College Lost & Found Portal**

## College
**Vaishnavi Group of Institutes**

## Project Objective
The objective of this minor project is to provide a simple, professional and responsive web portal through which college students and staff can report lost or found items, search existing reports, view item details and manage their own submissions.

## Problem Statement
Items such as mobile phones, identity cards, books, bags, keys and documents are frequently misplaced on college campuses. Traditional notice boards and informal messaging make it difficult to maintain searchable and up-to-date records. A centralized digital portal can improve discoverability and reduce the time required to reconnect owners with their belongings.

## Proposed Solution
The College Lost & Found Portal provides separate reporting workflows for lost and found items. Reports are saved in the browser using JavaScript LocalStorage. Users can browse reports, search by keywords, filter by category and status, view detailed information, and manage their own reports through the dashboard.

## Features
- Responsive college-style user interface
- Vaishnavi Group of Institutes branding
- Report lost item
- Report found item
- Client-side form validation
- Optional image upload and browser-side image compression
- Unique report IDs
- LocalStorage-based data persistence
- Search by item, description, location, identification or reporter
- Category and status filters
- Sort by newest, oldest, name or category
- Item details modal with contact option
- Personal dashboard using submitted contact information
- Edit own reports
- Delete reports with confirmation
- Mark reports as resolved
- Dynamic statistics
- Recent reports
- Success/error notifications
- Empty-state handling

## Technology Used
- HTML5
- CSS3
- Vanilla JavaScript
- LocalStorage API

No React, Angular, Node.js, PHP, Python, MySQL, Firebase or external backend is required.

## Hardware / Software Requirements

### Hardware
- Computer or laptop
- Minimum 2 GB RAM recommended
- Basic storage for project files

### Software
- Google Chrome, Microsoft Edge, Mozilla Firefox or another modern browser
- VS Code or any text/code editor
- No server installation is required

## Project Modules
1. **Home Module** — introduction, quick actions, statistics and recent reports.
2. **Lost Report Module** — captures details of lost items.
3. **Found Report Module** — captures details of found items.
4. **Browse Module** — search, filtering, sorting and item details.
5. **Dashboard Module** — edit, delete and resolve the user's reports.
6. **About Module** — project purpose, workflow, modules and technology.
7. **Data Module** — LocalStorage CRUD operations and sample data.

## Folder Structure
```text
College-Lost-Found-Portal/
│
├── index.html
├── report-lost.html
├── report-found.html
├── items.html
├── dashboard.html
├── about.html
├── README.md
│
├── css/
│   └── style.css
│
├── js/
│   ├── data.js
│   ├── main.js
│   ├── reports.js
│   └── dashboard.js
│
└── images/
    └── college-logo.png
```

## How to Run
1. Keep the folder structure unchanged.
2. Put the official college logo supplied for the project at `images/college-logo.png`.
3. Open `index.html` directly in a modern browser.
4. Use **Report Lost** or **Report Found** to create a report.
5. Browse reports from **Lost & Found**.
6. Open **Dashboard**, enter the same contact information used in a report, and manage the submission.

Because the project uses LocalStorage, it can run directly from the local file system in normal modern browsers. If a browser restricts a feature under `file://`, open the folder with VS Code Live Server; no application backend is required.

## How LocalStorage Works
The JavaScript data layer stores all reports as a JSON array under the key:

`vgi_lost_found_reports_v1`

The dashboard contact is stored separately under:

`vgi_lost_found_dashboard_contact_v1`

When a report is created, JavaScript:
1. Creates a unique ID.
2. Builds a report object.
3. Reads existing reports from LocalStorage.
4. Adds the new object.
5. Saves the updated JSON array.

Edit, delete and resolve operations follow the same client-side CRUD pattern.

## Data Structure
Each report contains:
- `id`
- `type`
- `itemName`
- `category`
- `description`
- `location`
- `date`
- `time`
- `identification`
- `reporterName`
- `contact`
- `image`
- `status`
- `createdAt`
- `updatedAt` when edited

## Future Scope
- Secure college login and role-based access
- Central server/database
- Admin verification and moderation
- Email/SMS notifications
- Secure in-app messaging
- Duplicate/matching-item suggestions
- QR-based item verification
- Cloud image storage
- College ERP/student-directory integration
- Audit logs and analytics dashboard

## Advantages
- Easy to use
- Low-cost implementation
- No database installation
- Works on desktop and mobile
- Fast client-side search and filtering
- Suitable for a college minor-project demonstration
- Demonstrates practical HTML, CSS, JavaScript and LocalStorage skills

## Limitations
- Data is stored only in the current browser/device.
- Reports are not automatically shared between different users or computers.
- LocalStorage is not suitable for production-scale multi-user data.
- Contact information is visible to users who can view the report.
- No server-side authentication or moderation is included.

## Conclusion
The College Lost & Found Portal demonstrates a complete front-end workflow for managing lost and found reports in a college environment. The project combines semantic HTML5, responsive CSS3 and modular Vanilla JavaScript with LocalStorage-based persistence to provide a functional application without a backend. It can serve as a foundation for a future production system with authentication, a central database and administrative controls.

## Academic Note
This project is intended as a college minor project/demo application. For real deployment, user authentication, privacy controls, server-side validation, moderation and secure data storage should be added.
