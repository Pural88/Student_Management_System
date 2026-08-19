# Student Management System

This is a Student Management System built using Flask (Python) and MySQL.

## Prerequisites
- Python 3.x
- MySQL Server (e.g., XAMPP, WAMP, or standalone MySQL)

## How to run locally

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Pural88/Student_Management_System.git
   cd Student_Management_System/"student management"
   ```

2. **Install requirements:**
   Install the required Python packages using pip:
   ```bash
   pip install -r requirements.txt
   ```
   *(Note: It is recommended to use a virtual environment)*

3. **Database Setup:**
   - Create a MySQL database (check `main.py` for the required database name, usually it matches what is in `students.sql` or the connection string in `main.py`).
   - Import the `students.sql` file into your MySQL database to set up the necessary tables.

4. **Run the Application:**
   Run the Flask server:
   ```bash
   python main.py
   ```
   The application will typically start on `http://127.0.0.1:5000/`. Open this URL in your web browser.

## Deployment
While this project can be run locally for development and testing, it is fully deployable to cloud platforms like Heroku, AWS, or PythonAnywhere. Ensure you configure your production database connection strings and environment variables appropriately before deploying.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
