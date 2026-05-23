# 📝 Jotter — Lightweight Extensible Text Architecture

Jotter is a highly modular, multi-window desktop text editor engineered using Java, designed to deliver high-performance document handling, custom rich-text manipulation, and inline multimedia insertion. Built with a focus on clean event scheduling and robust file serialization, Jotter serves as a lightweight alternative to traditional desktop word processors.

![Java](https://img.shields.io/badge/Language-Java-red?style=flat-square)
![GUI](https://img.shields.io/badge/GUI-Swing%20%2F%20AWT-orange?style=flat-square)
![Architecture](https://img.shields.io/badge/Pattern-MVC-blue?style=flat-square)

---

## 🛠️ System Capabilities

* **Advanced Document Control:** Implements atomic file operations including stream-based creation, disk serialization (Open/Save routines), printing integration, and native clipboard interfacing (Cut, Copy, Paste, Selection buffers).
* **Dynamic Document Metrics:** Real-time character and word-token parse metrics computed passively via listener hooks on the primary text document and displayed via a stateful status bar.
* **Multi-Instance Processing:** Built to support concurrent application execution paths, enabling users to spawn multiple independent text-editing windows running on separate threads.

---

## 🚀 Key Engineering Contributions & Logic

While this was a collaborative initiative at CPUT, my specific responsibilities focused on the architectural design of high-utility features, text parsing engines, and project branding:

### 🔍 1. High-Performance Search & Token Highlighting Engine
* **The Logic:** Developed an asynchronous document search routine that traverses the text model to identify keyword sub-strings.
* **The Implementation:** Integrated a custom text-attribute highlighting engine. It computes string token indices using positional offsets and applies a background painter overlay to all concurrent matches without disrupting UI layout threads.

### 🖼️ 2. Inline Multimedia Ingestion Pipeline
* **The Logic:** Designed a system to process and embed external imagery directly within a text document canvas.
* **The Implementation:** Managed file parsing routes to stream, read, and render external image dimensions inline, mapping spatial element wrappers inside the rich-text component boundaries.

### 🎨 3. Corporate Visual Identity & Asset Generation
* Generated the vector-based visual assets, desktop iconography, and structural branding systems representing the runtime environment.

---

## 🔬 Technology Stack & Core API Integrations

* **Language & Runtime:** Java SE (Standard Edition)
* **UI Framework:** **Java Swing** — Utilized for component containment trees, customizable text components, and absolute layout designs.
* **Event Handling & Graphics:** **Java AWT (Abstract Window Toolkit)** — Leveraged for window action tracking, coordinate tracking, layout triggers, and low-level component rendering pipelines.
* **File Architecture:** **Java I/O System** — Engineered robust `File` handling, `FileReader`/`FileWriter` character streams, and high-performance buffered streams (`BufferedReader`/`BufferedWriter`) to safely execute disk read/write cycles.

---

## 🛣️ System Architecture Roadmap

To scale the codebase into a enterprise-ready system architecture, the following engineering sprints are mapped out for subsequent versions:
