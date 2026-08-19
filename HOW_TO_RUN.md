# How to Run Locally

This guide is for setting up and running the Student Management System on your local computer using **MySQL Workbench**.

## Prerequisites
- Python 3.x
- MySQL Workbench

---

### Step 1: Set up the Database
1. Open **MySQL Workbench**, connect to your local instance, and log in.
2. In the top toolbar, click the **Create a new schema** button (the yellow cylinder with a plus icon).
3. Name the schema **`students`** (all lowercase) and click **Apply**, then **Apply** again.
4. Go to **File -> Open SQL Script...** and select the `students.sql` file from the `student management` folder.
5. In the left "Schemas" panel, right-click the `students` schema you just created and select **Set as Default Schema** (it will turn bold).
6. Click the yellow lightning bolt icon (⚡) at the top of the script window to execute the script and create your tables.

### Step 2: Update your Database Password (If applicable)
By default, the code expects your MySQL root user to not have a password. If you typed in a password to log into MySQL Workbench, you must update the code:
1. Open `student management/main.py`.
2. Go to line 26:
   ```python
   app.config['SQLALCHEMY_DATABASE_URI']='mysql://root:@localhost/students'
   ```
3. If your password is, for example, `1234`, change it to:
   ```python
   app.config['SQLALCHEMY_DATABASE_URI']='mysql://root:1234@localhost/students'
   ```
4. Save the file.

### Step 3: Install Required Packages
Open a new terminal window inside the `student management` folder and install the necessary Python dependencies:
```bash
pip install -r requirements.txt
```

### Step 4: Run the Application
In that same terminal, start the server by running:
```bash
python main.py
```
Your terminal will print out a local web address (usually `http://127.0.0.1:5000/`). Ctrl-click that link or open it in your web browser to view your project!
