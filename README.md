# 🛒 Fresh POS - Hybrid-Cloud Web POS System

A lightweight, offline-first Point of Sale (POS) system built with pure HTML, CSS, and Vanilla JavaScript. It uses **Google Sheets** as a free, serverless cloud database while relying on `localStorage` for blazing-fast, offline-capable performance.

Perfect for small retail shops, flour mills, and quick-service businesses.

## ✨ Key Features

* **⚡ Hybrid-Cloud Sync:** Instant UI loading using local storage, with silent background synchronization to Google Sheets.
* **🛒 Advanced Billing:** Supports decimal quantities (e.g., 1.5 kg), discounts, and split payments (Cash + UPI).
* **🖨️ Thermal Printer Ready:** Auto-generates and formats 3-inch (80mm) professional invoices ready for Bluetooth/USB thermal printers.
* **📦 Inventory Management:** Add items with base64-compressed images, toggle "Track Stock" vs "Unlimited", and organize by Categories/Units.
* **📊 Interactive Reports:** Visual sales dashboards using Chart.js, date-range filtering, CSV data export, and the ability to reprint old bills.
* **⚙️ Custom Invoicing:** Set custom invoice prefixes (e.g., `INV-0001`) and auto-incrementing bill numbers.
* **📱 Mobile Responsive:** Clean, touch-friendly UI that works flawlessly on desktop monitors, tablets, and smartphones.

## 🛠️ Tech Stack

* **Frontend:** HTML5, CSS3, Vanilla JavaScript
* **Backend / Database:** Google Apps Script + Google Sheets
* **Charts:** Chart.js (via CDN)
* **Storage:** Browser `localStorage`

## 🚀 Setup & Installation

To run this POS system yourself, you need to host the frontend files and connect them to your own Google Sheet.

### Step 1: Host the Frontend
1. Clone this repository:
   ```bash
   git clone [https://github.com/yourusername/fresh-pos.git](https://github.com/yourusername/fresh-pos.git)
You can run it locally using Live Server, or host it for free using GitHub Pages, Vercel, or Netlify.

### Step 2: Set up the Google Sheets Database
Go to Google Sheets and create a new blank spreadsheet.

Click on Extensions > Apps Script.

Delete the default code and paste the backend script (You can find the required App Script code in the backend-script.js file if you saved it, or ask the developer).

Click Deploy > New deployment.

Select type Web app.

Set "Execute as" to Me and "Who has access" to Anyone.

Click Deploy and copy the resulting Web App URL.

(Note: The script will automatically create the Sales, Products, Settings, and SystemData tabs for you during your first transaction).

Step 3: Connect Frontend to Backend
Open the app.js file in your code editor.

Find the GOOGLE_SCRIPT_URL variable at the top of the file:

JavaScript
const GOOGLE_SCRIPT_URL = 'PASTE_YOUR_COPIED_URL_HERE';
Paste your URL, save the file, and push the changes to GitHub.

### 📖 Usage Guide
Inventory Setup: Go to the Inventory tab to add your products. Set your starting invoice number in the Settings panel.

Billing: Go to the Billing tab. Click items to add them to the cart. Click the quantity number in the cart to type exact decimals (e.g., 1.5 kg).

Checkout: Click "Proceed to Checkout", apply any discounts, choose the payment method, and click Save & Print.

Analytics: Go to the Reports tab to view your live cloud-synced charts, filter by date, or download your sales as a .csv.

### 📄 License
This project is open-source and available under the MIT License.
