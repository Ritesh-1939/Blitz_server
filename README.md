# Blitz: Multithreaded Web Server in C++

Blitz is a custom-built multithreaded web server implemented in C++ using the Winsock API for Windows. It supports file uploads and downloads through a user-friendly web interface and handles simultaneous client requests using multithreading.

## 🚀 Features

- 📂 Upload support for:
  - Text files
  - Audio files
  - Video files (e.g., `.mp4`)
- ⬇️ File download support
- ⚡ Handles multiple clients concurrently (multithreaded)
- 🧠 Built from scratch using:
  - **C++**
  - **Windows Sockets (Winsock)**
- 🌐 Frontend built using HTML/CSS/JavaScript
- 🗃️ Uploaded files stored in `www/files/` directory

## 🗂️ Project Structure

Blitz_server/
├── Server.cpp # Sets up socket and listens for connections
├── Handler.cpp # Processes client requests (upload/download)
├── Utils.cpp # Utility functions (parsing, path, etc.)
├── Globals.hpp # Shared configuration and constants
├── www/ # Web root (HTML interface + uploaded files)
│ ├── index.html # Main upload/download page
│ └── files/ # Folder where uploaded files are saved
└── .vscode/ # VSCode config (optional)


## 🛠️ How It Works

1. Server starts on a specific port and listens for incoming connections.
2. When a user accesses the web page, they can upload or download files.
3. Uploads are parsed via `multipart/form-data` and saved to `www/files/`.
4. Multithreading ensures multiple users can interact with the server simultaneously.

## 🧪 How to Run

### 🖥️ Prerequisites
- Windows OS
- C++ Compiler (e.g., MSYS2 with `g++`)
- Winsock development libraries

### 🔧 Build and Run

```bash
g++ Server.cpp Handler.cpp Utils.cpp -o BlitzServer -lws2_32 -std=c++17
./BlitzServer
Then open your browser and visit:

http://localhost:8080
👨‍💻 Team Members
Ritesh (Lead Developer)

[Virajita Panwar & Harshmani Kumar]


📜 License
This project is open-source and available under the MIT License.