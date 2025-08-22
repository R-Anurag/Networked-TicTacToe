# Networked Tic Tac Toe — Java (Swing + TCP Sockets)

**Networked Tic Tac Toe** is a Java application that implements the classic Tic-Tac-Toe game with a **client–server architecture**.  
The UI is built with **Swing**, while networking uses **TCP sockets** to synchronize game state between a host (server) and one or more clients over LAN.

---

## Features
- **Multiplayer over Network**: Server-client model using TCP sockets.  
- **Interactive GUI**: Built with Java Swing, featuring rounded buttons and custom icons.  
- **Sound Effects**: Background music and effects integrated using `.wav` files.  
- **Robust Design**: Handles invalid moves, turn synchronization, and disconnection gracefully.  
- **Cross-Platform**: Runs on any machine with Java 8+ installed.

---

## Project Structure
```
networkedTicTacToe/
│── src/io/github/rAnurag/
│   ├── Server.java            # Launches the game server
│   ├── ClientHandler.java     # Manages communication between server & clients
│   └── TicTacToe.java         # GUI and client-side logic
│
│── res/                       # Resources (images, audio)
│   ├── replayIcon.png
│   ├── backgroundMusic.wav      
│   └── backgroundMusic2.wav
│
├── .gitignore
├── .classpath
├── .project
```

---

## Requirements
- **Java 8+** (JDK installed and configured in PATH)
- A terminal or IDE (Eclipse/IntelliJ/VS Code) to run the project

---

## Running the Project

1. **Clone the repository**
   ```bash
   git clone https://github.com/R-Anurag/Networked-TicTacToe.git
   cd networkedTicTacToe
   ```

2. **Compile the source files**
   ```bash
   javac -d bin src/io/github/rAnurag/*.java
   ```

3. **Start the server**
   ```bash
   java -cp bin io.github.rAnurag.Server
   ```

4. **Start a client**
   ```bash
   java -cp bin io.github.rAnurag.TicTacToe
   ```

5. Run another client instance to simulate Player 2.  
   Both clients will connect to the server and be able to play Tic Tac Toe.

---

### How to Play with Friends

1. **Start the Server (Host Player – You):**  
   - On **your computer**, run **`Server.java`** → this creates the game server.  
   - Then, also run **`TicTacToe.java`** → this starts your game client.  
   - When asked, enter:  
     - **Username** → your name  
     - **IP Address** → `localhost`  
     - **Port** → choose any number `>= 1024` (e.g., `1234`)  

2. **Join the Game (Friend Player):**  
   - On your **friend’s computer**, run **`TicTacToe.java`** (⚠️ do **not** run `Server.java`).  
   - When asked, enter:  
     - **Username** → friend’s name  
     - **IP Address** → your computer’s **LAN IPv4 address** (e.g., `192.168.x.x`)  
     - **Port** → the **same port number** you used (e.g., `1234`)  

3. **Play Together!**  
   - The server running on your machine connects both players.  
   - Every move you or your friend makes is updated live on both boards.  

💡 **Extra Tips:**  
- If **both players are on the same computer**:  
  - Run the server once (`Server.java`)  
  - Run two clients (`TicTacToe.java`)  
  - Both clients should use: `IP = localhost` and the same port.  
- Make sure both computers are on the **same local network (LAN/Wi-Fi)**.  
- If firewalls block the connection, allow Java through the firewall.  

---

## Example Connection Setup
Two players connect via username, IP, and port.
<img width="811" height="550" alt="connection" src="https://github.com/user-attachments/assets/ec8aaceb-54ae-44ff-a27b-742fbde272f4" />

---

## Future Enhancements
- Adding **AI opponent** with Minimax algorithm.  
- Adding **chat functionality** during gameplay.  
- Adding **custom themes** and board skins.  
- Implementing **leaderboard and achievements**.  
- Extending to **mobile platforms (Android/iOS)**.  

---

## License
This project is open-source and available under the **MIT License**.
