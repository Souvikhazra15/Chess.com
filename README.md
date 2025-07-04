# Chess Game

A real-time multiplayer chess game built using Node.js, Express, and Socket.IO.

## Installation

1. Clone the repository:
```
git clone https://github.com/your-username/chess-game.git
```

2. Install the dependencies:
```
cd chess-game
npm install
```

3. Start the server:
```
npm start
```

The server will start running on `http://localhost:3000`.

## Usage

1. Open your web browser and navigate to `http://localhost:3000`.
2. The first two players to connect will be assigned as the "white" and "black" players, respectively. Any additional players will be assigned as "spectators".
3. The white player makes the first move, and the game continues with the players taking turns.
4. The game board and moves are updated in real-time for all connected players.

## API

The application uses Socket.IO to handle real-time communication between the client and server. The following events are emitted:

- `connection`: Emitted when a new client connects to the server.
- `disconnect`: Emitted when a client disconnects from the server.
- `move`: Emitted when a player makes a valid move. The move is passed as an argument.
- `boardState`: Emitted after a valid move is made, sending the current state of the chess board in FEN notation.
- `playerRole`: Emitted to a new client, informing them of their role (white, black, or spectator).
- `Invalid move`: Emitted when a client attempts an invalid move.

## Contributing

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push your branch to your forked repository.
5. Submit a pull request to the original repository.

## License

This project is licensed under the [MIT License](LICENSE).

## Testing

To run the tests, execute the following command:

```
npm test
```

The tests cover the basic functionality of the chess game, including valid and invalid moves, player roles, and board state updates.
