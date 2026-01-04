# 🌍 World Chat - Real-Time Chat Application

A Flask-based real-time chat application using WebSockets (Flask-SocketIO) for instant messaging.

## 🚀 Quick Start

### Prerequisites
- Python 3.7 or higher
- pip (Python package manager)

### Installation & Running

1. **Navigate to project directory:**
   ```bash
   cd "c:\Users\Psychozz\Downloads\Compressed\world chat\world_chat"
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirments.txt
   ```
   
   *If `pip` is not recognized, try:*
   ```bash
   python -m pip install -r requirments.txt
   ```
   or
   ```bash
   python3 -m pip install -r requirments.txt
   ```

3. **Run the application:**
   ```bash
   python app.py
   ```
   or
   ```bash
   python3 app.py
   ```

4. **Access the app:**
   Open your browser and go to:
   - **http://localhost:5000**
   - **http://127.0.0.1:5000**

## 📦 Dependencies

- **Flask 2.2.5** - Web framework
- **Flask-SocketIO 5.3.6** - WebSocket support for real-time communication
- **python-socketio 5.8.0** - Socket.IO client/server
- **python-engineio 4.7.1** - Engine.IO backend
- **eventlet 0.33.3** - Async server backend
- **Flask-Session 0.8.0** - Session management
- **Flask-SQLAlchemy 3.1.1** - Database ORM (optional)
- **bcrypt 3.2.0** - Password hashing (optional)
- **requests 2.25.1** - HTTP library

## 🎯 Features

- ✅ Real-time messaging using WebSockets
- ✅ Username-based chat sessions
- ✅ User join notifications
- ✅ Instant message delivery to all connected users
- ✅ Session management

## 🔧 Troubleshooting

### Python not found
If you get "Python was not found", install Python from [python.org](https://www.python.org/downloads/) and make sure to check **"Add Python to PATH"** during installation.

### Port already in use
If port 5000 is already in use, modify `app.py` line 51:
```python
socketio.run(app, host='0.0.0.0', port=5001)  # Change port number
```

### Dependencies installation fails
Try installing dependencies individually:
```bash
pip install Flask==2.2.5
pip install Flask-SocketIO==5.3.6
pip install eventlet==0.33.3
```

## 📁 Project Structure

```
world_chat/
├── app.py              # Main Flask application
├── requirments.txt     # Python dependencies
├── vercel.json         # Vercel deployment config
├── static/             # Static files (CSS, JS, images)
├── templates/          # HTML templates
│   ├── index.html      # Login/username entry page
│   └── chat.html       # Chat room page
└── README.md           # This file
```

## 🌐 Deployment

This project includes a `vercel.json` file for deployment on Vercel. You can also deploy to:
- Heroku
- Railway
- PythonAnywhere
- Any server supporting Python and WebSockets

## 📝 Usage

1. Open the application in your browser
2. Enter a username on the home page
3. Click to join the chat room
4. Start sending messages in real-time!
5. Open multiple browser windows to test multi-user chat

## 🔐 Security Notes

- The current `secret_key` is set to `"hie"` - **change this in production!**
- Update line 7 in `app.py` with a secure random key:
  ```python
  app.secret_key = "your-secure-random-secret-key-here"
  ```

## 📄 License

This project is open source and available for educational purposes.

---

**Enjoy chatting! 💬**
