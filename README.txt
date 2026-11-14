SENTINEL HOME — Interactive 3D IoT Simulation
================================================

CONTENTS
- index.html: complete interactive browser simulation

RUN
1. Extract the ZIP file.
2. Open a terminal in the extracted folder.
3. Run a local static server:
   Python 3:  python -m http.server 8000
4. Open http://localhost:8000 in a modern browser.

You can also open index.html directly in many browsers, but a local server is
recommended because the 3D engine is loaded as an ES module.

REQUIREMENTS
- Internet connection on first load (Three.js and OrbitControls are loaded from jsDelivr CDN).
- Modern browser with WebGL enabled.

FEATURES
- Upgraded two-storey 3D cutaway miniature smart home with detailed rooms, furniture, roof, windows, porch and landscaping.
- Exactly four visible ESP32 development-board representations.
- Central Raspberry Pi 4 representation.
- Orbit, pan and zoom camera controls; realistic hinged entrance door that swings when the door approach event is triggered.
- Test triggers for door proximity, smoke, flame, rain and night activity.
- Day/night scene toggle, animated rain and Wi-Fi/MQTT data packets.
- Live dashboard, simulated telemetry and event log.

IMPORTANT TECHNICAL NOTE
This is a visual browser simulation. Sensor readings, MQTT messages, device
states and events are simulated locally in JavaScript. It does NOT connect to
physical ESP32 boards, a real Raspberry Pi, Wi-Fi or an MQTT broker. To make it
a live hardware dashboard, add a backend/API or MQTT-over-WebSocket bridge and
map the actual topic names and payload formats to the UI.

The house is a presentation-oriented two-storey architectural visualization. ESP32 and sensor forms are detailed visual representations, not manufacturing-accurate CAD. The HC-SR04 is placed beside the entrance facing the approach path; the door is mounted on a hinge and animated independently.
The design follows the specified architecture: four independent ESP32 nodes
publish through Wi-Fi/MQTT to a Raspberry Pi 4 hub; no PIR or servo is shown.
