# Open Streaming

A customizable, full-screen web launcher for your favorite streaming platforms. It presents user-friendly grid interface where you can organize, launch, and manage services like Netflix, Hulu, YouTube, Plex, and more.

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
```

---

## How I Use/Setup The Webpage For Use On A HTPC

> I purchased a wireless remote/keyboard combo (Rii Mini K25) that connects to the PC via USB Dongle.  The openstreaming site should function with almost any wireless remote that emulates keyboard arrow keys for it's directional buttons but most of the big streaming sites aren't programmed to work with nicely with arrow keys, so purchasing a remote that has the ability to emulate a mouse cursor is a must.

1. I host the html file on a local webserver I maintain, just make sure the streamingassets folder is in the same directory as openstreaming.html file.
2. I have a mini-PC that I installed Arch Linux on.  I'm using LXQt as the desktop environment and LightDM as the display manager.  I installed the following packages:
   - git
   - nano
   - chromium
   - xscreensaver.
4. I configured/changed Chromium's homepage, new tab page and default startup page to web addresss where I'm hosting the file.
5. I added the following command to startup: chromium --start-fullscreen (chromium --kiosk is an alternative option).  This was done via the LXQt session settings GUI.
6. I enabled autologin for the htpc user, you can do this by editing the lightdm config file at /etc/lightdm/lightdm.conf.  (Step will differ if you choose a different DM, DE or OS)
   - Find the section labeled **[Seat:*]** and uncomment this line **'autologin-user=your_username'** and replace **your_username** with the name of your user.
7. I needed to add this user to the 'autologin' group, so I ran these two commands:
   - sudo groupadd -f autologin
   - sudo gpasswd -a your_username autologin.
5. Now when I boot the HTPC it immediately logs in, starts Chromium fullscreen and opens the openstreaming webpage by default.  I can press the 'home' button on the wireless remote to go back to openstreaming page at anytime.
> I also setup xscreensaver, it's 100% optional but kind of fun to bring back the nostalgia of screensavers.

> This is also possible to do on a Windows PC but I don't recommend it because Windows is massive resource hog and also...why would you want to use anything other than Linux :)

## How To Use WebPage Itself

1. Use the **"Add a Popular Service"** to select a service.
2. Then click the **"Add from List"** button to add popular streaming services instantly.
3. Or, fill in the custom fields to add a new service manually.  For example, a locally hosted JellyFin instance.
> Tip: To use local images, place them in the `streamingassets/` folder and reference them like `streamingassets/myservice.png` in the custom image path textbox.  You can also enter a full URL to somewhere like steamgriddb.
> The .png assets for JellyFin and Emby are already included so when adding one of these services, leave the image url field blank.
5. Use drag-and-drop to rearrange services as you like.
6. Click the ❌ button on the top right to delete services.
7. Use the **Export** / **Import** buttons to save or load layouts in JSON format.

![openstreaming1](https://github.com/user-attachments/assets/3a4c6558-cf22-4b7a-8866-9c3811491d4b)

![openstreaming2](https://github.com/user-attachments/assets/4f8139c1-1bf6-4923-a3f1-bce7381a6629)

![openstreaming3](https://github.com/user-attachments/assets/d8dd19fe-7814-41b5-a696-16d27768c475)


