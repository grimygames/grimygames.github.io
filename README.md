GrimyGames.com Web Portal

Welcome to the official repository for GRIMYGAMES.COM — the central hub for games, art, video, and design by Daniel Lee Kennedy. The site features portfolio galleries, custom web-based mini-games, dynamic live-stream status indicators, and links to all GrimyGames social and storefront presences.

🚀 Features

Responsive Dual-Layout: The site utilizes distinct .desktop and .mobile container structures toggled via CSS media queries to ensure a tailored experience on all devices.

Dynamic Live Stream Indicator: Uses a custom Vanilla JS fetch script to ping a local status.json file. If the streamer is live, the Picarto button dynamically glows hot-pink and updates its text.

Embedded HTML5 Mini-Game: Features an embedded, fully playable 300x250 web game (Molotov World) built with Phaser 3, tracking both local player scores and a global community world score.

Rich Animations: Powered by GSAP (TweenMax) for smooth, staggered entrance animations, bouncing UI elements, and interactive hovers.

Portfolio & Merch Hub: Direct portals to itch.io builds (Super Dumpster Dive, Panties On My Face, etc.) and Threadless merchandise.

🛠️ Technology Stack

Frontend: HTML5, CSS3, JavaScript (ES6)

Frameworks & Libraries:

Bootstrap (Grid and responsive layout)

Semantic UI (UI components)

jQuery (DOM manipulation and smooth scrolling)

GSAP / TweenMax (Advanced animations)

Slick Carousel (Sliders)

Game Engine: Phaser 3 (For bottle-game.html)

Analytics & Marketing: Google Analytics (gtag.js), Claspo

📂 Project Structure

/
├── index.html           # Main landing page (desktop & mobile layouts)
├── index_2.html         # Updated landing page with embedded mini-game
├── bottle-game.html     # Standalone Phaser 3 mini-game ("Molotov World")
├── status.json          # Manual boolean toggle for the Live Stream indicator
├── css/                 # Stylesheets (Bootstrap, Semantic, Custom, Animate, etc.)
├── js/                  # Scripts (jQuery, GSAP, Lightbox, custom behaviors)
├── img/                 # Core site imagery, banners, and thumbnails
│   ├── banners/         # Header graphics
│   ├── icon/            # Social media and storefront icons
│   ├── thumb/           # Game and shirt preview thumbnails
│   └── game/            # Specific assets for bottle-game.html
└── audio/               # Sound effects for bottle-game.html


💻 Local Development & Setup

Because this site uses the fetch() API for the live stream indicator (status.json) and Canvas/WebGL for the Phaser mini-game (bottle-game.html), it cannot simply be double-clicked directly from your hard drive (e.g., file:///C:/index.html). Browsers will block these requests due to CORS security policies.

To run the site locally:

Clone the repository:

git clone https://github.com/yourusername/grimygames.git
cd grimygames


Start a local web server:

Using VS Code: Install the Live Server extension, right-click index.html, and select "Open with Live Server".

Using Python:

python -m http.server 8000


Using Node.js:

npx serve


View the site: Open your browser and navigate to http://localhost:8000 (or whatever port your server provides).

🎮 Updating the Mini-Game (Molotov World)

The mini-game is isolated in bottle-game.html and injected into the main site via <iframe>.

Assets: To swap game graphics or audio, replace the corresponding files in the img/game/ and audio/ folders.

Configuration: Open bottle-game.html and locate the ASSETS_CONFIG block at the very top of the script to tweak drop speeds, target window difficulty, bottle positioning, and credits text.

🔴 Toggling the Live Stream Indicator

To manually show that you are live streaming on Picarto:

Open status.json.

Change "isLive": false to "isLive": true.

Save the file. The site will automatically pull this data and apply the .is-live CSS classes to your social icons.

© License & Copyright

© GRIMYGAMES.COM. All games, art, video, and design assets are the property of Daniel Lee Kennedy unless otherwise specified.
