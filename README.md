🪑 Real-Time Seat Selection System
A web app for students to select seats in a classroom, with real-time updates across multiple devices using Google Apps Script and Google Sheets as a database.

🌟 Features
✅ Real-Time Updates – All users see seat selections instantly
✅ No CORS Issues – Uses Google Apps Script as a backend
✅ Responsive Design – Works on desktop and mobile
✅ Teacher Controls – Reset all seats with a password
✅ Persistent Data – All data saved in Google Sheets

🛠️ Tech Stack
Frontend: HTML5, CSS3, JavaScript

Backend: Google Apps Script

Database: Google Sheets

Hosting: GitHub Pages

🚀 Setup Instructions
1️⃣ Google Apps Script Setup
Create a new Google Apps Script project (script.google.com)

Copy the backend code (link to backend code section in this README)

Create a Google Sheet named "SeatSelectionData"

In the script editor:

javascript
// Replace this line in the code:
const ss = SpreadsheetApp.getActiveSpreadsheet();
// With:
const ss = SpreadsheetApp.openById("YOUR_GOOGLE_SHEET_ID");
Deploy as a Web App (Execute as "Me", Access "Anyone")

2️⃣ GitHub Pages Deployment
Fork this repository

Edit index.html and update:

javascript
const CONFIG = {
  GOOGLE_SCRIPT_URL: "YOUR_APPS_SCRIPT_URL",
  API_KEY: "YOUR_SECRET_KEY", // Keep this secure!
  PASSWORD: "prof123", // Teacher reset password
  POLL_INTERVAL: 5000 // 5-second updates
};
Enable GitHub Pages in Settings → Pages → main branch

3️⃣ First-Time Use
Students visit the GitHub Pages URL

Enter their details and select a seat

Teachers can reset seats using password: prof123

📝 Customization
Change Classroom Layout
Edit the seat grid in index.html:

html
<div class="classroom" id="classroom">
  <!-- Example seat -->
  <div class="seat" data-seat="A3">
    <span class="seat-label">A3</span>
  </div>
  <!-- Add more seats... -->
</div>
Modify Styling
Edit the CSS variables in index.html:

css
:root {
  --teacher-color: #9b59b6;
  --available-color: #ecf0f1;
  --selected-color: #2ecc71;
  --occupied-color: #e74c3c;
}
⚠️ Troubleshooting
Issue	Solution
Seats not updating	Check Google Script URL in CONFIG
403 Errors	Ensure Google Sheet is shared with the script account
Reset not working	Verify teacher password matches in both script and frontend
📜 License
MIT License - Free for educational use. Commercial use requires permission.

🙏 Credits
Developed by [Victor Ferauche] - [Contact vicfera75@gmail.com]

📌 Recommended Repository Structure
seat-selection-system/
├── index.html          # Main application file
├── README.md           # This file
└── images/             # Screenshots (optional)
