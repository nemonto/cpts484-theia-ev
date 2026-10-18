# WRS Section 3 — Improved Understanding (D-3)

**Author:** Justus Jones · **Co-author:** Austin Aragon · **Built from:** WRS §2 (`WRS-Section2-Updated.md`), checked against the THEIA Preliminary Definition v1.0 (§3.3.4)

This section works on its own. It derives Problems → Goals → Objectives → Requirement
Specifications from the issues and decisions in §2. IDs that §2 cites in its "Satisfied by" rows
(FR1–FR13, NFR1–NFR7, WA5/WA7/WA9, ID1–ID3, §3.1.3.2) keep those meanings here, so §2 and §3
stay consistent.

---

## 3.1 Improved Understanding

### 3.1.1 Problems

| ID | Problem | Source issues |
|---|---|---|
| P1 | Blind and visually impaired (BVI) users can't tell where they are inside a building, or which floor they're on, without sighted help. | FRI6, DI4 |
| P2 | BVI users can't find or compare routes to a destination, especially across floors or connected buildings. | FRI5, DI2, DI3, DI4, NFRI2 |
| P3 | Directions given as minutes or meters are hard to follow without sight. Users turn too early or too late, and curved paths and fixtures confuse them. | FRI3 |
| P4 | Static obstacles and temporary blockages (closures, construction) aren't known before the user reaches them. | FRI4, NFRI5 |
| P5 | Users who get lost or fall may not be able to get help quickly, but automatic alarms on every location loss would be mostly false. | FRI2 |
| P6 | Users have different and changing needs (speed vs. safety vs. comfort, volume, pace), and it isn't clear who controls which setting. | NFRI3, NFRI4 |
| P7 | Users have to enter the same destinations over and over even though their days follow a routine. | FRI1 |
| P8 | Vague quality claims in the definition ("ubiquitous", "usable", "extensible", "as many sensors as possible") can't be tested, so the app can't be shown to meet them. | NFRI1, NFRI6, NFRI7, DI5 |

### 3.1.2 Goals

| ID | Goal | Problem |
|---|---|---|
| G1 | The user always knows where they are, including the floor. | P1 |
| G2 | The user can reach any mapped destination by a route they chose or accepted. | P2 |
| G3 | Instructions match how BVI users move: body-relative, timed, and warned in advance. | P3 |
| G4 | The user is warned about known obstacles and blockages, and routes avoid them. | P4 |
| G5 | Getting lost is recovered from first. Real emergencies reach a human quickly, with the user's location. | P5 |
| G6 | The user adjusts comfort settings themself. The caretaker protects safety settings. | P6 |
| G7 | Routine trips need little or no input. | P7 |
| G8 | Every quality claim has a measurable acceptance criterion. | P8 |

### 3.1.3 Domain, Stakeholders, Objectives

#### 3.1.3.1 Domain

The domain is **indoors**: one or more mapped campus buildings with multiple floors, joined only
by mapped **indoor** connectors (skybridges, tunnels).

| ID | Improved domain statement | Issue |
|---|---|---|
| ID1 | Inter-building travel is in scope only through mapped indoor connectors. Outdoor paths are out of scope. | DI2 |
| ID2 | Routes may pass through rooms tagged **public pass-through** in the map (library, lobby, atrium). They never pass through private rooms. Navigation inside a destination room is out of scope. | DI3 |
| ID3 | Changing floors is in scope. THEIA guides the user to the elevator or stairs, names the target floor, and confirms the floor from beacons. The user operates the elevator or stairs. | DI4 |

#### 3.1.3.2 Stakeholders

| Stakeholder | Type | Responsibility in the system |
|---|---|---|
| BVI user | Primary | Chooses destinations, routes, and modes. Changes comfort settings. Calls for help. |
| Caretaker | Secondary | Sets safety settings behind a PIN (emergency contacts, fall detection, default mode). Enters the schedule and favorites. Gets emergency texts first. |
| Accessibility department staff | Secondary | Maintain map data: rooms, pass-through tags, static obstacles, temporary closures. |
| Facilities | Secondary | Install and maintain beacons. |
| Campus police | Secondary | Receive emergency escalations by ordinary cellular call or text. |

#### 3.1.3.3 World Assumptions (adopted or added)

"Masterlist" means the assumption is adopted from the *World Assumptions Masterlist v1.0*.
"Added" means the team added it to resolve a §2 issue.

| ID | Assumption | Source | Issue |
|---|---|---|---|
| WA1 | Each room and significant location has a wireless beacon. In range of one, the phone receives its ID (e.g., "Room 301"). We also assume beacons at hallway junctions, connectors, elevators, and stair landings. The Phase I prototype simulates beacon signals. | Masterlist, extended (Added: junctions, connectors, elevators, landings) | NFRI1, DI4 |
| WA2 | Primary users can navigate between floors and can operate a normal elevator (get in and out, press buttons, recognize the correct floor) and/or use stairs. | Masterlist | DI4 |
| WA3 | Primary users can hear, understand, and speak English. So can caretakers. | Masterlist | NFRI6 |
| WA4 | Primary users are experienced with smartphone accessibility functions (home and volume buttons, voice commands). Caretakers are familiar with normal smartphone app use. | Masterlist | NFRI4, NFRI6 |
| WA5 | Obstacles are static (pillars, trash cans, corners, walls). Moving obstacles (pedestrians, vehicles) are out of scope. Users may also use a cane or guide dog and can operate it together with the app. | Masterlist | FRI4, NFRI5 |
| WA6 | Primary users are reasonably familiar with the building, but may not know every route, especially across floors or buildings. | Masterlist (first part); Added (second part) | DI2 |
| WA7 | Accessibility staff keep the map data current, and Facilities keep the beacons working. | Added | DI1 |
| WA8 | Navigation works without internet. Cellular service is needed only for emergency texts and calls. Emergency dial-out is necessary. | Masterlist (dial-out); Added (offline navigation) | NFRI1, FRI2 |
| WA9 | THEIA uses only Bluetooth (beacons), accelerometer and gyroscope (steps, falls), compass (heading), microphone (voice), and speaker and vibration (output). The camera is used only when the user chooses to send a photo in an emergency. | Added | DI5 |
| WA10 | Indoor navigation only, room/location to room/location, not inside rooms (finding a chair or table). | Masterlist (ID1 and ID2 refine this) | DI2, DI3 |

#### 3.1.3.4 Functional Objectives

| ID | Objective | Goal |
|---|---|---|
| FO1 | Report the user's current location and floor on request. | G1 |
| FO2 | Accept a destination by voice, gesture, favorite, or schedule. | G2, G7 |
| FO3 | Compute and present route options. | G2 |
| FO4 | Give turn-by-turn instructions in steps and seconds. | G3 |
| FO5 | Warn about static obstacles and blockages and route around them. | G4 |
| FO6 | Guide floor changes and connector crossings. | G2, G1 |
| FO7 | Detect off-route travel and recover. | G5 |
| FO8 | Escalate real emergencies with the user's location. | G5 |
| FO9 | Let the user and caretaker configure the app at separate levels. | G6 |
| FO10 | Suggest the next destination from the schedule. | G7 |

#### 3.1.3.5 Non-Functional Objectives

| ID | Objective | Goal |
|---|---|---|
| NFO1 | Safe: safety rules hold in every mode. | G4, G8 |
| NFO2 | Fast: "fastest" is defined and measurable. | G2, G8 |
| NFO3 | Comfortable: a mode that reduces stress (fewer turns, quieter routes). | G6, G8 |
| NFO4 | Usable without sight. | G3, G8 |
| NFO5 | Available ("ubiquitous") in every mapped building, offline. | G1, G8 |
| NFO6 | Customizable per user. | G6, G8 |
| NFO7 | Extensible at defined points. | G8 |

---

## 3.2 Requirement Specifications

### 3.2.1 Functional Requirements

Priority: **High** is needed for a user to complete a trip safely. **Medium** improves it. **Low** can wait for Phase II.

| ID | Requirement | Objective | Issue | Priority |
|---|---|---|---|---|
| FR1 | **Where am I.** When the user says "Where am I?" or uses the matching gesture (NFR4), THEIA shall announce the building, floor, nearest named landmark or room, and which way the user is facing within 2 s. This works at any time, not only during navigation. If no beacon is in range, THEIA shall say "Location unknown" and give the last known location and how long ago it was heard. | FO1 | FRI6 | High |
| FR2 | **Destination input.** THEIA shall accept a destination by spoken room name or number, by choosing a saved favorite, or by accepting a schedule suggestion (FR13). It shall read the destination back and wait for "Yes" before routing. If the name matches more than one place, THEIA shall read up to 3 matches to choose from. If nothing matches, THEIA shall say it couldn't find that place and ask again. | FO2 | §2 summary (uncovered statement) | High |
| FR3 | **Route options.** THEIA shall compute routes through hallways, mapped indoor connectors, and public pass-through rooms (ID2). It shall read up to 3 routes, each with estimated time, number of turns, and floor changes (elevator or stairs). The user picks one by number. If there is no answer within 10 s, THEIA shall start the best route for the current mode (FR12). If no route exists (for example, every path is closed), THEIA shall say so and offer the nearest reachable point. | FO3 | FRI5, DI3 | High |
| FR4 | **Distance and direction.** Instructions shall give the distance in steps plus approximate seconds, and the direction as left, right, slight left, slight right, or straight. Step length shall be calibrated per user during setup. | FO4 | FRI3 | High |
| FR5 | **Turn timing and path shape.** THEIA shall warn about 5 steps before each turn ("In 5 steps, turn left") and say "Stop, turn left" at the turn. It shall describe curved hallways and fixtures the path goes around ("hallway curves right", "fountain ahead, keep left"). | FO4 | FRI3 | High |
| FR6 | **Static obstacles.** THEIA shall announce each mapped static obstacle on the route (pillars, benches, displays, steps) at least 5 steps before reaching it, with which side to pass on. THEIA shall not claim to detect moving obstacles (WA5). | FO5 | FRI4, NFRI5 | High |
| FR7 | **Blockages.** Accessibility staff can mark a hallway or door closed, and a user can report "Blocked" by voice. Either way, THEIA shall exclude that segment from routing and re-route any active navigation within 5 s. User reports expire after 2 hours unless staff confirm them. | FO5 | FRI4 | Medium |
| FR8 | **Floors and connectors.** For a floor change, THEIA shall guide the user to the elevator or stairs (by their preference), name the target floor, and confirm the floor from beacons after arrival. If the floor is wrong, THEIA shall say so and give directions back. Connector crossings shall be announced at entry and exit with the building name. | FO6 | DI2, DI4 | High |
| FR9 | **Off-route recovery.** If the user is more than 5 m from the route, or no beacon has been heard for 15 s during navigation, THEIA shall say "You may be off route," give the last known location, and re-route from the next location fix. Losing location shall never trigger an emergency on its own. | FO7 | FRI2 | High |
| FR10 | **Emergency escalation.** When the user says "Help", or when a fall is detected and the user doesn't respond within 30 s, THEIA shall text the caretaker with the last known beacon location (building, floor, nearest room) and offer to call the caretaker or campus police (emergency dial-out, WA8). If there is no cellular signal, THEIA shall tell the user, retry every 30 s, and send as soon as it connects. A false alarm can be cancelled within the 30 s by saying "I'm OK." The user may choose to attach a photo. | FO8 | FRI2 | High |
| FR11 | **Two-level settings.** The user shall change comfort settings (volume, speech rate, instruction interval, mode) by voice at any time. Safety settings (emergency contacts, fall detection on/off, default mode) shall be changed only after the caretaker PIN is entered. | FO9 | NFRI4 | Medium |
| FR12 | **Mode selection.** The user shall pick Fast, Safe, or Comfortable mode by voice, before or during a trip. The mode changes route ranking (NFR1–NFR3) but never turns off safety rules (NFR1). | FO9, FO3 | NFRI3 | Medium |
| FR13 | **Schedule suggestions.** Using the schedule and favorites entered by the user or caretaker, THEIA shall suggest the next destination when the app opens within 15 min before a scheduled event ("Your next class is CS 484 in Sloan 175. Go there?"). It acts only after the user says "Yes." THEIA shall not learn from location history. | FO10, FO2 | FRI1 | Low |

### 3.2.2 Non-Functional Requirements

| ID | Requirement | Acceptance criterion | Objective | Issue | Priority |
|---|---|---|---|---|---|
| NFR1 | **Safety rules in every mode.** Routes shall avoid closed segments (FR7), give obstacle warnings (FR6), and keep emergency escalation (FR10) available, whatever the mode. Safe mode also prefers elevators to stairs and avoids crowded atria tagged in the map. | Test routes in all three modes never include closed segments, and FR6/FR10 work in each mode. | NFO1 | NFRI3 | High |
| NFR2 | **Fastest route.** "Fastest" means the least estimated time over accessible segments: walking time at the user's calibrated pace, plus 3 s per turn, plus the mapped average elevator wait. | For a test map, the route ranked first in Fast mode has the lowest computed time. | NFO2 | NFRI2 | Medium |
| NFR3 | **Comfortable route.** Comfortable mode ranks routes by fewest turns and floor changes, as long as the route takes no more than 1.5× the fastest route's time. | For a test map, Comfortable mode picks the route with fewest turns within the 1.5× limit. | NFO3 | NFRI3 | Medium |
| NFR4 | **Usable without sight.** Every function shall be available by voice **and** by a simple gesture, with audio and vibration feedback. No task requires reading the screen. | BVI testers complete FR1, FR2, FR3, and FR10 without sighted help. Navigation starts within 2 voice commands. | NFO4 | NFRI6 | High |
| NFR5 | **Availability ("ubiquitous").** THEIA shall work in every mapped building without internet (maps stored on the phone), update location within 2 s of entering a beacon's range, and launch from the lock screen by voice. It shall use only the sensors in WA9. | With airplane mode on (except Bluetooth), FR1–FR9 pass in a mapped building. Location update time ≤ 2 s in 95% of trials. | NFO5 | NFRI1, DI5 | High |
| NFR6 | **Customizable.** Volume, speech rate, instruction interval, step length, elevator/stairs preference, and default mode shall be adjustable per user and kept between sessions, at the levels set in FR11. | Each setting changes behavior as specified and persists after restart. | NFO6 | NFRI4 | Medium |
| NFR7 | **Extensible.** A new building shall be added by loading map data with no app update. A new language shall be added through resource files only. A new sensor shall be added through the sensor module without changing routing code. | Adding a test building's map makes it routable without a new app release. | NFO7 | NFRI7 | Low |

---

## 3.3 Traceability

### 3.3.1 Problems → Goals → Objectives

| Problem | Goal | Functional objectives | Non-functional objectives |
|---|---|---|---|
| P1 | G1 | FO1, FO6 | NFO5 |
| P2 | G2 | FO2, FO3, FO6 | NFO2 |
| P3 | G3 | FO4 | NFO4 |
| P4 | G4 | FO5 | NFO1 |
| P5 | G5 | FO7, FO8 | — |
| P6 | G6 | FO9 | NFO3, NFO6 |
| P7 | G7 | FO2, FO10 | — |
| P8 | G8 | — | NFO1–NFO7 |

### 3.3.2 Objectives → Requirement Specifications

| Objective | Requirements |
|---|---|
| FO1 | FR1 |
| FO2 | FR2, FR13 |
| FO3 | FR3, FR12 |
| FO4 | FR4, FR5 |
| FO5 | FR6, FR7 |
| FO6 | FR8 |
| FO7 | FR9 |
| FO8 | FR10 |
| FO9 | FR11, FR12 |
| FO10 | FR13 |
| NFO1 | NFR1 |
| NFO2 | NFR2 |
| NFO3 | NFR3 |
| NFO4 | NFR4 |
| NFO5 | NFR5 |
| NFO6 | NFR6 |
| NFO7 | NFR7 |

### 3.3.3 §2 Issues → §3 Elements

| Issue | Resolved in |
|---|---|
| DI1 | §3.1.3.2, WA7 |
| DI2 | ID1, FR8 |
| DI3 | ID2, FR3 |
| DI4 | ID3, FR8 |
| DI5 | WA9, NFR5 |
| FRI1 | FR13 |
| FRI2 | FR9, FR10 |
| FRI3 | FR4, FR5 |
| FRI4 | FR6, FR7, WA5 |
| FRI5 | FR3 |
| FRI6 | FR1 |
| NFRI1 | NFR5 |
| NFRI2 | NFR2 |
| NFRI3 | FR12, NFR1, NFR3 |
| NFRI4 | FR11, NFR6 |
| NFRI5 | WA5, FR6 |
| NFRI6 | NFR4 |
| NFRI7 | NFR7 |

**Coverage check (SC-2):** every Goal traces back to a Problem and forward to at least one
Objective. Every Objective traces to at least one Requirement. Every §2 issue is resolved by at
least one §3 element. Every FR/NFR traces to an Objective.

### 3.3.4 Preliminary Definition → §3 Coverage

Every statement in the THEIA Preliminary Definition v1.0, and where §3 covers it.

| Def. § | Statement (short) | Covered by |
|---|---|---|
| 1 | Domain is indoors: multiple floors with classrooms, offices, bathrooms, lounges, elevators | §3.1.3.1, ID3, WA10 |
| 1 | Primary stakeholder: a blind person navigating indoors | §3.1.3.2 |
| 1 | Caretaker sets the configuration of the app | §3.1.3.2, FR11 |
| 1 | Caretaker comes to aid in an emergency (lost or injured) | FR9, FR10 |
| 1 | Accessibility staff and police as secondary stakeholders | §3.1.3.2, WA7 |
| 1 | Navigate between locations in the same or connected buildings | ID1, FR3, FR8 |
| 1 | Non-functional objectives: safe, fast, comfortable navigation | NFO1–NFO3, NFR1–NFR3 |
| 1 | Usability is a top priority; the user can't read the screen; use voice recognition | NFO4, NFR4 (High) |
| 1 | Use as many smartphone sensors as possible | WA9, NFR5 (narrowed per DI5) |
| 2 | Accept the destination; suggest or confirm one from schedule or habit | FR2, FR13 |
| 2 | Find routes, present options, accept the user's preference | FR3, FR12 |
| 2 | Tell the user to walk a distance (minutes, steps) | FR4 |
| 2 | Tell the user to stop at the right place to turn | FR5 |
| 2 | Detect obstacles and say how to avoid them | FR6, FR7, WA5 |
| 2 | Emergency calls and messages after a fall or lost location | FR9, FR10 (lost location is off-route first, per FRI2) |
| 2 | Suggest the next action from schedule or habit | FR13 (merged with bullet 1, per FRI1) |
| 2 | "More that you can think of" | FR1, FR7, FR8, FR11 |
| 3 | Help the user navigate safely | NFR1 |
| 3 | Lead the user through the fastest route | NFR2 |
| 3 | Lead the user through the most comfortable route | NFR3 |
| 3 | Usable for blind people | NFR4 |
| 3 | Ubiquitous | NFR5 |
| 3 | Customizable to every user (volume, instruction interval) | FR11, NFR6 |
| 3 | Easily extensible (interface, language, user needs, features, sensors, hardware) | NFR7 (limited to buildings, languages, sensors per NFRI7) |

### 3.3.5 Requirements → Prototype (D-4)

Where each functional requirement appears in the *Theia Prototype Mock-Up*. "—" means the
mock-up doesn't show it yet. Screens 3 and 5 are images only, so their rows are mapped by slide title and should be checked against the slides.

| FR | Prototype feature |
|---|---|
| FR1 | Screen 2 (two-finger tap); voice command "Where am I?" |
| FR2 | Screen 1, Voice Home ("Take me to ___"; confirm by "Yes" or double-tap) |
| FR3 | Screen 2, Navigation (elevator): choose a route by saying "1" or "2" |
| FR4 | Screen 2, Navigation |
| FR5 | Screen 2, Navigation (short buzz = turn now) |
| FR6 | Screen 2, Navigation |
| FR7 | Voice command "This way is blocked" |
| FR8 | Screen 2, Navigation (elevator) |
| FR9 | Screen 3, Off-route (3 buzzes) |
| FR10 | Screen 4, Help (say "Help" or two-finger hold); Screen 4, fall check |
| FR11 | Screen 5, Settings |
| FR12 | Screen 5, Settings |
| FR13 | — |
