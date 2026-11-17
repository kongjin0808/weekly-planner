# Weekly Timetable & Task Planner

A modern hybrid dark timetable planner with Google Sheets backend sync, inspired directly by your schedule design.

---

## 🚀 Quick Start (Instant Preview)

You can use the website immediately right on your machine!
1. Open File Explorer to:
   `C:\Users\chong\.gemini\antigravity\scratch\weekly-task-planner\`
2. Double-click **`index.html`** to open it in Chrome, Edge, or Firefox.
3. You will immediately see:
   - Your **7 AM to 12 AM Sunday-to-Saturday schedule** with red accent grid lines and pre-loaded sample entries (matching your photo: *Data Analytics, Material Selection, Vibration, Meet Advisor*).
   - The **Event Form** below the timetable to add items with "Every Week" vs "This Week Only".
   - The **Task Manager page** with the **5-step (20% per block) progress bar**, deadline indicators, and filters.

---

## 📊 Connecting to Google Sheets (2-Minute Setup)

You do **not** need to give anyone access to your Google account. You control everything through your own Google Drive:

### Step 1: Create a Google Sheet
1. Go to [https://sheets.new](https://sheets.new) to create a new blank Google Sheet.
2. Name it something like **My Timetable & Tasks**.

### Step 2: Paste the Apps Script Code
1. In your new Google Sheet, click the top menu: **Extensions** > **Apps Script**.
2. Delete whatever code is inside the editor.
3. Open `google-apps-script.js` from this folder, copy all contents, and paste it into the Apps Script editor.
4. Click the **Save** (💾) icon.

### Step 3: Deploy as a Web App
1. Click the blue **Deploy** button (top right) > select **New deployment**.
2. Click the gear icon next to "Select type" and choose **Web app**.
3. Fill in the deployment form:
   - **Description**: `Planner API`
   - **Execute as**: `Me (your email)`
   - **Who has access**: `Anyone` *(Note: This allows your local HTML page to send and receive your data)*.
4. Click **Deploy**.
5. Google will ask you to authorize access. Click **Authorize access**, select your Google account, click **Advanced**, and click **Go to Untitled project (unsafe)**. (This is standard for personal Apps Scripts).
6. **Copy the Web App URL** (it looks like `https://script.google.com/macros/s/.../exec`).

### Step 4: Paste into your Planner
1. In your open `index.html` in your browser, click the **Synced** / **Settings** pill at the top right.
2. Paste your Web App URL into the box and click **Save & Sync Now**.
3. Your Google Sheet will automatically generate two tabs (`Timetable` and `Tasks`) and keep everything backed up to the cloud!

---

## ✨ Features Included

1. **Red Accent Grid with Dark Slate Hybrid Style**:
   - High legibility, dark mode, red grid lines matching your reference photo.
   - Sunday to Saturday, 7:00 AM to 12:00 AM (17 hourly rows).
2. **Multi-Hour Event Cards**:
   - Classes spanning 2 or 3 hours (e.g. 12 PM - 3 PM) render continuously down the column.
3. **Quick Slot Click**:
   - Clicking directly on any empty grid cell automatically pre-fills that day and start time into the form below.
4. **"Every Week" vs. "This Week Only"**:
   - "Every Week" events stay permanently.
   - "This Week Only" events automatically reset on Sundays so your schedule stays fresh.
5. **Task Progress Bar (5 Steps = 20% each)**:
   - `[-]` and `[+]` buttons to decrement/increment by 20%.
   - You can also click directly on any of the 5 segment blocks.
   - Automatically detects overdue tasks and flags tasks due today.
