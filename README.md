# ToolApp - GIS Tool Tracking System

## Overview

**ToolApp** is a Geographic Information System (GIS) application designed to efficiently track tools and monitor their usage across different users and locations. Organizations can manage tool inventory, assign tools to users, track real-time locations, and generate comprehensive usage reports through an intuitive web interface powered by modern mapping technologies.

---

## Features

**GIS Integration:** Interactive maps with real-time tool location tracking and geofencing capabilities.

**Tool Management:** Complete tool registry with check-in/check-out system and status monitoring.

**User Management:** Secure authentication with role-based access control and activity logging.

**Location Tracking:** Real-time GPS tracking with movement history and geofenced zones.

**Analytics Dashboard:** Usage statistics, custom reports, and data visualization charts.

**Mobile Support:** Responsive design with QR code scanning for quick tool identification.

**Maintenance Scheduling:** Automated reminders and maintenance tracking system.

**Offline Capability:** Limited functionality available without internet connection.

---

## Installation

1. **Clone the Repository:**
```bash
git clone https://github.com/knurlybekov/ToolApp.git
cd ToolApp
```

2. **Install Dependencies:**
```bash
npm install
```

3. **Database Setup:**
   * Install PostgreSQL with PostGIS extension
   * Create database and run migrations
   * Configure environment variables in `.env`

4. **API Configuration:**
   * Add your mapping service API keys to `/src/config/maps.js`
   * Configure database connection in `/src/config/database.js`

5. **Start the Application:**
```bash
npm run dev
```

---

## Available Components

### Dashboard
* Overview of tool inventory and usage statistics
* Real-time alerts and notifications
* Quick access to frequently used features

### ToolsList
* Displays all tools with current status and location
* **Add Tool** button to show ToolForm
* Filter and search functionality for tool discovery
* Bulk operations for multiple tool management

### ToolForm
* Add or edit tool details (Name, Category, Specifications, Location)
* QR code generation for new tools
* Pre-fills fields during edit operations

### MapView
* Interactive map showing real-time tool locations
* Geofencing zones with customizable boundaries
* Tool clustering for better visualization
* Location history tracking and playback

### UserManagement
* User registration and profile management
* Role assignment and permission control
* Activity logs and usage statistics per user

### ReportsPanel
* Generate custom reports based on various parameters
* Export data in multiple formats (PDF, CSV, Excel)
* Usage analytics and trend visualization

---

## Test Cases

**Dashboard:** Displays tool inventory summary with real-time status updates.

**Add Tool:** ToolForm appears with required fields (Name, Category, Location, QR Code generation).

**Check-out Tool:** User selection updates tool status and assigns to selected user.

**Map Integration:** Tools display on interactive map with accurate GPS coordinates.

**Search Functionality:** Filter tools by name, category, status, or assigned user.

**Role-based Access:** Different features available based on user permissions (Admin, Manager, Worker).

---

## Libraries Used

**Frontend:** React.js, Leaflet/Google Maps API, Chart.js, Material-UI

**Backend:** Node.js/Express, PostgreSQL with PostGIS, JWT Authentication

**Real-time:** Socket.io for live location updates

**Mobile:** React Native for mobile application

---

## Contributing

Contributions are welcome! Fork the repository, create a feature branch, and submit a pull request with detailed description of changes.

## Contact

For queries or feedback: **n.pranideepreddy1999@gmail.com**

---

Efficiently manage your tools and optimize resource utilization with **ToolApp**! 🛠️
