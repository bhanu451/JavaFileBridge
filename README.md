# JavaFileBridge

# 📁 Java Socket-Based File Transfer (Client-Server)

This project demonstrates a **Client-Server** file transfer system in **Java** using **TCP sockets**. It allows a user (client) to send files (text, image, audio, video, and document formats) to a server, which receives and stores them appropriately.

---

## 🚀 Features

- ✅ Supports multiple file types:
  - Text: `.txt`, `.java`, etc.
  - Binary: `.jpg`, `.jpeg`, `.png`, `.mp3`, `.mp4`, `.pdf`, `.docx`, `.ppt`
- ✅ Threaded server supports multiple simultaneous clients
- ✅ Simple GUI client using **Java AWT**
- ✅ Differentiates between text and binary files for handling

---

## 🖥️ Technologies Used

- Java SE (Socket, I/O, Threads)
- AWT (Abstract Window Toolkit) for GUI

---

## 📂 Project Structure


---

## ⚙️ How It Works

### 🔹 Server (`Server.java`)
- Listens on port **7860**
- Waits for incoming connections using `ServerSocket`
- For each client:
  - Accepts filename
  - Extracts file extension
  - If binary type, stores as `Recievedfile<filename>` (note: typo in prefix)
  - If text, writes to `ReceivedFile<filename>` using `PrintWriter`

### 🔹 Client (`Client.java`)
- Displays GUI to accept filename input
- Sends file name and data to server using `Socket`
- Displays success messages in the GUI `TextArea`

---

## 🛠️ How to Compile & Run

### 1 Start the Server

```bash
javac Server.java
java Server


```
## 2 Start the Client

```bash
javac Client.java
java Client
```
Input the full file name with extension (e.g., sample.txt, image.jpg)

Click Send to transfer the file

💡 Ensure the file exists in the client's local directory or provide the full path.
| File Type | Extension | Saved As (on server)     |
| --------- | --------- | ------------------------ |
| Image     | `.jpg`    | `Recievedfileimage.jpg`  |
| Text      | `.txt`    | `ReceivedFilesample.txt` |
| Audio     | `.mp3`    | `Recievedfileaudio.mp3`  |
| Document  | `.pdf`    | `Recievedfiledoc.pdf`    |

Server GUI
Serever_GUI.png
