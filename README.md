# eTourGood Database

The eTourGood Database is an open-source initiative providing structured, high-quality data for the global tourism industry. Initiated by Turgut Özal Aydın, this project offers datasets on languages, airlines, airports, travel agent associations, and more, serving developers, researchers, and tourism professionals. Use cases include building travel applications, analyzing tourism trends, or integrating with booking platforms. Community contributions are encouraged to keep the data accurate and up-to-date.

## Features

- **Comprehensive Datasets**: Includes data on world languages, countries, airlines, airports, tour types, and other tourism-related categories.
- **User-Friendly Interface**: A responsive, minimalist web interface with search, sort, and filter functionalities.
- **Open-Source**: Licensed under the MIT License, allowing free use, modification, and distribution.
- **Extensible**: Easy to add new datasets or enhance the interface with community contributions.

## Project Structure

The project is organized under the `database/` directory:

```plaintext
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
│   ├── logo.png


Datasets
Each dataset is stored as a JavaScript array in the js/data/ directory, designed for seamless integration into web, mobile, or analytical applications. Below are the key datasets and their structures:
•  World Languages (world-languages.js):
	•  Fields: name (e.g., “English”), officialCountries (e.g., “Widely spoken across many countries”)
•  World Countries (world-countries.js):
	•  Fields: phoneCode (e.g., “+90”), code (e.g., “TR”), name (e.g., “Türkiye”), continent (e.g., “Asia”), capital (e.g., “Ankara”)
•  World Airlines (world-airlines.js):
	•  Fields: iataCode (e.g., “TK”), name (e.g., “Turkish Airlines”), country (e.g., “Türkiye”), alliance (e.g., “Star Alliance”), icaoCode (e.g., “THY”)
•  World Airports (world-airports.js):
	•  Fields: iataCode (e.g., “IST”), name (e.g., “Istanbul Airport”), city (e.g., “Istanbul”), country (e.g., “Türkiye”), countryCode (e.g., “TR”)
•  Travel Agent Associations (association-ta.js):
	•  Fields: abbreviation (e.g., “TÜRSAB”), name (e.g., “Türkiye Seyahat Acentaları Birliği”), country (e.g., “Türkiye”), website (e.g., “tursab.org.tr”)
•  Tour Types (tour-types.js):
	•  Fields: name (e.g., “Cultural”), description (e.g., “Explore historical and cultural landmarks”)
•  Activity Types (activity-types.js):
	•  Fields: name (e.g., “Hiking”), description (e.g., “Guided walks through natural landscapes”)
•  Museum Types (museum-types.js):
	•  Fields: name (e.g., “Art”), description (e.g., “Collections of paintings and sculptures”)
•  Hotel Types (hotel-types.js):
	•  Fields: name (e.g., “Boutique”), description (e.g., “Small, stylish hotels with unique themes”)
•  Transport Types (transport-types.js):
	•  Fields: name (e.g., “Bus”), description (e.g., “Public or private bus services”)
•  Guide Types (guide-types.js):
	•  Fields: name (e.g., “Local Guide”), description (e.g., “Guides with deep knowledge of the area”)
•  Hotel Room Types (hotel-room-types.js):
	•  Fields: name (e.g., “Standard”), description (e.g., “Basic room with essential amenities”)
•  Booking Statuses (booking-statuses.js):
	•  Fields: name (e.g., “Confirmed”), description (e.g., “Booking is confirmed and active”)
•  Payment Types (payment-types.js):
	•  Fields: name (e.g., “Credit Card”), description (e.g., “Payment via credit or debit card”)
Installation
To run the eTourGood Database locally:
1.  Clone the Repository:
git clone https://github.com/turgutoaydin/etourgood-database.git
cd etourgood-database/database
2.  Set Up a Local Server:
	•  Use a local server to avoid CORS issues with file:// protocol. For example:
python -m http.server 8000
	•  Alternatively, use VS Code Live Server or any other local server tool.
3.  Access the Application:
	•  Open your browser and navigate to http://localhost:8000.
4.  Verify File Structure:
	•  Ensure all files are in the correct paths as shown in the project structure above.
	•  Place your logo at database/assets/logo.png or update the path in index.html if different:
<a href="../index.html" class="logo"><img src="assets/logo.png" alt="eTourGood Database Logo"></a>
5.  Clear Browser Cache:
	•  If you encounter issues (e.g., “No data available”), clear the browser cache (Ctrl+Shift+R or Cmd+Shift+R) to ensure the latest files are loaded.
Usage
•  Browse Data: Select a category (e.g., “World Languages”) from the sidebar to view its data in a list or table format.
•  Search: Use the sidebar search to filter menu items or the content search to filter data within a section.
•  Sort: Click table headers (e.g., “IATA Code” for airports) to sort data in ascending or descending order.
•  Contribute: Add or update datasets in the js/data/ directory or enhance the interface (see Contributing below).
Troubleshooting
If you see the error “No data available for this section. Please ensure the data file is loaded correctly”:
1.  Check File Paths:
	•  Verify that all data files (e.g., js/data/world-languages.js) exist in the database/js/data/ directory.
	•  Ensure file names match exactly (case-sensitive, e.g., world-languages.js not World-Languages.js).
2.  Validate Data Format:
	•  Each data file should define a global variable in the format const variableName = [...]. For example:
const worldLanguages = [{ name: "English", officialCountries: "Widely spoken" }, ...];
	•  Check for syntax errors (e.g., missing brackets, invalid JSON).
3.  Script Load Order:
	•  In index.html, ensure data file <script> tags (e.g., <script src="js/data/world-languages.js">) come before <script src="js/main.js">.
4.  Console Logs:
	•  Open the browser console (F12 > Console) and look for errors like Uncaught ReferenceError: worldLanguages is not defined or logs like World Languages data: undefined.
	•  These indicate which file (e.g., js/data/world-languages.js) is missing or failing to load.
5.  Local Server:
	•  Run the project via a local server (e.g., python -m http.server) instead of file:// to avoid CORS issues.
6.  Cache Issues:
	•  Clear the browser cache (Ctrl+Shift+R) to ensure the latest files are loaded.
Contributing
We welcome contributions to improve the eTourGood Database. To contribute:
1.  Fork the Repository:
	•  Fork the project on GitHub.
2.  Make Changes:
	•  Add or update data in the js/data/ directory, following the existing structure (e.g., { iataCode: "TK", name: "Turkish Airlines", ... } for airlines).
	•  Enhance the interface (e.g., improve search or add new features) in js/main.js, styles.css, or other files.
3.  Test Locally:
	•  Verify JSON format and test UI rendering to ensure compatibility.
4.  Submit a Pull Request:
	•  Create a pull request with a clear description (e.g., “Added 10 new airports” or “Fixed typo in countries”).
5.  Contact:
	•  For feedback or issues, email turgutoaydin@gmail.com.
Examples:
•  Add a new airline: { iataCode: "XY", name: "Example Air", country: "Country", alliance: "None", icaoCode: "XYZ" } in world-airlines.js.
•  Update a country’s capital in world-countries.js.
•  Improve the search UI in js/modules/filter.js.
License
This project is licensed under the MIT License, allowing free use, modification, and distribution with proper attribution.
Contact
For questions, suggestions, or data updates, reach out to turgutoaydin@gmail.com.