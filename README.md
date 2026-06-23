# 🏔️ Superstition Mountains — 3D LIDAR Terrain Viewer

An interactive 3D map of Arizona's Superstition Mountains and the Apache Trail canyons,
built from real **USGS lidar elevation data**, with satellite imagery, hiking trails,
and landmarks you can fly around in your web browser.

---

## 👉 Just want to look at it? Click this link:

### **https://scking21.github.io/Superstition-Mountains-/**

That's it. It opens in your web browser — no download, no installing anything.
Works on a computer (Chrome, Safari, Edge, Firefox). Give it a few seconds to load the terrain.

> 📱 It works best on a laptop or desktop. On a phone it will load but the controls are harder to use.

---

## 🖱️ How to move around

| What you want to do | How |
|---|---|
| **Tilt / rotate** the view | Hold the **left** mouse button and drag |
| **Slide the map around** (like Google Earth) | Hold the **right** mouse button and drag |
| **Zoom in and out** | **Scroll** the mouse wheel |
| **Fly around freely** | Tick the **"Free-fly (WASD)"** box, then use the **W A S D** keys |
| **Jump to a place** | **Click any blue label** (like "Weavers Needle") and it flies you there |

Use the panel in the top-left corner to turn things on and off:
satellite photos, hiking trails, landmark labels, a flat top-down map view,
the sun direction, and how tall the mountains look.

---

## 📥 Want your own copy to keep?

1. Near the top of this page, click the green **`< > Code`** button.
2. Click **Download ZIP**.
3. Find the downloaded file and **unzip it** (double-click it).

You now have all the map data, including the raw lidar elevation file. To actually
*view* it, the easiest way is still the link above — but see the next section if you
want to run it on your own computer offline.

---

## 🗺️ What's inside

| File | What it is |
|---|---|
| `index.html` | The 3D map viewer (the whole app is this one file) |
| `heightmap.bin` / `heightmap.json` | The elevation data, ready for the viewer |
| `satellite.jpg` | Aerial/satellite photo draped over the terrain |
| `trails.json` | Hiking trails + roads (from OpenStreetMap) |
| `superstition_dem.tif` | The **raw USGS lidar elevation** GeoTIFF (for GIS / mapping folks) |

**Coverage:** ~39 × 31 km, about 5.2 million elevation points, from 465 m to 1,907 m
(1,526–6,256 ft) elevation.

**Landmarks:** Weavers Needle, Flatiron, Superstition Mountain, Battleship Mountain,
Miners Needle, Fremont Saddle, Bluff Spring, Coronado Mesa, Fish Creek Canyon,
Fish Creek Hill, Fish Creek Bridge, Horse Mesa Dam, Apache Lake, Canyon Lake,
Tortilla Flat, and the trailheads.

**Trails & roads:** Peralta, Dutchman, Bluff Spring, Siphon Draw, Superstition Ridgeline,
Carney Springs, Lost Goldmine, Boulder Canyon, Second Water, Cavalry, Reavis Ranch,
Reavis Gap, Rogers Canyon, JF Trail, the Apache Trail (SR-88), and FR 79 to Horse Mesa Dam.

---

## 💻 Run it on your own computer (optional, a little technical)

Because the viewer loads data files, you can't just double-click `index.html` — your
browser blocks that for safety. You need to start a tiny local web server. If you have
**Python** installed (Macs usually do):

1. Open the **Terminal** app.
2. Type `cd ` (with a space), then drag the unzipped folder onto the Terminal window, and press **Enter**.
3. Paste this and press **Enter**:
   ```
   python3 -m http.server 8000
   ```
4. Open your browser and go to: **http://localhost:8000**
5. When you're done, press **Ctrl + C** in the Terminal to stop it.

(If that feels like too much — just use the web link at the top. It's the same thing.)

---

## 📜 Data sources & credit

- **Elevation:** [USGS 3DEP](https://www.usgs.gov/3d-elevation-program) lidar-derived elevation (public domain).
  - **Lidar vintage:** wilderness from the AZ Maricopa/Pinal 2020 collection (flown 2020–2021); the northern canyons (Horse Mesa Dam, Fish Creek, Apache Lake) from the CA/AZ FEMA Region 9 collection (flown 2018–2019).
- **Satellite imagery:** Esri World Imagery.
- **Trails, roads & place names:** [© OpenStreetMap contributors](https://www.openstreetmap.org/copyright) (ODbL).
- **3D graphics:** [three.js](https://threejs.org/).

Hand-placed landmark pins are approximate. Trails come straight from OpenStreetMap.
Not for navigation — for fun and exploration. 🌵
