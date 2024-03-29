# Flask DB Requests

This is a ***straightforward*** application consists of a `server` (**stores information about tasks**) and a `client` (**that makes requests to the server to query/modify the database**).

To interact with the application, refer to the provided endpoints and their functionalities documented in the task description table. You can use the client script or tools like `Postman` to test the server endpoints.

**Server URL:** [http://127.0.0.1:5000/](<http://127.0.0.1:5000/>)

**Type of (`Operations` - `Requests`):**

| **Operation**           | URL                                          |**Type**| Request Body                  | Response                     |
|:-----------------------:|----------------------------------------------|:------:|-------------------------------|------------------------------|
| **Sanity**              | [.../sanity](<http://127.0.0.1:5000/sanity>)               |**GET** | `{}`                          | `{"status_code": "200"}`     |
| **Add Task**            | [.../add](<http://127.0.0.1:5000/add>)                 |**POST**| `Task ObjectNode`                 | `{"status_code": "200"}`  |
| **Print Tasks**          | [.../print](<http://127.0.0.1:5000/>)              |**GET**| `{}`                          | **JSON** with all tasks   |
| **Print Completed Tasks**| [.../print/completed](<http://127.0.0.1:5000/print/completed>)    |**GET**| `{}`                          | **JSON** with completed tasks |
| **Delete Task**         | [.../delete/id](<http://127.0.0.1:5000/delete/id>)      |**DELETE**| `{}`                          | `{"status_code": "200"}`     |
| **Delete All Tasks**     | [.../delete/all](<http://127.0.0.1:5000/delete/all>)       |**DELETE**| `{}`                          | `{"status_code": "200"}`     |
| **Update Task**          | [.../update/id](<http://127.0.0.1:5000/update/id>)        |**POST**| `{}`                          | `{"status_code": "200"}`     |
| **Update Task Assignee** | [.../update/id/name](<http://127.0.0.1:5000/update/id/name>)     |**POST**| `{}`                          | `{"status_code": "200"}`     |
| **Save**                 | [.../save](<http://127.0.0.1:5000/save>)               |**POST**| `{}`                          | `{"status_code": "200"}`     |
| **Load**                 | [.../load](<http://127.0.0.1:5000/load>)               |**POST**| `{}`                          | `{"status_code": "200"}`     |

**Note:** `save` and `load` operations save and load the state of the database respectively in a JSON file `database.json`.

## Usage and Setup

### Windows

1. Open a terminal and follow these steps:
   - Create a Virtual Environment: `py -3 -m venv venv`
   - Activate the Virtual Environment: `venv\Scripts\activate`
   - Install Flask: `pip install Flask`
   - Install Requests: `pip install requests`

### Linux/Mac OS

1. Open a terminal in `flask-db-requests` and follow these steps:
   - Create a Virtual Environment: `python3 -m venv venv`
   - Activate the Virtual Environment: `chmod +x venv/bin/activate` then `./venv/bin/activate`
   - Install Flask: `pip install Flask`
   - Install Requests: `pip install requests`

### Running the Application

1. Once the virtual environment is set up, use the following commands to run the server and client:
   - Start the Server: `python3 -m flask --app server run`
   - Start the Client: `python3 client.py`
