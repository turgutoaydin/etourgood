# 🌍 eTourGood Database

**eTourGood Database** is an open-source initiative providing structured, high-quality tourism data for global use. Created by [Turgut Özal Aydın](https://github.com/turgutoaydin), this project serves developers, researchers, and tourism professionals who want to build tourism-related applications, perform data analysis, or integrate with travel platforms.

---

## 🚀 Overview

This database offers structured datasets that include:

- 🌐 World Languages & Countries  
- ✈️ Airlines & Airports  
- 🧭 Tour & Activity Types  
- 🏨 Hotel & Room Types  
- 🚌 Transport & Guide Types  
- 🖼️ Museum Types  
- 🧾 Booking Statuses & Payment Methods  
- 🏢 Travel Agent Associations

**Use Cases**  
✅ Travel app development  
✅ Booking engine integration  
✅ Tourism data visualization  
✅ Academic and market research

---

## 📁 Project Structure

database/
├── index.html
├── styles.css
├── js/
│   ├── main.js
│   ├── modules/
│   │   ├── sort.js
│   │   ├── filter.js
│   ├── data/
│   │   ├── world-languages.js
│   │   ├── world-countries.js
│   │   ├── world-airlines.js
│   │   ├── world-airports.js
│   │   ├── association-ta.js
│   │   ├── tour-types.js
│   │   ├── activity-types.js
│   │   ├── museum-types.js
│   │   ├── hotel-types.js
│   │   ├── transport-types.js
│   │   ├── guide-types.js
│   │   ├── hotel-room-types.js
│   │   ├── booking-statuses.js
│   │   ├── payment-types.js
├── assets/
│   └── logo.png

---

## 📊 Dataset Highlights

Each dataset is defined as a JavaScript array for easy frontend integration. All are located in the `js/data/` folder.

### Example: `world-languages.js`

```javascript
const worldLanguages = [
  {
    name: "English",
    officialCountries: "Widely spoken across many countries"
  },
  {
    name: "Turkish",
    officialCountries: "Official language in Türkiye, Cyprus"
  }
];

Included Datasets:
	•	world-languages.js: Language name, official countries
	•	world-countries.js: Country code, name, continent, capital
	•	world-airlines.js: IATA/ICAO codes, country, alliance
	•	world-airports.js: IATA code, name, city, country
	•	association-ta.js: Travel agent associations by country
	•	tour-types.js: Tour category name & description
	•	activity-types.js: Activities like hiking, diving, etc.
	•	museum-types.js: Museum categories (art, history, etc.)
	•	hotel-types.js: Boutique, resort, business, etc.
	•	transport-types.js: Bus, plane, ferry, etc.
	•	guide-types.js: Local, professional, regional guides
	•	hotel-room-types.js: Standard, deluxe, suite, etc.
	•	booking-statuses.js: Confirmed, pending, canceled, etc.
	•	payment-types.js: Credit card, crypto, cash, etc.

⸻

⚙️ Installation
	1.	Clone the Repository

git clone https://github.com/turgutoaydin/etourgood-database.git
cd etourgood-database/database


	2.	Start Local Server
Use a local server to avoid file:// CORS issues:

python -m http.server 8000

Or use VS Code Live Server extension.

	3.	Open in Browser
Navigate to:
👉 http://localhost:8000
	4.	Add Logo (Optional)
Place your logo in:
assets/logo.png
Or update the path in index.html.
	5.	Clear Cache if Necessary
Press Ctrl + Shift + R or Cmd + Shift + R for hard refresh.

⸻

🔍 Usage
	•	View Data: Select any dataset from the sidebar.
	•	Search: Use sidebar or table-level filters.
	•	Sort: Click table headers to sort columns.
	•	Contribute: Add new datasets or improve UI.

⸻

🧰 Troubleshooting

If you see:

"No data available for this section. Please ensure the data file is loaded correctly."

Check the following:
	•	✅ File names and paths (case-sensitive)
	•	✅ JavaScript format (each file should define a global const)
	•	✅ Proper syntax (no trailing commas, no broken brackets)
	•	✅ Script load order in index.html

⸻

🤝 Contributing

All contributions are welcome!
	•	Add new tourism-related datasets
	•	Translate the interface
	•	Enhance the design or UI/UX
	•	Fix bugs or propose new features

To contribute:
	1.	Fork the repository
	2.	Create a new branch
	3.	Submit a pull request

⸻

📄 License

This project is licensed under the MIT License.
You are free to use, modify, and distribute it for personal or commercial purposes.

⸻

📬 Contact

📌 Website: etourgood.com
📧 Email: hello@etourgood.com
👤 Creator: Turgut Özal Aydın
📍 Based in Türkiye

⸻

Thank you for supporting open data for a better tourism future!

---