# WRS Section 2 — Issues with the Preliminary Definition Given

## 2.1 Issues with "Domain, Stakeholders, Functional and Non-Functional Objectives"

### DI1 — Stakeholder roles

| | |
|---|---|
| Original statement | "Staff members in the accessibility department and the police might also be considered secondary stakeholders." |
| Classification | Ambiguous, Incomplete |
| Issue | Accessibility staff and police are listed as stakeholders, but nothing says what they do in the system or what the system expects from them. Nothing says who creates or maintains the building maps either, though navigation can't work without them. |
| Option 1 | List them as stakeholders only, with no defined role. |
| Option 2 | Give each stakeholder a concrete responsibility tied to an app function. |
| Decision | Option 2 |
| Rationale | Every stakeholder should justify a requirement. Accessibility staff manage spatial data (maps, temporary closures); Facilities manage physical infrastructure (beacons); Campus Police receive emergency escalations via standard cellular telephony. This eliminates map maintenance ambiguity. |
| Satisfied by | §3.1.3.2 Stakeholders, WA7 |

### DI2 — Connected buildings

| | |
|---|---|
| Original statement | "...going from one location to another in the same or different buildings that are connected to each other." |
| Classification | Inconsistent |
| Issue | The domain is described as "indoors" (a multi-floor building the user is familiar with), but this objective adds travel between buildings without saying whether the connectors (skybridges, tunnels, outdoor walkways) are in scope. |
| Option 1 | A single building only. |
| Option 2 | Multiple buildings, joined only by **indoor** connectors that are mapped. |
| Option 3 | The whole campus, including outdoor paths between buildings. |
| Decision | Option 2 |
| Rationale | This keeps the definition's own objective (connected buildings) while staying indoors. Outdoor travel adds GPS, traffic, and weather, which are outside an indoor app. |
| Satisfied by | ID1, FR8 |

### DI3 — Destinations inside shared spaces

| | |
|---|---|
| Original statement | Masterlist: "Navigation is limited for going from one room/location to another, NOT inside each room." |
| Classification | Ambiguous |
| Issue | Some locations can only be reached by walking **through** another room (e.g., a study room inside a library, or an office inside a department suite). It isn't clear whether routing through a room breaks the "not inside rooms" rule. |
| Option 1 | Never route through any room; such destinations are unreachable. |
| Option 2 | Route through rooms the map tags as **public pass-through** spaces (library, lobby, atrium); never through private rooms. |
| Decision | Option 2 |
| Rationale | Option 1 would leave real destinations unreachable. Public pass-through spaces act like hallways, so the room-to-room rule still holds for private rooms. |
| Satisfied by | ID2, FR3 |

### DI4 — Navigating between floors

| | |
|---|---|
| Original statement | "...the domain will be indoors, which can consist of multiple floors..." |
| Classification | Incomplete |
| Issue | The domain mentions multiple floors, but no requirement covers changing floors: finding the elevator or stairs, choosing between them, or confirming the user reached the right floor. The Masterlist assumes users can **operate** an elevator or stairs, but not that they can **find** one. |
| Option 1 | Leave floor changes entirely to the user. |
| Option 2 | THEIA guides the user to the elevator or stairs (by preference), says which floor to go to, and confirms the floor afterwards from beacons. The user operates the elevator or stairs. |
| Decision | Option 2 |
| Rationale | Prioritize beacon validating floor entry and exit to eliminate wandering floor navigation (Scenario 3). |
| Satisfied by | ID3, FR8 |

### DI5 — "Use as many sensors as possible" *(new)*

| | |
|---|---|
| Original statement | "...use of as many sensors that are available on an advanced smartphone would make your app more helpful." |
| Classification | Ambiguous, Unsound |
| Issue | "As many as possible" isn't a testable requirement. Running every sensor all the time drains the battery and raises privacy concerns (camera, microphone), and some sensors add nothing for indoor navigation. |
| Option 1 | Use every available sensor all the time. |
| Option 2 | Use a defined set of sensors, each tied to a function. |
| Decision | Option 2 |
| Rationale | Each sensor must justify itself: Bluetooth (beacons → location), accelerometer and gyroscope (steps, falls), compass (heading), microphone (voice commands), speaker and vibration (output). The camera is used only when the user chooses to send a photo in an emergency. |
| Satisfied by | WA9, NFR5 |

---

## 2.2 Issues with "Functional Requirements"

### FRI1 — Suggesting the next action from schedule or habit

| | |
|---|---|
| Original statement | "Figuring out what the next action(s) would be, based on the user's schedule or habit, and suggesting/accepting the user's choice." Also bullet 1: "...suggest or confirm a possible destination location, utilizing the user's routine schedule or habit." |
| Classification | Ambiguous, Redundant |
| Issue | It doesn't say how THEIA "figures out" the next action: from location history, a schedule, or caretaker setup. The same idea also appears twice (bullets 1 and 7), which is redundant. |
| Option 1 | Learn habits automatically from location history. |
| Option 2 | Use a schedule and favorites entered by the user or caretaker. |
| Option 3 | Both. |
| Decision | Option 2 (merge the two bullets into one requirement) |
| Rationale | An entered schedule is predictable and avoids tracking the user's movements. The user always confirms, so a wrong suggestion costs only one "No." Automatic learning can be reconsidered in Phase II. |
| Satisfied by | FR13 |

### FRI2 — Emergency calls when location is lost

| | |
|---|---|
| Original statement | "Placing emergency calls and messages, possibly after detecting a fall or when the system has lost its current location." |
| Classification | Unsound, Incomplete |
| Issue | Losing the location happens routinely (between beacons, phone in a pocket). Treating that as an emergency would cause frequent false alarms. The statement also doesn't say who is contacted, or whether the user confirms first. |
| Option 1 | Automatically call for help whenever location is lost or a fall is detected. |
| Option 2 | Treat lost location as **off-route** and try to recover first. Contact someone only when the user says "Help," or after a fall with no response within 30 s. Text the caretaker first and offer campus police. |
| Decision | Option 2 |
| Rationale | Implement a 30 second verification window to mitigate false alarms, appending the last cached beacon coordinates to the outgoing distress text (Scenario 2). |
| Satisfied by | FR9, FR10 |

### FRI3 — Distance and direction instructions

| | |
|---|---|
| Original statement | "Telling the user to walk a distance (e.g., 2 minutes before turning, or walk for 30 steps, etc.)" and "Telling the user to stop at the right place to turn." |
| Classification | Ambiguous, Incomplete |
| Issue | It isn't clear which unit to use (minutes, steps, meters) or how early to warn before a turn. It also doesn't cover non-straight paths, such as a curved hallway or walking around a pillar or fountain. |
| Option 1 | Distances in meters or feet. |
| Option 2 | Steps plus approximate seconds, with left/right/slight-left directions. |
| Option 3 | Clock-face directions ("go to 2 o'clock"). |
| Decision | Option 2, plus a warning about 5 steps before each turn, "stop" at the turn, and descriptions of curves and fixtures to go around |
| Rationale | Steps are relative to the body and many blind users already count them, while meters are hard to judge without sight. Step length is calibrated per user. The early warning gives time to slow down, fixing Stevie's early turn (Scenario 1). |
| Satisfied by | FR4, FR5 |

### FRI4 — Detecting obstacles *(new)*

| | |
|---|---|
| Original statement | "Detecting obstacles and telling the user what to do in order to avoid collision." |
| Classification | Unsound, Ambiguous |
| Issue | A phone in a pocket or hand can't reliably detect obstacles with its sensors, and the statement doesn't say which obstacles count. Promising detection the app can't deliver is a safety risk. |
| Option 1 | Camera-based obstacle detection (the user holds the phone up). |
| Option 2 | Static obstacles stored in the building map, plus blockages reported by users and staff. Moving obstacles are left to the cane or guide dog. |
| Decision | Option 2 |
| Rationale | Delegate dynamic awareness to existing mobility aids. Restrict app responsibility to static map features and structural blockages. This keeps navigation hands free and consistent with the physical limitations of the usering while white canes and guide dogs are being used. |
| Satisfied by | FR6, FR7, WA5 |

### FRI5 — Presenting route options *(new)*

| | |
|---|---|
| Original statement | "Figuring out the routes to reach the destination, and informing the user of the options (if there are more than one), and accepting user's preference." |
| Classification | Incomplete |
| Issue | It doesn't say how many options to give or how to describe them by voice, since the user can't see a map. A long list read aloud is hard to remember. |
| Option 1 | Always pick one route automatically. |
| Option 2 | Read up to 3 routes, each with estimated time, number of turns, and floor changes; the user picks by number. |
| Decision | Option 2 |
| Rationale | Three options can be held in memory. The summary (time, turns, elevator or stairs) is what users need to choose. If the user doesn't answer within 10 s, THEIA picks the best route for the current mode. |
| Satisfied by | FR3 |

### FRI6 — Missing "Where am I?" function *(new)*

| | |
|---|---|
| Original statement | "More that you can think of." |
| Classification | Incomplete |
| Issue | The list has no way for the user to simply ask their current location, which is the first thing a blind user needs when disoriented. It's also needed before starting a route and when reporting a location to a helper. |
| Option 1 | Announce location only during navigation. |
| Option 2 | A "Where am I?" voice command (and gesture) available at any time. |
| Decision | Option 2 |
| Rationale | It's cheap to provide (beacons already give the location) and supports recovery when lost (Scenario 2). |
| Satisfied by | FR1 |

---

## 2.3 Issues with "Non-functional Requirements"

### NFRI1 — "Ubiquitous"

| | |
|---|---|
| Original statement | "The system shall be ubiquitous." |
| Classification | Ambiguous |
| Issue | "Ubiquitous" isn't defined or testable. It could mean every building, every phone, with or without internet, or always running. |
| Option 1 | Works everywhere (not feasible without beacons and maps). |
| Option 2 | Works in every **mapped** building, including without internet, and locates the user quickly. |
| Option 3 | Works on every phone model. |
| Decision | Option 2 |
| Rationale | It's measurable: maps are stored on the phone, location updates within 2 s of entering a beacon's range, and THEIA can be launched from the lock screen by voice. Emergency texts still need cellular. |
| Satisfied by | NFR5 |

### NFRI2 — "Fastest route"

| | |
|---|---|
| Original statement | "The system shall lead the user through the fastest route." |
| Classification | Ambiguous |
| Issue | "Fastest" isn't defined. It could mean shortest distance, fewest turns, or least time. For a blind user, a short route with many turns or an elevator wait may not be the quickest. |
| Option 1 | Shortest distance. |
| Option 2 | Fewest turns. |
| Option 3 | Least estimated walking time over accessible segments, adding time for turns and elevator waits. |
| Decision | Option 3 |
| Rationale | Time is what the user actually cares about when late for class. Adding turn and elevator time reflects how blind users slow down at turns. This matches the definition used in Scenario 3. |
| Satisfied by | NFR2 |

### NFRI3 — Safe, fast, and comfortable navigation

| | |
|---|---|
| Original statement | "...safe navigation, fast navigation, and comfortable navigation" (§1), and the matching NFRs in §3. |
| Classification | Incomplete, Inconsistent (they can conflict) |
| Issue | None of the three is defined in terms of what the app does, and they can conflict: the fastest route may use stairs or a crowded atrium, which is less safe or comfortable. Nothing says which one wins. |
| Option 1 | One fixed balance of the three, decided by the app. |
| Option 2 | The user picks a mode (Fast, Safe, or Comfortable), and the basic safety rules apply in every mode. |
| Decision | Option 2 |
| Rationale | Users' needs differ, and even one user's needs change between trips (late for class vs. tired). Keeping safety rules in every mode means choosing "Fast" never makes a route unsafe. |
| Satisfied by | FR12, NFR1, NFR3 |

### NFRI4 — Who customizes the app

| | |
|---|---|
| Original statement | "The system shall be customizable to every user: e.g. volume, the interval of instructions, etc." vs. §1: "a caretaker ... who sets the configuration of the app." |
| Classification | Inconsistent |
| Issue | §1 says the caretaker sets the configuration, while §3 says it is customizable to every user. It's unclear who may change which settings. |
| Option 1 | Caretaker only. |
| Option 2 | User only. |
| Option 3 | Two levels: the caretaker sets safety settings (emergency contacts, fall detection, default mode) behind a PIN, and the user changes comfort settings (volume, speech rate, interval, mode) by voice at any time. |
| Decision | Option 3 |
| Rationale | Isolate system configuration by operational impact. Comfortable UI metrics (volume, speech tempo) remain dynamic and voice controlled by the primary user. Critical safety variables (emergency contacts, fall metrics) are walled behind a caretaker PIN to eliminate accidental disabled states. |
| Satisfied by | FR11, NFR6 |

### NFRI5 — Alerting nearby pedestrians

| | |
|---|---|
| Original statement | "The system shall help the user safely navigate indoors." |
| Classification | Incomplete |
| Issue | Safety could include making nearby pedestrians aware of the user so they step aside, but the definition doesn't mention people around the user. |
| Option 1 | THEIA plays an audible alert to warn nearby pedestrians. |
| Option 2 | Treat moving people as out of scope; the cane or guide dog already signals the user to others. |
| Decision | Option 2 |
| Rationale | The Masterlist puts moving obstacles (pedestrians) out of scope. An alert sound would be socially awkward for the user and could compete with THEIA's own voice instructions. It can be revisited in Phase II. |
| Satisfied by | WA5 (documented as out of scope), FR6 |

### NFRI6 — "Usable for blind people" *(new)*

| | |
|---|---|
| Original statement | "The system shall be usable for blind people." |
| Classification | Ambiguous |
| Issue | "Usable" isn't defined or measurable. The definition mentions voice recognition, but voice fails in noisy hallways, and nothing says how the user interacts without the screen. |
| Option 1 | Voice only. |
| Option 2 | Voice plus a standard screen reader over a normal visual interface. |
| Option 3 | Every function is available by voice **and** by a simple gesture, with audio and vibration feedback, and nothing requires reading the screen. |
| Decision | Option 3 |
| Rationale | Gestures back up voice in noise, vibration backs up audio when it's hard to hear, and the result is testable: core tasks can be completed without sighted help, and navigation starts within 2 voice commands. |
| Satisfied by | NFR4 |

### NFRI7 — "Easily extensible" *(new)*

| | |
|---|---|
| Original statement | "The system shall be easily extensible to accommodate the following typical variations: variations in interface, language, definitive needs of the user, new features, new sensors and hardware, etc." |
| Classification | Ambiguous |
| Issue | "Easily extensible" has no measure, and the list ends in "etc." Without limits, this could mean anything. |
| Option 1 | Every variation needs a new app release. |
| Option 2 | Define extension points: new buildings via map data, new languages via resource files, new sensors via a sensor module. |
| Decision | Option 2 |
| Rationale | Adding a building is the most common change and shouldn't need an app update. Separating languages and sensors makes the other listed variations testable. |
| Satisfied by | NFR7 |

---

## Summary

| Section | Issues | Count |
|---|---|---|
| 2.1 Domain / Stakeholders / Objectives | DI1–DI5 | 5 |
| 2.2 Functional | FRI1–FRI6 | 6 |
| 2.3 Non-Functional | NFRI1–NFRI7 | 7 |

Preliminary definition statements still without an issue (optional, if time allows): "Accepting from the user the destination location" and "The system shall lead the user through the route that the user would feel the most comfortable with" (partly covered by NFRI3).
