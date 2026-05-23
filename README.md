# 📝 Jotter — Lightweight Desktop Text Editor

Jotter is a clean, multi-window text editor built from scratch in Java. Think of it like a lightweight Notepad but upgraded with rich-text features, inline images, and a live search highlighting engine. 

![Java](https://img.shields.io/badge/Language-Java-red?style=flat-square)
![GUI](https://img.shields.io/badge/GUI-Swing%20%2F%20AWT-orange?style=flat-square)

---

## ⚡ Core Features

* **File Serialization:** Full control over file operations—built using robust read/write stream pipelines to safely open, save, and print documents.
* **Live Document Metrics:** A dynamic status bar that parses text tokens in real-time to display character and word counts on the fly using listener hooks.
* **Multi-Threading:** Built to handle multiple windows running at the same time on separate execution threads.

---

## 🛠️ My Specific Contributions

This was a group project at CPUT, but I owned the engineering behind these core modules:

### 🔍 1. Search Panel & Token Highlighting Engine
* **How it works:** Built a text-searching routine that scans the document model to find keyword matches.
* **The Tech:** Calculated character offsets inside the text component to apply a background painter highlight overlay to all matches simultaneously without freezing the UI thread.

### 🖼️ 2. Inline Image Ingestion Pipeline
* **How it works:** Implemented a system that lets users drop images directly into the text field.
* **The Tech:** Managed the input parsing logic to stream, read, and render external image files inline within the document's layout boundaries.

### 🎨 3. UI Assets & Icon Design
* Designed the vector graphics, desktop application icon, and overall branding system for Jotter.

---

## 💻 Tech Stack & Core APIs

* **Language:** Java SE
* **GUI Layer:** **Java Swing** — Used for the main component window tree, layout managers, and custom text areas.
* **Event Handling:** **Java AWT (Abstract Window Toolkit)** — Handled low-level graphics rendering, click events, and window state changes.
* **File I/O:** **Java I/O Package** — Implemented `FileReader`, `FileWriter`, and high-performance `BufferedReader`/`BufferedWriter` streams for seamless disk access.

---

## 🚀 Future Roadmap

Here’s the game plan to take this project from a local desktop app to an enterprise system:

1. **Modernize the UI:** Migrate the legacy Swing layout over to a hardware-accelerated **JavaFX** setup for cleaner CSS styling and fluid animations.
2. **Upgrade the Search Engine:** Turn the keyword finder into a full regular expression (**RegEx**) search-and-replace pipeline.
3. **Complex Export Formats:** Build document parsers to export raw text files straight into formatted PDF or `.docx` formats.
4. **Cloud Sync & Persistence Engine:** Replace the local file fallback with an embedded **SQLite database caching layer** paired with a cloud backend for cross-device synchronization.
