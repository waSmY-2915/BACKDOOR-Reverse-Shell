# Prerequisites

Before working with the **Backdoor (Reverse Shell) Using Python** project, you should have a basic understanding of Python programming, networking, and operating-system concepts.

The project uses only Python's standard library, so there are no external packages that need to be installed. The main requirement is understanding the concepts used by `client.py` and `server.py`.

## 1. Python Basics

You should be comfortable with:

* Variables and data types
* Functions
* Conditional statements
* Loops
* Modules and imports
* Exception handling
* Working with strings and bytes

The project requires basic Python knowledge because both the client and server are implemented in Python.

## 2. Networking Fundamentals

Understand the basics of:

* IP addresses
* Ports
* TCP/IP
* Client-server architecture
* Network connections
* IPv4 addressing

You should understand the difference between a normal client-server connection, a bind shell, and a reverse shell.

### Basic Socket Concepts

The project uses:

```python
socket.AF_INET
socket.SOCK_STREAM
```

`AF_INET` is used for IPv4 communication, while `SOCK_STREAM` provides TCP-based communication.

## 3. Socket Programming

You should understand the basic Python socket functions:

```python
socket()
bind()
listen()
accept()
connect()
send()
recv()
```

The server uses functions such as `bind()`, `listen()`, and `accept()` to wait for connections, while the client uses `connect()` to establish the connection.

A simple client-server socket exercise should be completed before attempting the full project.

## 4. JSON

The project uses JSON for exchanging structured information between the client and server.

You should understand:

```python
json.dumps()
json.loads()
```

`json.dumps()` converts Python data into a JSON string, while `json.loads()` converts JSON data back into Python objects.

## 5. Command Execution

Basic knowledge of Python's `subprocess` module is required.

You should understand concepts such as:

```python
subprocess.Popen()
stdout
stderr
```

The client uses subprocess functionality to process commands received through the socket connection.

## 6. File and Directory Operations

You should be familiar with:

```python
os.chdir()
os.getcwd()
open()
```

You should also understand reading and writing files in binary mode:

```python
open("file.txt", "rb")
open("file.txt", "wb")
```

These concepts are used for directory navigation and file operations within the project.

## 7. Base64 Encoding

Basic knowledge of Base64 encoding and decoding is useful for understanding the file-transfer functionality.

Important functions include:

```python
base64.b64encode()
base64.b64decode()
```

Base64 converts binary data into a text representation that can be transmitted through the socket connection and converted back on the receiving side.

> **Note:** Base64 is an encoding mechanism, not encryption.

## 8. Exception Handling

You should understand Python's:

```python
try:
    ...
except:
    ...
```

Exception handling is important for managing connection failures, invalid data, and other runtime errors.

## 9. Retry Logic

The client uses retry logic to handle situations where the server is temporarily unavailable.

You should understand:

```python
time.sleep()
```

along with loops and exception handling.

## 10. Recommended Lab Environment

For learning and testing, use an isolated environment such as:

* Your own computer
* Two virtual machines
* A private lab network
* Loopback address (`127.0.0.1`)

For initial testing, using:

```text
127.0.0.1:4444
```

keeps the communication on the local machine.

## 11. Basic Tools

You should have:

* **Python 3**
* A terminal or command prompt
* A code editor such as VS Code
* Basic Linux or Windows command-line knowledge

No external Python packages are required because the project uses Python's standard library.

## 12. Recommended Learning Order

A good order for preparing for this project is:

```text
Python Basics
      ↓
Networking Fundamentals
      ↓
TCP/IP & Ports
      ↓
Python Socket Programming
      ↓
JSON Serialization
      ↓
Command Execution
      ↓
File & Directory Operations
      ↓
Base64 Encoding
      ↓
Exception Handling
      ↓
Retry Logic
      ↓
Client-Server Testing
      ↓
Reverse Shell Concepts
```

## Safety Note

Practice this project only in an environment where you have explicit authorization.

For initial experiments, use `127.0.0.1` or an isolated virtual lab rather than connecting to third-party systems. The project source itself recommends local or controlled-network testing to avoid legal and ethical issues.
