# Open Streaming

A customizable, full-screen web launcher for your favorite streaming platforms. It presents user-friendly grid interface where you can organize, launch, and manage services like Netflix, Hulu, YouTube, Plex, and more.

---

##  Features

- **modern interface** with support for logos and dynamic layouts  
- **Preloaded popular services** for easy one-click addition  
- **Custom service input** for adding any website with a custom label and image  
- **Drag-and-drop rearrangement** of service tiles  
- **One-click deletion** of unwanted services  
- **Export/Import layout** as JSON files to back up or transfer your setup  
- **Mouse + IR remote/keyboard navigation** support
  
---

## Folder Structure

```
open-streaming/
├── openstreaming.html         # Main launcher HTML file
├── streamingassets/           # Folder for local service images
│   ├── netflix.png
│   ├── hulu.png
│   ├── emby.png
│   └── finallogo.png
└── layout.json                # (Optional) Saved user layout
```

---

## How to Use

1. **Open `openstreaming.html` in a browser** (Chrome recommended)
2. Click **"Add from List"** to add popular streaming services instantly
3. Or, fill in the custom fields to add a new service manually
4. Use drag-and-drop to rearrange services as you like
5. Click the ❌ button to delete services
6. Use the **Export** / **Import** buttons to save or load layouts

> Tip: To use local images, place them in the `streamingassets/` folder and reference them like `streamingassets/myservice.png`.

---

## Tech Stack

- HTML, CSS, JavaScript (no frameworks)
- Fully client-side — no backend or internet required after setup

---

## Optional Enhancements

- Add a browser shortcut or launch in kiosk mode
- Package with Electron or CEF to turn it into a native fullscreen desktop app


