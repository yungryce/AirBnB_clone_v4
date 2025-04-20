# AirBnB Clone - Dynamic Web Application

![AirBnB Logo](https://i.imgur.com/QiU1LdE.png)

## Project Overview

This is the final implementation of the AirBnB clone project, featuring a full-stack web application with dynamic content loading through JavaScript. The complete system includes:

1. **Command Line Interface**: Console for managing objects
2. **Data Models and Storage Engines**: File-based and database persistence 
3. **RESTful API**: HTTP interface for programmatic access to data
4. **Dynamic Web Interface**: JavaScript-based front-end that consumes the API

## Technology Stack

| Category | Technologies |
|----------|-------------|
| **Backend** | Python 3.4.3, Flask |
| **Database** | MySQL, SQLAlchemy ORM |
| **API** | RESTful architecture, JSON, CORS, Swagger/Flasgger |
| **Frontend** | HTML5, CSS3, JavaScript, jQuery |
| **Storage** | JSON File Storage, MySQL Database |
| **Testing** | unittest framework |

## Key Features

### Dynamic Content
- Real-time API status indicator
- Filter places by amenities, states, and cities without page reload
- Show/hide reviews dynamically
- Asynchronous data loading with AJAX

### Enhanced API
- Improved error handling
- Cross-Origin Resource Sharing (CORS) support
- API documentation with Swagger/Flaggger
- Search functionality for places

## Project Structure

* `api/` - RESTful API implementation
  * `v1/` - API version 1
    * `views/` - API route handlers
    * `app.py` - Flask application with error handling and CORS
* `models/` - Data models with optimized storage engines
  * `engine/` - Enhanced storage engines with get() and count() methods
* `web_dynamic/` - Dynamic web application 
  * `static/scripts/` - JavaScript for dynamic content loading
  * `static/styles/` - CSS stylesheets
  * `templates/` - HTML templates
* `web_flask/` - Static web application (v2-v3)
* `console.py` - Command interpreter

## Installation & Setup

1. Clone the repository:
```bash
git clone https://github.com/username/AirBnB_clone_v4.git
cd AirBnB_clone_v4
```

2. Setup MySQL database (if using db storage):
```bash
cat setup_mysql_dev.sql | mysql -u root -p
```

3. Install dependencies:
```bash
pip3 install -r requirements.txt
```

## Usage

### Running the Web Application

Start the API server:
```bash
HBNB_MYSQL_USER=hbnb_dev HBNB_MYSQL_PWD=hbnb_dev_pwd HBNB_MYSQL_HOST=localhost \
HBNB_MYSQL_DB=hbnb_dev_db HBNB_TYPE_STORAGE=db HBNB_API_HOST=0.0.0.0 \
HBNB_API_PORT=5001 python3 -m api.v1.app
```

In another terminal, run the web server:
```bash
HBNB_MYSQL_USER=hbnb_dev HBNB_MYSQL_PWD=hbnb_dev_pwd HBNB_MYSQL_HOST=localhost \
HBNB_MYSQL_DB=hbnb_dev_db HBNB_TYPE_STORAGE=db python3 -m web_dynamic.2-hbnb
```

Access the application at http://localhost:5000/2-hbnb

### API Documentation

Interactive API documentation is available at:
```
http://0.0.0.0:5001/apidocs/
```

### Console

The command interpreter is still available for direct data manipulation:
```bash
./console.py
```

## Frontend Features

- **API Status Indicator**: Shows the status of the backend API
- **Filters**: Select amenities, states, or cities to filter places
- **Dynamic Place Loading**: Places are loaded based on selected filters
- **Expandable Reviews**: Click to show/hide reviews for each place

## Development Progression

1. **v1**: Command-line functionality with file storage
2. **v2**: Database integration and web server configuration
3. **v3**: RESTful API implementation
4. **v4**: Dynamic web interface with JavaScript

## Authors
See the list of [contributors](./AUTHORS) who participated in this project.

## License
This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](./LICENSE) file for details.