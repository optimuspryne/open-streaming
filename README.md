# Open Streaming

A customizable, full-screen web launcher for your favorite streaming platforms. It presents user-friendly grid interface where you can organize, launch, and manage services like Netflix, Hulu, YouTube, Plex, and more.

---

##  Features

- **Modern interface** with support for logos and dynamic layouts  
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

## How I Use/Setup The Webpage For Use On A HTPC

1. I host the site on a local webserver I maintain, just make sure the streamingassets folder is in the same directory as openstreaming.html
2. I setup a Windows 11 PC (Using Tiny11 as the base OS) on a MicroPC to use as my HomeTheatre PC.  I setup 'Auto-Logon', then I installed Brave Browser and changed the HomePage and NewTab page to my hosted URL.
> I chose Windows 11 because I couldn't find a Linux Distro that could reliably access and play the content on various streaming platforms, but feel free to tinker with other distros, maybe you'll have better luck than me. 
3. I then modified the Registry to launch Brave Browser in Kiosk mode (A quick internet search will get you the steps for this) to save some resources that explorer.exe would typically use.  If you don't want to modify the registry you can always just create a simple Powershell or Batch script to run Brave in Kiosk mode during startup.  I'm not going to go into details on how to accomplish this.
4. I then purchased a wireless remote/keyboard combo (Rii Mini K25).  The website should function with almost any IR/Wireless remote or even just a keyboard/mouse.  Some of the streaming sites aren't optimized for using a remote so purchasing one that has the abilitly to simulate a mouse cursor is a must.
5. Now when I boot the HTPC is immediately logs in, starts Brave in Kiosk mode and opens the webpage by default.  I can press the 'home' button the remote to go back to openstreaming at anytime.


## How To Use WebPage Itself

2. Click **"Add from List"** to add popular streaming services instantly
3. Or, fill in the custom fields to add a new service manually
4. Use drag-and-drop to rearrange services as you like
5. Click the ❌ button on the top right to delete services
6. Use the **Export** / **Import** buttons to save or load layouts

> Tip: To use local images, place them in the `streamingassets/` folder and reference them like `streamingassets/myservice.png` in the Custom Image Path textbox.


