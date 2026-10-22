# Two TVs

One-screen remote for two Roku TVs. A single static page (`index.html`) that sends commands from your phone straight to each TV over home Wi-Fi using Roku's External Control Protocol (port 8060).

## Use

1. Serve the page over plain `http://` (the TVs don't speak HTTPS, and browsers block https → http requests):
   `python3 -m http.server 8000`, then open `http://<computer-ip>:8000` on your phone.
2. Tap ⚙︎ and enter each TV's name and IP (TV: Settings → Network → About).
3. Share → Add to Home Screen.

If a dot flashes green but the TV ignores it: TV Settings → System → Advanced system settings → Control by mobile apps → Network access → Permissive.

Edit the `APPS` list in `index.html` to change the app buttons.
