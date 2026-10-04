# Yu-OS

A small Windows 11 inspired desktop shell with a Yu Browser powered by Scramjet. The complete page is in [index.html](index.html).

## Run without npm

Open `index.html` directly in a browser. The desktop, searchable Start menu, browser-based Terminal, Settings, built-in and custom wallpapers, dark mode, session-only incognito mode, and History work without a server. Uploaded wallpapers are resized and saved in this browser on your device. Incognito mode keeps visits out of Yu-OS's local history; it does not control what websites record. The Terminal supports Yu-OS commands only; browser security does not allow it to run commands on your computer. YouTube and Spotify have dedicated app-style windows; without the Scramjet server, use the app window's **Open web app** button to launch the service in a new tab. Other sites load directly when they allow embedding.

## Run with the Scramjet proxy

Install Node.js 18 or newer, then run:

```sh
npm install
npm start
```

Open [http://localhost:8060](http://localhost:8060). The proxy needs localhost or HTTPS because Scramjet uses a service worker, plus the Wisp endpoint served by this app.

## Keep the Scramjet site online

The `render.yaml` file lets Render deploy this app as a web service. In Render, choose **New → Blueprint**, connect this GitHub repository, and let it use the settings in `render.yaml`. When deployment finishes, open the `onrender.com` address Render gives you. Scramjet should connect there without the Codespace running.

This uses Render's free plan. Free services sleep after being idle, so the first visit after a while can take up to about a minute to wake the site. Render supports the HTTPS and WebSocket connections this app needs. If you already have a public website address, add that address to the Render service's **Settings → Custom Domains** after deployment.
