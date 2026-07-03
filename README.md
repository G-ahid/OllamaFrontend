# What It Is

This project is a lightweight, local web interface designed to interact with a self-hosted Ollama, think of it a lightweight version of OpenWebUI, but without all the features.

# Minimalist Local Web Stack

A lightweight, transparent web application setup with a clean decoupled frontend, middleware router, and straightforward bash scripts to get up and running locally or over the cloud via a Cloudflare tunnel.

## Project Structure

Here is a quick look at how the project files are laid out:

```text
├── index.html        # Main web interface entry point
├── style.css         # Styling for the interface
├── frontend.js       # Client-side UI interactions
├── middleend.js      # Internal request routing / middleware logic
├── config.json       # App configurations 
├── run.sh            # Starts the Cloudflare tunnel mapping
├── run_server.sh     # Primary script to start the local backend server
├── server.log        # Generated runtime application logs
└── ico.jpeg          # Project favicon asset

```

---

## How It Works

* **The Frontend (`index.html`, `style.css`, `frontend.js`)**: A straightforward browser-side client interface handling UI presentation and capturing user interactions.
* **The Middleware (`middleend.js`)**: An intermediate JavaScript processing layer that sits comfortably between your raw frontend actions and any backend processing/config management.
* **Exposing the Server (`run.sh`)**: For quick remote sharing or testing, this script boots a Cloudflare tunnel pointing right to a local port (e.g., standardizing local port maps like `:11434`).

---

## Getting Started

### 1. Launching the Server

To spin up the primary service stack locally and begin tracking application details inside `server.log`, execute:

```bash
chmod +x run_server.sh
./run_server.sh

```

### 2. Exposing Locally via Cloudflare

If you want to proxy your local environment to a public URL securely without touching router port-forwarding configs, run the tunneling script:

```bash
chmod +x run.sh
./run.sh

```

---

## Configuration

Tweak system behaviors, default api connections, or constants directly by opening up and adjusting settings inside:

```json
// config.json
{
  ...
}

```
