# Yu-OS

A small Windows 11 inspired desktop shell with a Yu Browser powered by Scramjet. The complete page is in [index.html](index.html).

## Run without npm

Open `index.html` directly in a browser. The desktop, Settings, dark mode, and History work without a server. YouTube and Spotify open in new tabs; other sites load directly when they allow embedding.

## Run with the Scramjet proxy

Install Node.js 18 or newer, then run:

```sh
npm install
npm start
```

Open [http://localhost:8080](http://localhost:8080). The proxy needs localhost or HTTPS because Scramjet uses a service worker, plus the Wisp endpoint served by this app.
