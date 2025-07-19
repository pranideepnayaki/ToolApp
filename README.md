# ToolApp - Tool Tracking Web Application

## Overview
**ToolApp** is a Flask-based web application designed to track tools and work activities across construction sites. The application provides interactive mapping capabilities to visualize active work locations where tools are currently being used by employees, along with reporting and analytics features for work efficiency monitoring.

---

## Features
- **Interactive Mapping:** Folium-based maps showing active work locations where tools are currently in use
- **Work Process Tracking:** Monitor which employees are using which tools with start/end times and duration calculations
- **Analytics & Reporting:** Plotly-powered charts and reports for work efficiency analysis
- **Employee Management:** View employee information and work assignments
- **Tool Inventory:** Display tool information and current status (read-only)
- **Responsive Design:** Bootstrap-based web interface

---

## Technology Stack
- **Backend:** Python Flask with SQLAlchemy ORM
- **Database:** Microsoft SQL Server (Azure hosted)
- **Frontend:** Server-side rendered Jinja2 templates with Bootstrap
- **Mapping:** Folium for interactive maps
- **Data Visualization:** Plotly for charts and analytics
- **Data Processing:** Pandas for database-to-web integration

---

## Installation

1. **Clone the Repository:**
```bash
git clone https://github.com/pranideepnayaki/ToolApp.git
cd ToolApp-main
```

2. **Install Python Dependencies:**
```bash
pip install flask flask-sqlalchemy flask-login flask-socketio pandas pyodbc folium plotly matplotlib flask-paginate apscheduler
```

3. **Database Configuration:**
   - The application is configured to connect to Azure SQL Server
   - Update database credentials in `__init__.py` and `dbConn.py` with your connection details
   - Ensure you have the appropriate ODBC drivers installed

4. **Start the Application:**
```bash
python app.py
```

---

## Application Structure

### Core Components

**Authentication System:**
- User login/logout functionality
- Flask-Login integration for session management
- Employee-based authentication

**Dashboard:**
- Interactive Folium map showing active work locations
- Real-time display of tools currently in use
- Work area visualization with colored polygons

**Reporting:**
- Work efficiency analytics with time consumption vs. required time
- Bar charts and box plots for performance analysis
- Paginated data tables with filtering

**Data Management:**
- Employee information display
- Tool inventory viewing
- Work process tracking and history

---

## Current Limitations

This is a prototype application with the following limitations:
- **Read-only data management:** No create/edit functionality for tools or employees
- **Basic spatial operations:** Limited to coordinate display, no advanced GIS functions
- **Hardcoded credentials:** Database connection details are embedded in source code
- **No migration system:** Database schema management not implemented
- **Mixed database approaches:** Uses both SQLAlchemy ORM and raw SQL queries

---

## Database Schema

The application works with the following main tables:
- **employees:** User information and authentication
- **tools:** Tool inventory with location coordinates
- **work_process:** Work activity tracking with start/end times
- **side:** Work area definitions with boundary coordinates
- **work_list:** Work templates and time requirements

---

## Usage Example

1. **Login:** Use credentials from the employee database
2. **View Dashboard:** See interactive map with active work locations
3. **Access Reports:** Navigate to analytics for work efficiency charts
4. **Filter Data:** Use dropdown menus to filter by work areas

---

## Development Notes

This application demonstrates:
- Flask web framework implementation
- Pandas integration for data processing
- Interactive mapping with Folium
- Data visualization with Plotly
- Basic authentication and session management

**Areas for Production Enhancement:**
- Implement proper configuration management
- Add comprehensive CRUD operations
- Enhance security (password hashing, CSRF protection)
- Add proper database migrations
- Implement advanced spatial analysis capabilities

---

## Contributing
Contributions are welcome! Please feel free to submit issues and enhancement requests.

## Contact
For queries or feedback: **n.pranideepreddy1999@gmail.com**

---

*A Flask-based tool tracking application with mapping and analytics capabilities* 🛠️
