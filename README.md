# Sunrise & Sunset Dashboard

This project is a web application that allows users to fetch sunrise and sunset timings for a selected or current location. Users can interact with a map to update their location, view the solar data for today and tomorrow, and explore details like dawn, dusk, and golden hours. The app uses a Flask backend as a proxy server to handle API requests while overcoming CORS issues.

---

## **Features**

- Interactive map for selecting locations.
- Fetch sunrise and sunset data for any location.
- View timezone and detailed solar information for today and tomorrow.
- Use your current location with the "Use Current Location" button.
- Change background dynamically based on the selected location's time and season.

---

## **Technologies Used**

### **Frontend**
- HTML, CSS, JavaScript
- Leaflet.js for interactive maps

### **Backend**
- Python with Flask
- Flask-CORS for handling CORS issues

### **APIs**
- [Sunrise Sunset API](https://sunrisesunset.io/api/)
- [Nominatim OpenStreetMap API](https://nominatim.openstreetmap.org/)
- [TimezoneDB API](https://timezonedb.com/)

---



### **Backend Setup**

#### **1. Install Python and Required Packages**  
Ensure Python (3.x) is installed, then run:
```bash
pip install flask flask-cors requests
```

#### **2. Start the Flask Server**  
The server acts as a proxy for external APIs to handle CORS issues. To start the server:
```bash
python server.py
```
By default, the server will run on **http://localhost:5000**.

---

### **Frontend Setup**

#### **1. Open the Application**  
Navigate to the project directory and open the `index.html` file in your browser.

#### **2. Interact with the App**
- **Select a Location:** Choose from predefined options in the dropdown.
- **Map Interaction:** Click or drag the marker on the map to select a custom location.
- **Use Current Location:** Click the "Use Current Location" button to get data for your current coordinates.

---

## **Why Flask-CORS?**

When running a Flask backend, browsers enforce **CORS rules**, which prevent the frontend from accessing APIs directly due to security restrictions. By using a Flask backend:
- We overcome these restrictions using a proxy server.
- The `Flask-CORS` library ensures the backend adds necessary headers (`Access-Control-Allow-Origin`) to allow secure communication between the frontend and backend.

---

## **Usage**

1. **Interactive Map:** Drag or click on the map to update the location and fetch solar data.
2. **Predefined Locations:** Select from the dropdown for quick access to common locations.
3. **Background Updates:** Background images change dynamically based on the time and season of the selected location.

---

## **Troubleshooting**

1. **Flask Server Not Running:**  
   - Ensure Python is installed.
   - Verify all dependencies are installed using `pip list`.

2. **CORS Errors:**  
   - Ensure `Flask-CORS` is installed and enabled in `server.py`.

3. **API Key Errors:**  
   - Replace placeholder API keys in `server.py` with valid keys from the respective APIs.

---

## **Folder Structure**

```
sunrise-dashboard/
│
├── assets/
│   └── images/           # Background images for seasons and times of the day
├── scripts/
│   ├── main.js           # Core functionality for frontend interactions
│   ├── dataDisplay.js    # Handles displaying solar data
├── styles.css            # Styling for the application
├── index.html            # Main HTML file
└── server.py             # Flask backend proxy server
```

---


# Sample Screenshot of the Application working


![alt text](image1.png)

# changing background image according to the time in BRAZIL

![alt text](<Screenshot 2024-11-30 at 5.55.52 AM.png>)

# Selecting Location using MAP 

![alt text](<Screenshot 2024-11-30 at 5.56.10 AM.png>)

# Responsive LAYOUTS in IPHONE 14PRO MAX 

![alt text](<Screenshot 2024-11-30 at 5.57.30 AM.png>)

# for size 1200 X 1260 

![alt text](<Screenshot 2024-11-30 at 5.57.45 AM.png>)
