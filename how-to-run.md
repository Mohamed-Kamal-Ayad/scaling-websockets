1. build this image as "docker build -t wsapp ."
2. than run docker-compose up
3. open a browser console and type this

let ws = new WebSocket("ws://localhost:8080");
ws.onmessage = message => console.log(`Received: ${message.data}`);
ws.send("Hello! I'm client")

4. open multiple console windows to simulate multiple clients
