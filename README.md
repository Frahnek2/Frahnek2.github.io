# Birthday Gift Web App

A simple, interactive, and aesthetic web application designed as a digital birthday gift. It features a clickable present that opens to reveal personalized images, along with celebratory confetti animations!

## Features

- **Interactive Design:** Click the gift box to reveal surprises.
- **Animations:** Dynamic confetti effects using the `canvas-confetti` library.
- **Aesthetic UI:** Beautiful modern typography (Google Fonts 'Outfit') and smooth CSS transitions.
- **Dockerized:** Easily deployable anywhere using Docker and Nginx.

## Project Structure

- `birthday_app/` - Contains the source code of the web app.
  - `index.html` - The main structure of the web page.
  - `styles.css` - Custom styles, layouts, and animations.
  - `script.js` - Logic for interactions and confetti effects.
  - `assets/` - Images and graphical assets used in the app.
  - `Dockerfile` - For building the Docker container using a lightweight Nginx web server.

## Getting Started

### Prerequisites

Make sure you have [Docker](https://docs.docker.com/get-docker/) installed on your machine.

### Running the App Locally

1. Open your terminal and navigate to the `birthday_app` directory:
   ```bash
   cd birthday_app
   ```

2. Build the Docker image:
   ```bash
   docker build -t birthday-app .
   ```

3. Run the container (mapping container port 80 to your local port 8080):
   ```bash
   docker run -d -p 8080:80 birthday-app
   ```

4. Access the web app:
   Open your browser and navigate to `http://localhost:8080`.

### Accessing from a Mobile Device

To access the app from a phone or tablet on the same Wi-Fi network:

1. Find your computer's local network IP address (usually looks like `192.168.x.x` or `10.0.x.x`):
   - On **Linux** / **macOS**: Run `ip a` or `ifconfig`
   - On **Windows**: Run `ipconfig`
2. Ensure the Docker container is running and mapped to a port (e.g., `8080`).
3. Open a browser on your mobile device and navigate to `http://<YOUR_LOCAL_IP>:8080`.
