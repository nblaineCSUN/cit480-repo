Flask/gunicorn running on local host
PostgreSQL database running on a linux VM on same network

TWO SCRIPTS - app.py/dbscript.py

app.py
- Runs the flask app.
- imports dbscript for use
- creates very basic html page with a button that reads "Run Script"
- This button sends a POST
- Then the underlying code check if request.method == "POST"
- if it does, try: dbscript.run()
- prints results on webpage

dbscript.py
- logic contained in function run() # hence the dbscript.run() call
- This function simply connects to the hosted PostgreSQL database and runs a query for all entries in table
