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

# 📸 Screenshots

<img src="Screenshot/Screenshot 1.png" width="500"/> <img src="Screenshot/Screenshot 2.png" width="500"/>

<img src="Screenshot/Screenshot 3.png" width="500"/> <img src="Screenshot/Screenshot 4.png" width="500"/>





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
   ```
2. You can run it locally using Live Server, or host it for free using GitHub Pages, Vercel, or Netlify.

### Step 2: Set up the Google Sheets Database
1. Go to Google Sheets and create a new blank spreadsheet.

2. Click on `Extensions` > `Apps Script`.

3. Delete the default code and paste your backend Google Apps Script code.

4. Click `Deploy` > `New deployment`.

5. Select type `Web app`.

6. Set `"Execute as"` to Me and `"Who has access"` to Anyone.

7. Click Deploy and copy the resulting Web App URL.

(Note: The script will automatically create the Sales, Products, Settings, and SystemData tabs for you during your first transaction).

### Step 3: Connect Frontend to Backend
1. Open the app.js file in your code editor.

2. Find the `GOOGLE_SCRIPT_URL` variable at the top of the file:

```bash
const GOOGLE_SCRIPT_URL = 'PASTE_YOUR_COPIED_URL_HERE';
```
Paste your URL, save the file, and push the changes to GitHub.

## 📖 Usage Guide
1. Inventory Setup: Go to the Inventory tab to add your products. Set your starting invoice number in the Settings panel.

2. Billing: Go to the Billing tab. Click items to add them to the cart. Click the quantity number in the cart to type exact decimals (e.g., 1.5 kg).

3. Checkout: Click "Proceed to Checkout", apply any discounts, choose the payment method, and click Save & Print.

4. Analytics: Go to the Reports tab to view your live cloud-synced charts, filter by date, or download your sales as a .csv.

## 📄 License
This project is open-source and available under the MIT License.
