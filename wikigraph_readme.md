# 🕸️ WikiGraph — Explore Knowledge Visually

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

**WikiGraph** is a full-stack web application that transforms traditional, linear Wikipedia browsing into an interactive, visual mind-map. Instead of clicking through endless blue links, WikiGraph allows you to visually discover the hidden connections between topics, making knowledge exploration intuitive, fast, and beautiful.

---

## ✨ Features

- **Interactive Knowledge Graph:** Topics are displayed as connected nodes. Drag, zoom, and explore the relationships dynamically.
- **Endless Exploration (Rabbit Hole):** Click on any related node (topic) to instantly center it and fetch its new connections.
- **Modern Dashboard UI:** A clean, responsive interface featuring a hero section, search bar, side navigation, and a detailed article view.
- **Lightning-Fast Backend:** Powered by **FastAPI**, ensuring rapid data fetching and processing from the Wikipedia API.
- **Real-Time Summaries:** Instantly read brief summaries of selected topics without leaving the dashboard.

---

## 🛠️ Technology Stack

**Backend**
- **Python:** Core programming language.
- **FastAPI:** High-performance web framework used to build the RESTful API.
- **Wikipedia API:** Used to fetch article summaries and hyperlinks.
- **Uvicorn:** ASGI web server for running the FastAPI application.

**Frontend**
- **HTML/CSS:** For structure and the modern dashboard layout.
- **Vanilla JavaScript:** Handles API requests and updates the UI dynamically.
- **Vis.js:** A powerful browser-based visualization library used to render the interactive physics-based network graph.

---

## 🚀 How It Works (Client-Server Architecture)

1. **User Search:** The user enters a topic in the frontend UI or clicks a node.
2. **API Request:** The JavaScript frontend sends a GET request to the local FastAPI backend.
3. **Data Processing:** The backend queries Wikipedia, cleans the data, trims the summary, and limits the links to prevent graph clutter.
4. **Graph Rendering:** The backend sends a clean JSON response back to the frontend, which uses `Vis.js` to animate and draw the interactive map.

---

## 💻 Installation & Setup

Follow these steps to run WikiGraph locally on your machine.

### Prerequisites
- Python 3.8+ installed on your system.
- A web browser (Chrome, Firefox, Edge).

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/WikiGraph.git
cd WikiGraph
```

### 2. Install Backend Dependencies
It is recommended to use a virtual environment. Install the required Python packages:
```bash
pip install fastapi uvicorn wikipedia
```

### 3. Start the FastAPI Server
Run the following command to start the backend server:
```bash
uvicorn main:app --reload
```
*The server will start running at `http://127.0.0.1:8000`.*

### 4. Open the Application
Simply double-click the `index.html` file in your project folder to open it in your web browser. 

*Alternatively, if you have VS Code installed, you can use the "Live Server" extension to open the HTML file.*

---

## 📂 Project Structure

```text
WikiGraph/
│
├── main.py              # FastAPI backend logic and Wikipedia data processing
├── index.html           # Frontend UI, Dashboard layout, and Vis.js implementation
├── README.md            # Project documentation
└── requirements.txt     # List of Python dependencies
```

---

## 🔮 Future Enhancements

- **Bi-directional Search (Pathfinder):** Implement LeetCode-style Breadth-First Search (BFS) to find the shortest path between two entirely different Wikipedia topics.
- **Multi-language Support:** Allow users to search and generate graphs in languages other than English.
- **Save/Export Graphs:** Allow users to export their explored knowledge graphs as images or PDF files.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page if you want to contribute.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

*Made for the love of open knowledge and visual learning.* 🌍📘