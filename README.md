# MSSQL_Excel_Exporter
A Python desktop application designed to streamline SQL execution and reporting for MS SQL Server environments. Built for finance and data teams needing fast, repeatable workflows.

## Features

- **Direct SQL Input**: Execute SQL queries directly in the application
- **SQL File Support**: Load and execute .sql files
- **ODBC Connection**: Secure connection to MS SQL Server with credential management
- **One-Click Export**: Export query results to Excel instantly
- **User-Friendly Interface**: Simple, intuitive desktop GUI

---

## Prerequisites

- Python 3.8 or higher
- MS SQL Server access
- ODBC Driver for SQL Server

## Install ODBC Driver (if not already installed)

- Download from [Microsoft ODBC Driver for SQL Server](https://docs.microsoft.com/en-us/sql/connect/odbc/download-odbc-driver-for-sql-server)

---

## Basic Workflow

1. **Connect to Database**
   - Enter server name
   - Enter database name
   - Provide credentials (Windows Auth or SQL Auth)
   - Click "Connect"

2. **Execute SQL Query**
   - Type SQL directly in the query box, OR
   - Click "Load SQL File" to import a .sql file
   - Click "Execute Query"

3. **Export Results**
   - Review results in the data grid
   - Click "Export to Excel"
   - Choose save location
   - Excel file generated instantly

---

## Configuration

### Connection String Options

The application supports various connection methods:

**Windows Authentication:**
```python
DRIVER={ODBC Driver 18 for SQL Server};
SERVER=your_server;
DATABASE=your_database;
Trusted_Connection=yes;
```

**SQL Server Authentication:**
```python
DRIVER={ODBC Driver 18 for SQL Server};
SERVER=your_server;
DATABASE=your_database;
UID=your_username;
PWD=your_password;
```

---

## Troubleshooting

### Common Issues

**ODBC Driver Not Found:**
- Ensure ODBC Driver 18 for SQL Server is installed
- Check available drivers: `pyodbc.drivers()`

**Connection Failed:**
- Verify server name and database name
- Check firewall settings
- Ensure SQL Server allows remote connections
- Verify authentication method (Windows vs SQL)

**Excel Export Error:**
- Ensure openpyxl is installed
- Check write permissions for export directory
- Verify sufficient disk space

---

**Screenshots
