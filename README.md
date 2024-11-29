# Online-Collaborative-Whiteboard
This application will allow multiple users to draw, annotate, and interact with each other in real-time on a shared whiteboard. Each user will be able to:

-Draw freely using a pen tool.
-See the drawings of others in real time.
-Choose different colors and line thicknesses.
-Clear the whiteboard or reset it.

The server will handle multiple clients and broadcast their drawing actions to other connected clients.

Project Structure

-Server: Manages connections, handles client messages, and broadcasts drawing data to all connected clients.
-Client: A JavaFX-based GUI that allows users to draw on the whiteboard and communicate with the server.
-Shared Whiteboard: All clients can see each other's drawing actions in real time.

How the Application Works
Server Side:

-The WhiteboardServer listens for incoming client connections.
-Each new client creates a ClientHandler thread that handles communication between the server and the client.
-When the server receives drawing data from a client (e.g., coordinates of the lines), it broadcasts the data to all connected clients.

Client Side:

-The WhiteboardClient application creates a JavaFX canvas where users can draw.
-When a user draws, the client sends the drawing coordinates (start and end points) to the server.
-The server then broadcasts this data to all connected clients, allowing them to see the drawing in real-time.
