<div align="center">

# Traffix ⚖️🔀  
## **Smart TCP Traffic Distributor**

A lightweight, educational **TCP load balancer** written in pure Python.  
Distributes incoming client connections across multiple backend servers using **Round Robin** (default) or **Random** selection — perfect for learning networking, sockets, and load balancing fundamentals.

</div>

## ✨ Features

- 🔄 **Round Robin** (default) & **Random** backend selection
- 🔌 Bidirectional TCP proxying (client ↔ backend)
- 📡 Uses non-blocking I/O with `select()` — efficient for many connections
- 🗂️ Connection tracking (flow table) to keep sessions sticky
- 📝 Clean logging: connections, bytes transferred, disconnections
- ⚡ Super lightweight — no external dependencies!

## 🛠️ Tech Stack

- **Python 3.x** (standard library only)
- `socket` + `select` for multiplexing
- No frameworks — pure sockets magic!

## 🚀 Quick Start

### 1. Start the backend servers

Open two terminals:

  ```bash
  # Backend 1
  python backend_server1.py 8888

  # Backend 2
  python backend_server2.py 9999

  # Launch Traffix (the load balancer)
  python loadbalancer.py

It listens on port 5555 by default.
