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


## Future Enhancements
- Adding **AI opponent** with Minimax algorithm.  
- Adding **chat functionality** during gameplay.  
- Adding **custom themes** and board skins.  
- Implementing **leaderboard and achievements**.  
- Extending to **mobile platforms (Android/iOS)**.  

---

## License
This project is open-source and available under the **MIT License**.
