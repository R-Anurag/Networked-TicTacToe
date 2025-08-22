# Networked Tic Tac Toe — Java (Swing + TCP Sockets)

**Networked Tic Tac Toe** is a Java application that implements the classic Tic-Tac-Toe game with a **client–server architecture**.  
The UI is built with **Swing**, while networking uses **TCP sockets** to synchronize game state between a host (server) and one or more clients over LAN.

---

## Project Structure

```
networkedTicTacToe/
├── res/                    # Assets (images, audio, etc.)
├── src/io/github/rAnurag/
│   ├── ClientHandler.java  # Handles communication with each client
│   ├── Server.java         # Server logic for managing connections
│   └── TicTacToe.java      # Main game logic / client UI
├── .classpath
├── .project
└── .gitignore
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

## License
This project is open-source and available under the **MIT License**.
