Here is a comprehensive, polished `README.md` for your portfolio repository. It highlights the custom terminal logic, security-themed interactive elements, and modern UI design you have implemented.

---

# Ycdro OS – Interactive Personal Portfolio

A sleek, interactive personal portfolio website built with a focus on immersive user experience, zero-delay execution, and a minimalist aesthetic. The site features a custom "nuclear blackout" terminal intro, dynamic visitor telemetry, and seamless navigation.

## 🚀 Features

* **Zero-Delay Terminal Intro:** An unskippable, flash-free terminal boot sequence that silences the DOM upon load (`force-term`). It dynamically fetches and displays the visitor's live public IP address in the final sequence before dissolving into the homepage.
* **"Ask Anything" Telemetry Module:** A specialized interactive modal triggered via sidebar or keyboard shortcut (`Alt + K`). It analyzes and types out the user's browser, network, and geolocation telemetry (ISP, timezone, coordinates, memory) to demonstrate data visibility.
* **Minimalist Architecture:** Clean, glass-morphic certification cards and a streamlined sidebar navigation system anchored directly to homepage sections (`/#certs`).
* **Auditory Feedback System:** Engineered UI sound design utilizing the Web Audio API to generate synthetic keystrokes, hover states, and click acknowledgments dynamically. Includes a global mute toggle.
* **Advanced Keyboard Handling:** Custom event listeners for shortcut integrations and global blocking of specific browser shortcuts (e.g., `Alt + J`).
* **Responsive Theming:** Integrated Light, Dark, and System theme toggles synced with user preferences.

## 🛠️ Tech Stack

* **Frontend:** HTML5, CSS3, Vanilla JavaScript (ES6+)
* **APIs:** `ipinfo.io` & `api.ipify.org` (Geolocation & IP mapping)
* **Deployment & Hosting:** Vercel (Custom domain integration)

## 📂 Key File Structure

* `base.html` / `index.html`: Core structure housing the zero-delay protection script and anchor sections (`#projects`, `#skills`, `#certs`, `#writeups`).
* `chat.js`: The central logic controller. Handles the terminal boot sequence, dynamic IP fetching, Web Audio API sound synthesis, and the "Ask Anything" module.
* `_sidebar.html`: Primary navigation component featuring section anchoring, clock rendering, and theme toggles.
* `certifications.html` / `_certs.html`: Grid layout for glass-morphic credential displays.
* `style.css`: Global styling, CSS variables for theming, and layout configurations.

## ⚙️ Local Development

To run this project locally, you can use any standard local development server.

**Using Python:**

```bash
# Navigate to the repository directory
cd your-repo-name

# Start a local web server
python -m http.server 8000

```

Navigate to `http://localhost:8000` in your browser.

**Using Node (http-server):**

```bash
npx http-server

```

## 🔒 Security & Performance Notes

* **Adblocker Fallbacks:** The terminal IP fetcher includes dual-layer redundancy. It attempts `ipinfo.io` first, falls back to `api.ipify.org`, and defaults to `127.0.0.1` if network requests are strictly blocked by browser shields.
* **Zero-Flash Rendering:** The HTML `force-term` class ensures the homepage DOM is completely hidden during the intro sequence to prevent FOUC (Flash of Unstyled Content) or visual glitches.