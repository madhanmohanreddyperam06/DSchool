# School Management System

![HTML5](https://img.shields.io/badge/HTML-5-E34F26?style=flat-square&logo=html5)
![CSS3](https://img.shields.io/badge/CSS-3-1572B6?style=flat-square&logo=data:image/svg%2bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0iIzE1NzJCNiIgZD0iTTEuNSAwaDIxbC0xLjkxIDIxLjU2M0wxMS45NzcgMjRsLTguNTY1LTIuNDM4TDEuNSAwbTcuMDkgNC40MTNMNS40MSA0LjQxbC4yMTMgMi42MjIgMTAuMTI1LjAwMi0uMjU1IDIuNzE2aC02LjY0bC4yNCAyLjU3M2g2LjE4MmwtLjM2NiAzLjUyMy0yLjkxLjgwNC0yLjk1Ni0uODEtLjE4OC0yLjExaC0yLjYxbC4yOSAzLjg1NUwxMiAxOS4yODhsNS4zNzMtMS41M0wxOC41OSA0LjQxNHoiLz48L3N2Zz4=)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=flat-square&logo=javascript)
[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=flat-square&logo=python)](https://www.python.org/)
[![Django](https://img.shields.io/badge/Django-3.2+-092E20?style=flat-square&logo=django&logoColor=44B78B)](https://www.djangoproject.com/)
![MySQL](https://img.shields.io/badge/MySQL-Database-4479A1?style=flat-square&logo=mysql)
[![License](https://img.shields.io/badge/License-MIT-dfb317?style=flat-square)](LICENSE.txt)

A comprehensive Django-based web application designed for school administrators to efficiently manage school records, including student data, staff information, academic results, and financial management.

## Features

### Student Management
- Add, update, delete, and view student details
- Personal information management
- Class assignments and tracking
- Bulk upload via CSV files
- Student passport photo uploads

### Staff Management
- Manage staff records with personal details
- Staff status tracking
- Administrative controls

### Academic Management
- Handle academic sessions, terms, and classes
- Subject management
- Curriculum organization

### Financial Management
- Create and manage student fee invoices
- Payment tracking with receipts
- Balance monitoring
- Bulk invoice generation

### Result Management
- Record student test and exam scores
- Grade calculation and management
- Academic performance tracking

### System Configuration
- Site-wide settings customization
- Default value configurations
- System preferences

### Security & Authentication
- Admin login for secure access
- User role management
- Secure data handling

### User Interface
- Responsive design with Bootstrap
- User-friendly dashboard
- Data tables with sorting and filtering
- Toast notifications

## Technologies Used

- **Backend**: Django 3.2+
- **Database**: SQLite (default), PostgreSQL/MySQL (configurable)
- **Frontend**: HTML5, CSS3, JavaScript
- **UI Framework**: Bootstrap 4/5
- **Icons**: Font Awesome
- **Data Tables**: DataTables
- **Notifications**: Toastr
- **Other**: jQuery, OverlayScrollbars

## Prerequisites

- Python 3.8 or higher
- pip (Python package installer)
- Git (for cloning the repository)

## Installation and Setup

### 1. Clone the Repository
```bash
git clone https://github.com/madhanmohanreddyperam06/School-Management-System.git
cd School-Management-System
```

### 2. Create Virtual Environment (Recommended)
```bash
python -m venv venv
# On Windows
venv\Scripts\activate
# On macOS/Linux
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Database Setup
```bash
python manage.py migrate
```

### 5. Create Superuser (Optional)
A default superuser is created during migration, but you can create additional ones:
```bash
python manage.py createsuperuser
```

### 6. Run Development Server
```bash
python manage.py runserver
```

### 7. Access the Application
Open your browser and navigate to: `http://127.0.0.1:8000/`

## Default Admin Credentials

A default superuser is created during the initial migration:
- **Username**: admin
- **Password**: admin123

> **Security Note**: Change the default password immediately after first login in a production environment.

## Usage

1. **Login**: Use admin credentials to access the dashboard
2. **Dashboard Navigation**:
   - Manage students, staff, and academic records
   - Handle financial transactions and invoices
   - View and manage student results
   - Configure site settings
3. **Bulk Operations**:
   - Upload student data using CSV files
   - Generate bulk invoices
   - Export reports
4. **Site Configuration**:
   - Set default academic sessions
   - Configure terms and classes
   - Customize system preferences

## Testing

Run the test suite to ensure everything is working correctly:
```bash
python manage.py test
```

Run tests for specific apps:
```bash
python manage.py test apps.corecode
python manage.py test apps.students
python manage.py test apps.staffs
python manage.py test apps.finance
python manage.py test apps.result
```

## Project Structure

```
School-Management-System/
├── apps/                          # Django apps
│   ├── corecode/                  # Core functionality
│   ├── students/                  # Student management
│   ├── staffs/                    # Staff management
│   ├── finance/                   # Financial management
│   └── result/                    # Result management
├── school_app/                    # Main Django project
│   ├── settings.py                # Django settings
│   ├── urls.py                    # URL configurations
│   ├── wsgi.py                    # WSGI configuration
│   └── asgi.py                    # ASGI configuration
├── static/                        # Static files (CSS, JS, images)
├── templates/                     # HTML templates
├── media/                         # User uploaded files
├── requirements.txt               # Python dependencies
├── manage.py                      # Django management script
├── db.sqlite3                     # SQLite database
└── README.md                      # Project documentation
```

## Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature-name`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin feature/your-feature-name`
5. Open a Pull Request

### Development Guidelines

- Follow PEP 8 style guidelines
- Write tests for new features
- Update documentation as needed
- Ensure all tests pass before submitting PR

### Code Formatting

Format your code using:
```bash
# Sort imports
isort .

# Format code
black .
```

## License

This project is licensed under the MIT License - see the [LICENSE.txt](LICENSE.txt) file for details.

## Security

For security policies and reporting vulnerabilities, please see [SECURITY.md](SECURITY.md).

## Roadmap

- [ ] Multi-language support (i18n)
- [ ] REST API for mobile app integration
- [ ] Advanced reporting and analytics
- [ ] Email notifications
- [ ] Student portal for self-service
- [ ] Parent-teacher communication module
- [ ] Integration with external systems (payment gateways, etc.)
- [ ] Mobile-responsive improvements
- [ ] Performance optimizations

## Support

If you have any questions or need help:

- Open an issue on GitHub
- Check the documentation
- Review existing issues for similar problems
- Mobile : 9110395993
- EmailID : madhanmohanreddyperam06@gmail.com

## Acknowledgments

- Django framework and community
- Bootstrap for UI components
- Font Awesome for icons
- All contributors and users

---

**Made with ❤️ for educational institutions**
