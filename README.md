# 🚀 Real-Time ChatRoom Application

A lightweight, fast, real-time chat application built using **Spring Boot**, **WebSockets**, and **STOMP**. Users can join a common chatroom and exchange messages instantly — no page refresh required.

---

## ✨ Features

* ⚡ **Real-time messaging** using Spring WebSockets
* 💬 **Broadcast chatroom** for all connected users
* 🧑‍🤝‍🧑 Live user join/leave notifications
* 🟢 **Instant UI updates** using STOMP over WebSocket
* 🔧 Easy to run — no database needed
* 🪶 Lightweight backend with minimal configuration

---

## 🛠️ Tech Stack

| Layer      | Technology               |
| ---------- | ------------------------ |
| Backend    | Spring Boot 3.x          |
| Real-time  | Spring WebSocket + STOMP |
| Messaging  | SimpleBroker             |
| Build Tool | Maven                    |
| Runtime    | Java 21                  |

---

## 📸 Screenshots

> <img width="1920" height="1080" alt="Screenshot (6)" src="https://github.com/user-attachments/assets/c4048172-17c3-4bf7-94b8-25e92e75b437" />



<img width="1920" height="1080" alt="Screenshot (7)" src="https://github.com/user-attachments/assets/a668f394-771a-4c7c-bf52-ec407b948f1d" />



```
/screenshots
 ├── home.png
 ├── chatroom.png
 └── message-demo.png
```

---

## 🎥 Demo GIF

> Example placeholder:

```
/demo/demo.gif
```

---

# ⚙️ Installation & Setup

### **1️⃣ Clone the Repository**

```sh
git clone https://github.com/your-username/chatroom-app.git
cd chatroom-app
```

### **2️⃣ Build the Project**

```sh
mvn clean install
```

### **3️⃣ Run the Server**

```sh
mvn spring-boot:run
```

Server starts on:

```
http://localhost:8080
```

---

# 🚦 How It Works

### **🛰️ WebSocket Endpoints**

| Endpoint                | Description                      |
| ----------------------- | -------------------------------- |
| `/ws`                   | WebSocket handshake endpoint     |
| `/app/chat.sendMessage` | STOMP endpoint to send messages  |
| `/app/chat.addUser`     | STOMP endpoint when user joins   |
| `/topic/public`         | Broadcast topic for all messages |

---

## 📡 Message Payload Example

### **Send message**

```json
{
  "sender": "Tusharika",
  "content": "Hello everyone!",
  "type": "CHAT"
}
```

### **User joins**

```json
{
  "sender": "Tusharika",
  "type": "JOIN"
}
```

---

# 🗂️ Project Structure

```
src/
 └── main/
      ├── java/com/chatapp/
      │      ├── controller/
      │      ├── config/
      │      ├── model/
      │      └── handler/
      └── resources/
            ├── static/
            └── application.properties
```

---

# 🚀 Build for Production

You can package your app into a runnable JAR:

```sh
mvn clean package
```

Then run:

```sh
java -jar target/chatroom-0.0.1-SNAPSHOT.jar
```

---

# 🛡️ Future Improvements (Optional Section)

* 👤 Private DM between users
* 🧵 Multiple chat rooms
* 🔐 JWT Authentication
* 🎨 UI redesign with React/Next.js
* 💾 Save chat history in database

---

# 🤝 Contributing

Pull requests are welcome!
Feel free to open issues for features or bugs.

---

# 📄 License

This project is licensed under the **MIT License**.

---

