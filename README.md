# 🎮 PixelWorld — Pixel Game Map Editor

> **Build your world, one tile at a time.**
>
> Design 2D game levels with pixel-style terrain, obstacles, and decorations. Paint maps in your browser, preview the layout, and export the result as JSON for use in your own games.

---

## ✨ Features

### 🧱 Tile Palette
- Choose from grass, dirt, water, sand, stone, trees, walls, lava, paths, flowers, water edges, and empty tiles.
- Select a tile and click or drag across the canvas to paint.
- Use the eraser to remove or clear tiles.

### 🛠️ Editing Tools
- **Paint:** Draw tiles onto the map.
- **Eraser:** Replace tiles with empty tiles.
- **Fill:** Fill a connected area containing the same tile type.
- **Sample:** Pick a tile directly from the map.
- **Undo / Redo:** Step backward and forward through editing changes.
- **Grid toggle:** Show or hide tile boundaries.

### 🗺️ Map Workspace
- Resize the map by setting its width and height.
- Choose a tile size of 20, 24, 32, or 40 pixels.
- View the map on the main canvas and in the mini-map preview.
- Monitor live map statistics, including total tiles, tile types used, ground tiles, and obstacles.

### 📥 JSON Import and Export
- Export your map as a formatted `.json` file.
- Import a previously exported JSON map to continue editing.
- Include map dimensions, tile size, tile legend, tile definitions, map name, and tile data in the exported JSON.
- Use the exported map data as a starting point for your own 2D game.

### 🎨 Browser-Based Interface
- Modern dark interface with a purple-accented design.
- Responsive layout for desktop and smaller screens.
- No account, backend server, database, or package installation required.

---

## 📂 Project Structure

```text
PixelWorld/
├── PixelWorld.html   # Complete application (HTML, CSS, and JavaScript)
└── README.md         # Project documentation
```

The application is contained in a single HTML file.

---

## ⚙️ Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/rsamwilson2323-cloud/PixelWorld.git
```

### 2. Open the project folder

```bash
cd PixelWorld
```

### 3. Run PixelWorld

Open `PixelWorld.html` in a modern web browser such as Google Chrome, Microsoft Edge, or Firefox.

**Windows:** Double-click `PixelWorld.html` to open it in your default browser.

No build step or development server is required.

---

## 🕹️ How to Use

1. Open `PixelWorld.html` in your browser.
2. Select a tile from the **Tile Palette**.
3. Choose a tool: Paint, Eraser, Fill, or Sample.
4. Click or drag on the map canvas to edit your level.
5. Change the map name, dimensions, or tile size in **Map Settings**, then click **Apply Map Settings**.
6. Use the mini-map and live statistics to review your layout.
7. Click **Export JSON** to preview the map data.
8. Choose **Download .json** to save the map file.
9. Use **Import JSON** to load a previously exported map.

### Keyboard shortcuts

| Shortcut | Action |
|---|---|
| `Ctrl + Z` or `Cmd + Z` | Undo |
| `Ctrl + Y` or `Cmd + Y` | Redo |
| `Esc` | Close the JSON dialog |

---

## 🧩 Tile Types

| ID | Tile | Category |
|---:|---|---|
| `0` | Grass | Ground |
| `1` | Dirt | Ground |
| `2` | Water | Terrain |
| `3` | Sand | Ground |
| `4` | Stone | Terrain |
| `5` | Tree | Obstacle |
| `6` | Wall | Obstacle |
| `7` | Lava | Hazard |
| `8` | Path | Ground |
| `9` | Flower | Decoration |
| `10` | Water Edge | Terrain |
| `11` | Empty | Special |

The map is stored as a two-dimensional array. Each number represents a tile ID from the table above.

Example:

```json
{
  "format": "PixelWorld Map",
  "version": 1,
  "name": "My Pixel World",
  "width": 3,
  "height": 2,
  "tileSize": 32,
  "map": [
    [0, 0, 1],
    [0, 2, 11]
  ]
}
```

This is a simplified example of the exported structure. Exported files also include tile definitions, a legend, and a creation timestamp.

---

## 🧠 Technology Stack

| Technology | Purpose |
|---|---|
| HTML5 | Application structure |
| CSS3 | Styling and responsive layout |
| JavaScript | Editing tools, map state, import/export, and interactions |
| HTML Canvas API | Rendering the map and mini-map |
| JSON | Portable map data format |

---

## 📦 Requirements

- A modern web browser with HTML5 Canvas support.
- No Node.js, Python, npm, backend, or database is required.
- The core application does not require an internet connection after the HTML file is available.

---

## 📌 Notes and Limitations

- Map dimensions are limited to **5–80 tiles wide** and **5–50 tiles high**.
- Available tile sizes are **20, 24, 32, and 40 pixels**.
- The editor exports tile data; it does not export a playable game.
- Game engines may need a small importer that maps each tile ID to the appropriate sprite or game object.
- The **Empty** tile is represented by ID `11`.
- Imported JSON must contain a consistent rectangular `map` array and supported tile IDs. Unknown tile IDs are converted to Grass.
- The editor's undo history is temporary and is not saved in exported JSON.

---

## 🚀 Ideas for Future Improvements

- Add custom tile sets and sprite-sheet importing.
- Support tile layers for terrain, objects, and collision data.
- Add map templates and procedural map generation.
- Export sprite sheets or image previews.
- Add collision and spawn-point markers.
- Support keyboard-based drawing and selection.
- Add zoom and pan controls for larger maps.
- Provide export presets for popular game engines.
- Add persistent browser storage for unfinished maps.

---

## 👨‍💻 Author

**Sam Wilson**

- GitHub: [@rsamwilson2323-cloud](https://github.com/rsamwilson2323-cloud)
- LinkedIn: [Sam Wilson](https://www.linkedin.com/in/sam-wilson-14b554385/)

## 📜 License

No specific license is stated in this README. Add a `LICENSE` file to the repository if you want to define the terms under which others may use, modify, or distribute the project.

---

<div align="center">

### 🎮 PixelWorld — Pixel Game Map Editor

**Design. Build. Export.**

*Made with HTML, CSS, JavaScript, and Canvas.*

</div>
